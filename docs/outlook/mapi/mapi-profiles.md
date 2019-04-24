---
title: MAPI-Profile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340082"
---
# <a name="mapi-profiles"></a>MAPI-Profile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einem Profil werden Informationen zu Dienstanbietern und Nachrichtendiensten gespeichert, die auf einem Computer installiert sind. Bei jeder Sitzung wählt ein Client bei der Anmeldung ein Profil aus, das die zu verwendenden Anbieter und Dienste beschreibt. Ein Client kann aus einer Auflistung von Profilen auswählen und, falls gewünscht, eine als Standard festlegen. Das Standardprofil ist das Profil, das automatisch ausgewählt wird, wenn ein Client eine Sitzung startet und nicht explizit ein Profil angegeben hat.
  
Auch in diesen Themen finden Sie eine Erläuterung des Spitznamen Caches, der in einem binären Stream gespeichert wird.
  
- [Cache für Spitznamen](nickname-cache.md)
    
- [AutoVervollständigen-Stream](autocomplete-stream.md)
    
- [Analyse von Binärdateien](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Profilabschnitte

Profile sind in Abschnitte unterteilt, über die Clients und Dienstanbieter Benutzerprofileigenschaften anzeigen oder Konfigurationsänderungen vornehmen können. Ein Profil Abschnitt ist ein MAPI-Objekt, das die **IProfSect** -Schnittstelle implementiert, eine Schnittstelle, die von **IMAPIProp** abgeleitet wird und keine zusätzlichen Methoden aufweist. Weitere Informationen finden Sie unter [IProfSect: IMAPIProp](iprofsectimapiprop.md). Der einzige Zweck besteht darin, die Eigenschaften eines Profil Abschnitts zu ändern. Zum Abrufen eines **IProfSect** -Zeigers zu einem bestimmten Profil Abschnitt rufen Clients und Dienstanbieter die folgenden Methoden auf. 
  
|||
|:-----|:-----|
|Clients können Folgendes aufrufen:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Dienstanbieter können Folgendes aufrufen:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Entweder Clients oder Anbieter können Folgendes aufrufen:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Profile werden hierarchisch ähnlich wie die MAPISVC organisiert. INF-Datei. Oben in der Hierarchie gibt es Profilabschnitte mit Informationen, die für das Profil relevant sind. Die mittlere Ebene enthält Abschnitte, die Informationen zu einem bestimmten Nachrichtendienst enthalten, und die untere Ebene enthält Abschnitte, die Informationen zu einem der Dienstanbieter in einem Nachrichtendienst enthalten. 
  
Jedes Profil verfügt über mehrere erforderliche Eigenschaften, die in einem oder mehreren Abschnitten des Profils gespeichert werden. Jedes Profil verfügt beispielsweise über die Eigenschaften **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) und **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)). Der Suchschlüssel eines Profils wird auf den in MAPIGUID definierten Wert festgelegt. H als MUID_PROFILE_INSTANCE und ist immer garantiert einzigartig unter allen Profilen. Obwohl zwei Profile denselben Namen haben können, können Sie nicht denselben Suchschlüssel haben. Suchschlüssel sollten als binäre Daten anstelle von Daten eines bestimmten Typs behandelt werden.
  
Nachrichtenspeicher Anbieter müssen die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Nachrichtenspeichers in die Profilabschnitte für das Profil und für den Nachrichtenspeicher Anbieter aufnehmen und diese Einträge synchron halten. Wenn ein Nachrichtenspeicher erstellt wird, legt der Anbieter **PR_DISPLAY_NAME** basierend auf dem in diesen Profil Abschnitten gespeicherten Wert fest. 
  
Es gibt zwei Hauptunterschiede zwischen Profil Abschnitten und anderen Objekten, die von **IMAPIProp**erben: 
  
- Profilabschnitte unterstützen keine Transaktionen.
    
