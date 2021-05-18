---
title: PidTagExchangeProfileSectionId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316429"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>PidTagExchangeProfileSectionId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine dynamisch generierte GUID, die zum Bestimmen eines Kontos verwendet wird, wenn Sie mehrere Microsoft Exchange Server verwenden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Kennung:  <br/> |0x3d150102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Mehrere Exchange-Konten  <br/> |
   
## <a name="remarks"></a>Hinweise

Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen mehrere Exchange konten anstelle eines Exchange Kontos. Um mehrere Exchange zu verwenden, wurde das MAPI-Profillayout geändert. In Microsoft Office Outlook 2007 und früheren Versionen enthielten Profile einen festen Profilabschnitt für Exchange-Einstellungen wie Servername, Benutzername und Offlineordnerdatei (OST). speicherort. Diese Einstellungen wurden mithilfe eines eindeutigen Bezeichners identifiziert, der **pbGlobalProfileSectionGuid-Eigenschaft.** Der abschnitt, der für Exchange einstellungen verwendet wird, wird als Exchange Global Profile Section bezeichnet. 
  
Ein fester Profilabschnittsspeicherort ist nicht mehr ausreichend, um mehrere Exchange aufnehmen. Stattdessen ist für jedes Exchange in Ihrem Profil ein Abschnitt vorhanden, der den Einstellungen für dieses Konto gewidmet ist. Der neue Abschnitt, der für Exchange verwendet wird, wird durch den eindeutigen Bezeichner **emsmdbUID identifiziert.**
  
Im Abschnitt Nachrichtendienstprofil für das Exchange finden Sie eine Eigenschaft, die eine GUID enthält, die dynamisch generiert wird, wenn das Konto erstellt wird. Diese GUID wird in der **PidTagExchangeProfileSectionId-Eigenschaft** gespeichert. Nachrichtenspeicher und Adressbuchcontainer machen eine Eigenschaft verfügbar, um zu bestimmen, Exchange sie gehören. Auf den Zugriff in der Tabelle "Nachrichtendienste" kann Exchange diese Eigenschaft verfügbar gemacht werden. 
  
Sie können diese Eigenschaft über einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) auf **PidTagExchangeProfileSectionId** abrufen, nachdem Sie eine der folgenden Schnittstellen abgefragt haben: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Wenn das Objekt nicht mit einer Exchange verbunden ist, gibt der Aufruf **MAPI_E_NOT_FOUND**.
  
Sie können Container für eine **PidTagExchangeProfileSectionId** einschränken, wenn Sie das Adressbuch anzeigen. Sobald Sie über einen geöffneten Container verfügen, können Sie **die emsmdbUID von** diesem abfragen. Es ist auch erwähnenswert, dass der Empfänger auch die **PidTagExchangeProfileSectionId** in der Liste der Eigenschaften enthält, wenn ein Empfänger aus einem Exchange-Adressbuch ausgewählt wurde. 
  
> [!NOTE]
> In den Codebeispielen und Funktionskopfzeilen wird diese GUID als **emsmdbUID bezeichnet.** 
  
Eines der Exchange wird als Legacykonto Exchange gekennzeichnet. In der Regel ist es das erste Konto, das dem Profil hinzugefügt wurde. Jeder Aufruf zum Öffnen **von pbGlobalProfileSectionGuid** wird an den globalen Exchange des Legacykontos umgeleitet. Das Objektmodell ruft Aufrufe auf, die mit dem Nicht-Legacy-Exchange interagieren, auch mit dem Legacykonto Exchange interagieren. 
  
Der legacy Exchange-Dienst verfügt über **die Eigenschaft PR_EMSMDB_LEGACY** (0x3D18000B), die in der Nachrichtendiensttabelle auf **true** festgelegt ist. 
  
Die ältere **emsmdbUID** wird auch im Abschnitt Outlook Global Profile des Profils als **PidTagExchangeProfileSectionId gestempelt.** Code, der zur Unterstützung mehrerer Exchange-Konten geschrieben wurde, sollte nicht die ältere **emsmdbUID** abrufen, da er die richtige **emsmdbUID** abrufen sollte, abhängig vom Konto, mit dem Ihr Code interagiert.
  
## <a name="see-also"></a>Siehe auch



[Verwenden mehrerer Exchange Konten](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

