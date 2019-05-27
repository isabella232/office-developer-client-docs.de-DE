---
title: Verwenden mehrerer Exchange-Konten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329653"
---
# <a name="using-multiple-exchange-accounts"></a>Verwenden mehrerer Exchange-Konten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen die Integration mit mehreren Exchange-E-Mail-Konten. In Outlook 2010 oder Outlook 2013 konnte ein Benutzer zwei Exchange-Konten zum gleichen Profil hinzufügen und dennoch umfangreiche Exchange-Funktionen wie die veröffentlichte globale Adressliste (GAL), die Exchange-Abwesenheitskonfiguration und die Ordnerfreigabe nutzen.
  
Wer mit den MAPI-Profilabschnitten für Microsoft Office Outlook 2007 und früher vertraut ist, weiß, dass Exchange-Einstellungen, wie der E-Mail-Benutzername und der Servername, im festen Exchange Global Profile-Abschnitt, **pbGlobalProfileSectionGuid**, gespeichert sind. In Outlook 2010 und Outlook 2013 benötigt jedes Exchange-Konto einen eigenen Profilabschnitt zum Speichern von Einstellungen, was **pbGlobalProfileSectionGuid** überflüssig macht. 
  
Die Exchange-Einstellungen für Outlook 2010 und Outlook 2013 sind weiterhin im Profil gespeichert, aber pro Profil wird dynamisch ein eindeutiger Bezeichner für den Profilabschnitt zugewiesen, der die Einstellungen enthält. Der Speicherort der Exchange-Einstellungen im Profil wird in der [kanonischen Eigenschaft "PidTagExchangeProfileSectionId"](pidtagexchangeprofilesectionid-canonical-property.md) gespeichert, die sich im Nachrichtendienst-Profilabschnitt des Exchange-Kontos befindet. Diese Eigenschaft finden Sie auch im Profilabschnitt für jeden Anbieter in diesem Nachrichtendienst des Kontos. Der eindeutige Bezeichner wird nicht auf dem Server gespeichert und unterscheidet sich von Profil zu Profil.
  
Outlook 2010 und Outlook 2013 verwenden **PidTagExchangeProfileSectionId** als eindeutigen Bezeichner, um ein Exchange-Konto anzugeben. Bei dieser Art der Verwendung wird dieser eindeutige Bezeichner **emsmdbUID** genannt. Für einige MAPI- und Outlook-Operationen kann eine **emsmdbUID** erforderlich sein, um anzugeben, welches Exchange-Konto für die Operation verwendet werden soll. 
  
Um mehrere Exchange-Konten zu unterstützen, müssen Sie bestimmte Aufrufe neuer Funktionen in Ihrem Code verwenden. Ersetzen Sie jeden Aufruf, der eine **entryID** und entweder [IAddrBook::OpenEntry](iaddrbook-openentry.md) oder [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) auf [IMailUser : IMAPIProp](imailuserimapiprop.md) und [IDistList : IMAPIContainer](idistlistimapicontainer.md) verwendet, durch eine der folgenden Funktionen. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>Legacyunterstützung

Alle MAPI-Clients, die vor der Erstellung dieses neuen **emsmdbUID**-Abschnitts geschrieben wurden, werden weiterhin unterstützt. Diese Clients rufen weiterhin den vorherigen globalen Abschnitt ab (**pbGlobalProfileSectionGuid**). Abfragen nach diesem Profilabschnitt werden an ein bestimmtes Exchange-Konto weitergeleitet, das Legacyanfragen verarbeitet. Das Konto, das die Legacyaufrufe verarbeitet, kann anhand der Nachrichtendiensttabelle und durch Hinzufügen einer Spalte für PR_EMSMDB_LEGACY bestimmt werden. Nur für einen Nachrichtendienst ist diese Einstellung auf "true" festgelegt, und sein **PidTagExchangeProfileSectionId** wird als Legacy-**emsmdbUID** bezeichnet.
  
> [!NOTE]
> Konfigurierbare MAPI-Einstellungen wie der Standardspeicher und das Standardkonto haben keinen Einfluss darauf, welches Konto Legacyaufrufe verarbeitet. Das Konto, das die Legacyaufrufe verarbeitet, kann nicht konfiguriert werden. 
  