- Profilabschnitte unterstützen keine benannten Eigenschaften und geben MAPI_E_NO_SUPPORT aus Ihren **IMAPIProp:: GetIDsFromNames** -und **IMAPIProp:: GetNamesFromIDs** -Implementierungen zurück. Weitere Informationen finden Sie unter [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Da Profilabschnitte keine Transaktionen unterstützen, werden alle mit Aufrufen von **IMAPIProp:: CopyProps**, **CopyTo**oder SetProps vorgenommenen Änderungen sofort wirksam. **** Weitere Informationen finden Sie unter [IMAPIProp:: CopyProps](imapiprop-copyprops.md). Clients und Dienstanbieter können die **IMAPIProp:: SaveChanges** -Methode eines Profil Abschnitts aufrufen, die erfolgreich ausgeführt wird, aber keine Auswirkung auf die Profil Abschnittsdaten hat. Weitere Informationen finden Sie unter [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Wenn Änderungen sofort auftreten, kann sich dies auf die Implementierung der Eigenschaftenblätter auswirken, die von Clients zum Anzeigen von Profileigenschaften für Benutzer verwendet werden. Dienstanbieter, die möchten, dass Benutzer Änderungen verschieben oder rückgängig machen können, müssen ihre Eigenschaftenblätter mit Kopien von Profil Abschnitten anstelle der tatsächlichen Abschnitte implementieren. Mithilfe von Kopien können Benutzer Änderungen vornehmen und diese Änderungen später abbrechen, sodass die ursprünglichen Profilabschnitte unverändert bleiben. 
  
Die Reihenfolge, in der Informationen in einem Profil angezeigt werden, wirkt sich darauf aus, wie MAPI Ressourcen konfiguriert und Zuordnungen in einer Sitzung vornimmt. Die folgenden Zuordnungen sind von der Profilreihenfolge betroffen:
  
- Standardnachrichtenspeicher
    
- Persönliches Adressbuch
    
- Standardsuchpfad für Nachrichtenspeicher
    
- Standardsuchpfad des Adressbuchs
    
- Transport Anbieter Reihenfolge
    
MAPI legt den Standardnachrichtenspeicher als ersten Nachrichtenspeicher im Profil fest, für den das STATUS_DEFAULT_STORE-Flag in seiner **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt ist, was darauf hinweist, dass es sich um den Standardspeicher handeln kann. Clients können diese Einstellung außer Kraft setzen, indem Sie **IMAPISession:: SetDefaultStore**aufrufen. Weitere Informationen finden Sie unter [IMAPISession:: SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI erstellt einen Transportauftrag für die Verarbeitung von ausgehenden und eingehenden Nachrichten. Wenn mehr als ein Transportanbieter für eine Nachricht eines bestimmten Typs registriert ist, verwendet MAPI diese Reihenfolge, um zu bestimmen, welcher Anbieter die Nachricht behandeln soll. MAPI legt den Transportauftrag auf die Reihenfolge fest, in der die Transportanbieter dem Profil mit einer Ausnahme hinzugefügt wurden: die Übertragungen, die das STATUS_XP_PREFER_LAST-Flag in Ihrer **PR_RESOURCE_FLAGS** -Eigenschaft festgelegt haben, werden zuletzt in der Reihenfolge positioniert. Clients können den Transportauftrag durch Aufrufen von **IMsgServiceAdmin:: MsgServiceTransportOrder**festlegen. Weitere Informationen finden Sie unter [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Diese Richtlinien für die Bestellung von Dienstanbietern und Nachrichtendiensten können manchmal zu Konflikten kommen. Wenn ein Konflikt vorliegt, sollte der Code den Konflikt beheben. Sie können das Programm für die e-Mail-Systemsteuerung verwenden, um ein Profil zu prüfen, das Sie erstellt haben, um zu ermitteln, ob die Anbieter erwartungsgemäß konfiguriert wurden.
  

