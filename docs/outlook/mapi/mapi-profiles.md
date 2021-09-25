---
title: MAPI-Profile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ef17c0f1cfb3a4cf90e687616b299484be90f44b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610216"
---
# <a name="mapi-profiles"></a>MAPI-Profile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Profil speichert Informationen zu Dienstanbietern und Nachrichtendiensten, die auf einem Computer installiert sind. Für jede Sitzung wählt ein Client zur Anmeldezeit ein Profil aus, das die zu verwendenden Anbieter und Dienste beschreibt. Ein Client kann aus einer Sammlung von Profilen auswählen und bei Bedarf ein Profil als Standard festlegen. Das Standardprofil ist das Profil, das automatisch ausgewählt wird, wenn ein Client eine Sitzung startet und kein Profil explizit angegeben hat.
  
Außerdem finden Sie in diesen Themen eine Erläuterung des Spitznamencaches, der in einem binären Datenstrom gespeichert ist.
  
- [Cache für Spitznamen](nickname-cache.md)
    
- [Stream für automatisches Vervollständigen](autocomplete-stream.md)
    
- [Binäre Dateiparsing](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Profilabschnitte

Profile sind in Abschnitte unterteilt, auf die Clients und Dienstanbieter zugreifen können, um Benutzern Profileigenschaften anzuzeigen oder Konfigurationsänderungen vorzunehmen. Ein Profilabschnitt ist ein MAPI-Objekt, das die **IProfSect-Schnittstelle** implementiert, eine Schnittstelle, die von **IMAPIProp** abgeleitet ist und keine zusätzlichen Methoden aufweist. Weitere Informationen finden Sie unter [IProfSect : IMAPIProp](iprofsectimapiprop.md). Der einzige Zweck besteht darin, die Eigenschaften eines Profilabschnitts zu bearbeiten. Um einen **IProfSect-Zeiger** auf einen bestimmten Profilabschnitt abzurufen, rufen Clients und Dienstanbieter die folgenden Methoden auf. 
  
|||
|:-----|:-----|
|Clients können Folgendes aufrufen:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Dienstanbieter können Folgendes aufrufen:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clients oder Anbieter können Folgendes aufrufen:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Profile sind hierarchisch ähnlich wie MAPISVC organisiert. INF-Datei. Oben in der Hierarchie befinden sich Profilabschnitte, die für das Profil relevante Informationen enthalten. Die mittlere Ebene enthält Abschnitte, die Informationen zu einem bestimmten Nachrichtendienst enthalten, und die untere Ebene enthält Abschnitte, die Informationen zu einem der Dienstanbieter in einem Nachrichtendienst enthalten. 
  
Jedes Profil verfügt über mehrere erforderliche Eigenschaften, die in einem oder mehreren Abschnitten des Profils gespeichert sind. Beispielsweise weist jedes Profil die Eigenschaften **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) auf. Der Suchschlüssel eines Profils wird auf den in MAPIGUID definierten Wert festgelegt. H as MUID_PROFILE_INSTANCE and is always guaranteed to be unique among all profiles. Obwohl zwei Profile denselben Namen haben können, können sie nicht denselben Suchschlüssel haben. Suchschlüssel sollten als binäre Daten anstelle von Daten eines bestimmten Typs behandelt werden.
  
Nachrichtenspeicheranbieter müssen die **Eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ihres Nachrichtenspeichers in die Profilabschnitte für das Profil und für den Nachrichtenspeicheranbieter einschließen und diese Einträge synchronisiert lassen. Wenn ein Nachrichtenspeicher erstellt wird, legt der Anbieter **PR_DISPLAY_NAME** basierend auf dem in diesen Profilabschnitten gespeicherten Wert fest. 
  
Es gibt zwei wesentliche Unterschiede zwischen Profilabschnitten und anderen Objekten, die von **IMAPIProp** erben: 
  
- Profilabschnitte unterstützen keine Transaktionen.
    
- Profile sections do not support named properties, returning MAPI_E_NO_SUPPORT from their **IMAPIProp::GetIDsFromNames** and **IMAPIProp::GetNamesFromIDs** implementations. Weitere Informationen finden Sie unter [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Da Profilabschnitte transaktionen nicht unterstützen, werden alle Änderungen, die mit Aufrufen von **IMAPIProp::CopyProps,** **CopyTo** oder **SetProps** vorgenommen werden, sofort wirksam. Weitere Informationen finden Sie unter [IMAPIProp::CopyProps](imapiprop-copyprops.md). Clients und Dienstanbieter können die **IMAPIProp::SaveChanges-Methode** eines Profilabschnitts aufrufen, und sie ist erfolgreich, wirkt sich jedoch nicht auf die Profilabschnittsdaten aus. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Wenn Änderungen sofort auftreten, kann sich dies darauf auswirken, wie Dienstanbieter die Eigenschaftenblätter implementieren, die Clients zum Anzeigen von Profileigenschaften für Benutzer verwenden. Dienstanbieter, die möchten, dass Benutzer Änderungen verschieben oder rückgängig machen können, müssen ihre Eigenschaftenblätter mit Kopien von Profilabschnitten anstelle der tatsächlichen Abschnitte implementieren. Durch die Verwendung von Kopien können Benutzer Änderungen vornehmen und diese Änderungen später abbrechen, sodass die ursprünglichen Profilabschnitte unverändert bleiben. 
  
Die Reihenfolge, in der Informationen in einem Profil angezeigt werden, wirkt sich auf die Konfiguration von Ressourcen und Zuweisungen in einer Sitzung durch die MAPI aus. Die folgenden Zuweisungen sind von der Profilreihenfolge betroffen:
  
- Standardnachrichtenspeicher
    
- Persönliches Adressbuch
    
- Suchpfad des Standardnachrichtenspeichers
    
- Standardmäßiger Adressbuchsuchpfad
    
- Transportanbieterreihenfolge
    
MAPI legt fest, dass der Standardnachrichtenspeicher der erste Nachrichtenspeicher im Profil ist, für den das STATUS_DEFAULT_STORE-Flag in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt ist, was angibt, dass es sich um den Standardspeicher handelt. Clients können diese Einstellung überschreiben, indem **sie IMAPISession::SetDefaultStore** aufrufen. Weitere Informationen finden Sie unter [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI erstellt einen Transportauftrag für die Verarbeitung ausgehender und eingehender Nachrichten. Wenn sich mehr als ein Transportanbieter für eine Nachricht eines bestimmten Typs registriert hat, bestimmt mapi anhand dieser Reihenfolge, welcher Anbieter die Nachricht behandeln soll. MapI legt die Transportreihenfolge auf die Reihenfolge fest, in der die Transportanbieter dem Profil mit einer Ausnahme hinzugefügt wurden – die Transporte, die das STATUS_XP_PREFER_LAST Flag in ihrer **PR_RESOURCE_FLAGS** Eigenschaft festlegen, werden zuletzt in der Reihenfolge positioniert. Clients können die Transportreihenfolge festlegen, indem **sie IMsgServiceAdmin::MsgServiceTransportOrder** aufrufen. Weitere Informationen finden Sie unter [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Diese Richtlinien zum Sortieren von Dienstanbietern und Nachrichtendiensten können manchmal in Konflikt geraten. Wenn ein Konflikt vorliegt, sollte der Code den Konflikt lösen. Sie können das E-Mail-Systemsteuerungsprogramm verwenden, um ein profil zu überprüfen, das Sie erstellt haben, um festzustellen, ob die Anbieter wie erwartet konfiguriert wurden.
  

