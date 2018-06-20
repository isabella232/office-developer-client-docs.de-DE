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
ms.openlocfilehash: 7f241fde8aedeae9debc66f728ee21c1c6bed6fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793040"
---
# <a name="mapi-profiles"></a>MAPI-Profile

  
  
**Betrifft**: Outlook 
  
Ein Profil speichert Informationen zu Dienstanbietern und Message-Dienste, die auf einem Computer installiert sind. Für jede Sitzung wählt ein Client bei der Anmeldung ein Profil, das den Anbieter und die Dienste zu verwendende beschreibt. Ein Client kann eine als Standard auswählen aus einer Auflistung von Benutzerprofilen und, bei Bedarf einrichten. Das Standardprofil ist das Profil, das automatisch ausgewählt wird, wenn ein Client eine Sitzung startet und ein Profil nicht explizit angegeben wurde.
  
Auch in diesen Themen finden eine Erläuterung der Nickname-Cache Sie die in einem binären Stream gespeichert ist.
  
- [Nickname-cache](nickname-cache.md)
    
- [AutoVervollständigen-Stream](autocomplete-stream.md)
    
- [Analysieren der Binärdatei](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Profil Abschnitte

Profile sind in Abschnitten dieser Clients unterteilt und Dienstanbieter für Benutzer Profileigenschaften anzeigen oder Ändern der Konfiguration zugreifen. Ein Profilabschnitt ist ein MAPI-Objekt, das die **IProfSect** -Schnittstelle implementiert wird, eine Schnittstelle, die von **IMAPIProp** abgeleitet und verfügt über keine zusätzlichen Methoden. Weitere Informationen finden Sie unter [IProfSect: IMAPIProp](iprofsectimapiprop.md). Der Zweck ist die Eigenschaften eines Abschnitts Profil bearbeiten. Rufen Sie zum Abrufen eines **IProfSect** Zeigers auf einem bestimmten Profilabschnitt Clients und -Dienstanbieter die folgenden Methoden. 
  
|||
|:-----|:-----|
|Clients können aufrufen:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Dienstanbieter aufrufen können:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clients oder Anbieter können anrufen:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Profile sind wie die Datei MAPISVC hierarchisch viel angeordnet. INF-Datei. Klicken Sie oben in der Hierarchie sind Profil Abschnitte, die Informationen im Zusammenhang mit dem Profil enthalten. Die mittlere Ebene enthält Abschnitte, die Informationen zu einem Dienst bestimmte Nachricht enthalten, und die untere Ebene enthält Abschnitte, die Informationen über einen-Dienstanbieter in einem Nachrichtendienst enthalten. 
  
Jedes Profil hat mehrere erforderliche Eigenschaften, die in eine oder mehrere der in den Abschnitten des Profils gespeichert sind. Jedes Profil verfügt beispielsweise über die **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaften. Ein Profil suchen-Taste wird auf die in MAPIGUID definierten Wert festgelegt. H als MUID_PROFILE_INSTANCE und ist immer gewährleistet, dass für alle Profile eindeutig sein. Obwohl zwei Profile denselben Namen haben können, können sie nicht den gleichen Suche Schlüssel haben. Suche Schlüssel sollte als Binärdaten anstelle von Daten, die keinen bestimmten Typ behandelt werden.
  
Nachricht Anbieter sind erforderlich, fügen Sie ihren Nachrichtenspeicher **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in den Abschnitten Profil für das Profil und für ihre Nachricht Speicheranbieter und diese Einträge synchronisiert halten. Wenn ein Nachrichtenspeicher erstellt wird, wird der Anbieter **PR_DISPLAY_NAME** basierend auf dem Wert in den folgenden Abschnitten Profil gespeichert. 
  
Es gibt zwei Hauptunterschiede zwischen Profil Abschnitte und andere Objekte, die von **IMAPIProp**erben: 
  
- Profil Abschnitte unterstützen keine Transaktionen.
    
- Profil Abschnitte unterstützen keine benannte Eigenschaften zurückgeben MAPI_E_NO_SUPPORT aus ihrer **IMAPIProp::GetIDsFromNames** und **IMAPIProp::GetNamesFromIDs** Implementierungen. Weitere Informationen finden Sie unter [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Profil Abschnitte Transaktionen mit Aufrufen **IMAPIProp::CopyProps**, vorgenommenen Änderungen bieten keine Unterstützung **CopyTo**oder **SetProps** sofort wirksam. Weitere Informationen finden Sie unter [IMAPIProp::CopyProps](imapiprop-copyprops.md). Clients und Dienstanbieter können einem Profilabschnitt **IMAPIProp::SaveChanges** -Methode aufrufen und es wird erfolgreich ausgeführt, aber es hat keinen Einfluss auf die im Abschnitt Profildaten. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Ändert sich sofort durchgeführt haben, kann die wie Dienstanbieter Eigenschaftenblätter implementieren, die Clients verwenden, die Benutzern Profileigenschaften angezeigt beeinträchtigen. Dienstanbieter, die Benutzern möglich Zurückstellen oder rückgängig machen möchten, müssen ihre Eigenschaftenseiten mit Kopien von Abschnitten anstelle der echten Abschnitte Profil implementieren. Benutzer können mithilfe von Kopien Änderungen vornehmen und später diese Änderungen Abbrechen verlassen die ursprünglichen Profil Abschnitte unverändert. 
  
Die Reihenfolge, in der Informationen in einem Profil angezeigt, wirkt sich auf wie MAPI Ressourcen konfiguriert, und macht Zuordnungen in einer Sitzung. Die folgenden Zuordnungen unterliegen Profil Reihenfolge:
  
- Standard-Informationsspeicher
    
- Persönliches Adressbuch
    
- Nachricht Store Suchpfad Standard
    
- Default Address Book Suchpfad
    
- Die Reihenfolge der Transport-Anbieter
    
MAPI legt den Standard-Nachrichtenspeicher auf dem ersten Nachrichtenspeicher im Profil ist, ist das STATUS_DEFAULT_STORE-Flag festlegen in dessen **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft, die angibt, dass sie die Standard-Informationsspeichers werden kann. Clients können diese Einstellung außer Kraft setzen, indem Sie **IMAPISession::SetDefaultStore**aufrufen. Weitere Informationen finden Sie unter [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI erstellt einen Transport-Auftrag für die Verarbeitung von eingehender und ausgehender Nachrichten. Wenn mehr als eine Adressbuchhierarchie für eine Nachricht eines bestimmten Typs registriert hat, verwendet MAPI angegebenen Reihenfolge um zu bestimmen, welcher Anbieter die Nachricht behandelt werden sollen. MAPI wird die Transport die Reihenfolge, in der die sind das Transportprotokoll Anbieter auf das Profil mit einer Ausnahme – die Transporten hinzugefügt wurden, die das Flag STATUS_XP_PREFER_LAST in ihrer **PR_RESOURCE_FLAGS** -Eigenschaft festgelegt in der Reihenfolge zuletzt positioniert, werden. Clients können die Reihenfolge der Transport durch Aufrufen von **IMsgServiceAdmin::MsgServiceTransportOrder**festgelegt. Weitere Informationen finden Sie unter [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Diese Richtlinien für die Sortierung Dienstanbieter und Message-Dienste können manchmal Konflikte auftreten. Wenn ein Konflikt vorliegt, sollte Ihr Code den Konflikt zu lösen. Die Mail-Systemsteuerung Anwendung können Sie um ein Profil zu prüfen, die Sie erstellt haben, um zu bestimmen, ob der Anbieter erwartungsgemäß konfiguriert wurden.
  