Der **emsmdbUID** des Legacykontos wird in den Outlook Global Profile-Abschnitt kopiert. Wenn diese Eigenschaft nicht vorhanden ist, wird durch Abfragen nach der Nachrichtendiensttabelle ermittelt, welches Konto der Legacyhandler ist, und der Wert im Outlook Global Profile-Abschnitt festgelegt. 
  
Um es deutlich zu sagen: Der Outlook Global Profile-Abschnitt unterscheidet sich vom Exchange Global Profile-Abschnitt, und in Outlook 2010 und Outlook 2013 ist der Exchange Global Profile-Abschnitt nicht mehr wirklich global, da Sie mehrere Exchange Konten verwenden können. Der Outlook Global Profile-Abschnitt enthält Eigenschaften über Outlook, wie z. B. den Status des MRU-Ordners oder den Status der globalen Verbindung.
  
## <a name="address-book-account-contexts"></a>Adressbuch-Kontokontexte

Um Adressen mit mehreren Exchange-Konten korrekt aufzulösen, verwenden Sie die neuen Funktionen, die einen Kontenkontext berücksichtigen, sodass Aufrufe an das Adressbuch das richtige Exchange-Konto durchsuchen.
  
Einige frühere Adressbuch-APIs sind veraltet, da sie keine vollständige Unterstützung mehrerer Exchange-Konten boten. Dieser Kontokontext ist in der Regel eine **emsmdbUID**.
  
Neben der **emsmdbUID** haben mehrere Exchange-Konten auch eine **emsabpUID**.
  
1. Der Wert **emsmdbUID** gibt den Konto-Kontext. 
    
2. Der Wert **emsabpUID** identifiziert eine Exchange-Adressbuchanbieter. 
    
Der **emsabpUID**-Wert wird typischerweise bei der Auflösung eines Empfängers verwendet. Wenn Sie einen Empfänger mit [IAddrBook::ResolveName](iaddrbook-resolvename.md) auflösen, enthält eine Exchange-Empfängerzeile die Eigenschaft **PR_AB_PROVIDERS** (0x3D010102), die den **emsabpUID**-Wert enthält. Dieser **emsabpUID**-Wert identifiziert den Exchange-Adressbuchanbieter für den jeweiligen Empfänger. 
  
Wenn Sie den **emsabpUID**-Wert für eine bestimmte **emsmdbUID** ermitteln möchten, öffnen Sie den Profilabschnitt für **emsmdbUID**, und rufen Sie die Eigenschaft **PR_EMSABP_USER_UID** (0x0x3D1A0102) ab. 
  
Wenn Sie [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) aufrufen, stellen Sie sicher, dass die Exchange-Empfänger in der Liste, die Sie übergeben, die Eigenschaft **PR_AB_PROVIDERS** mit der **emsabpUID**-Eigenschaft enthalten, die dem Adressbuchanbieter entspricht, zu dem der Empfänger gehört. Der Aufruf von [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) in einer Zeile, die Sie von [IAddrBook::ResolveName](iaddrbook-resolvename.md) erhalten haben, erfordert keine zusätzliche Aktion, aber bestimmter Codes ruft [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) in Zeilen auf, die nur die Eigenschaft **PR_ENTRYID** enthalten. Zeilen in dieser und ähnlichen Situationen sollten sowohl **PR_ENTRYID** als auch **PR_AB_PROVIDERS** enthalten, deren Eigenschaft **PR_AB_PROVIDERS** auf die richtige **emsabpUID** festgelegt ist.
  
Eine einfache Beschreibung des Prozesses zum Auflösen mehrerer Exchange-Konten lautet wie folgt:
  
- Auf der Grundlage des angegebenen eindeutigen Dienstbezeichners sucht Ihr Code in der Tabelle des Nachrichtenspeichers der **PR_SERVICE_UID**-Eigenschaft, die mit Ihrem Dienstbezeichner übereinstimmt. Von dort aus können Sie den richtigen **PR_MDB_PROVIDER** ermitteln. Diese Zeile enthält den entsprechenden Speicher.
    
- Auf der Grundlage der angegebenen **emsmdbUID** sucht Ihr Code in der Nachrichtendiensttabelle nach der Zeile, die die **PidTagExchangeProfileSectionId** enthält, die der **emsmdbUID** übereinstimmt.
    
## <a name="see-also"></a>Siehe auch



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[Kanonische PidTagExchangeProfileSectionId-Eigenschaft](pidtagexchangeprofilesectionid-canonical-property.md)


[Öffnen des globalen Profilabschnitts](https://support.microsoft.com/kb/188482)

