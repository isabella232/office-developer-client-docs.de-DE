---
title: MAPI-Profile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340082"
---
# <a name="mapi-profiles"></a>MAPI-Profile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einem Profil werden Informationen zu Dienstanbietern und Nachrichtendiensten gespeichert, die auf einem Computer installiert sind. Für jede Sitzung wählt ein Client zur Anmeldezeit ein Profil aus, das die zu verwendenden Anbieter und Dienste beschreibt. Ein Client kann aus einer Sammlung von Profilen auswählen und, falls gewünscht, eines als Standard festlegen. Das Standardprofil ist das Profil, das automatisch ausgewählt wird, wenn ein Client eine Sitzung startet und kein Profil explizit angegeben hat.
  
Außerdem finden Sie in diesen Themen eine Diskussion über den Spitznamencache, der in einem binären Datenstrom gespeichert ist.
  
- [Cache für Spitznamen](nickname-cache.md)
    
- [Autocomplete Stream](autocomplete-stream.md)
    
- [Binärdatei-Analyse](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Profilabschnitte

Profile sind in Abschnitte unterteilt, auf die Clients und Dienstanbieter zugreifen können, um Profileigenschaften für Benutzer anzeigen oder Konfigurationsänderungen vornehmen zu können. Ein Profilabschnitt ist ein MAPI-Objekt, das die **IProfSect-Schnittstelle** implementiert, eine Schnittstelle, die von **IMAPIProp** ab leitet und keine zusätzlichen Methoden enthält. Weitere Informationen finden Sie unter [IProfSect : IMAPIProp](iprofsectimapiprop.md). Der einzige Zweck besteht in der Bearbeitung der Eigenschaften eines Profilabschnitts. Um einen **IProfSect-Zeiger** auf einen bestimmten Profilabschnitt abzurufen, rufen Clients und Dienstanbieter die folgenden Methoden auf. 
  
|||
|:-----|:-----|
|Clients können anrufen:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Dienstanbieter können anrufen:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clients oder Anbieter können anrufen:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Profile sind hierarchisch ähnlich wie der MAPISVC organisiert. INF-Datei. Am anfang der Hierarchie befinden sich Profilabschnitte, die informationen enthalten, die für das Profil relevant sind. Die mittlere Ebene enthält Abschnitte, die Informationen zu einem bestimmten Nachrichtendienst enthalten, und die untere Ebene enthält Abschnitte, die Informationen zu einem der Dienstanbieter in einem Nachrichtendienst enthalten. 
  
Jedes Profil verfügt über mehrere erforderliche Eigenschaften, die in einem oder mehreren Abschnitten des Profils gespeichert werden. Beispielsweise verfügt jedes Profil über die **eigenschaften PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Der Suchschlüssel eines Profils wird auf den in MAPIGUID definierten Wert festgelegt. H als MUID_PROFILE_INSTANCE und ist immer für alle Profile eindeutig. Obwohl zwei Profile denselben Namen haben können, können sie nicht denselben Suchschlüssel haben. Suchschlüssel sollten als Binärdaten anstelle von Daten eines bestimmten Typs behandelt werden.
  
Nachrichtenspeicheranbieter müssen die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft ihres Nachrichtenspeichers in die Profilabschnitte für das Profil und für ihren Nachrichtenspeicheranbieter einbehalten und diese Einträge synchronisieren. Wenn ein Nachrichtenspeicher erstellt wird, legt der **PR_DISPLAY_NAME** basierend auf dem in diesen Profilabschnitten gespeicherten Wert fest. 
  
Es gibt zwei wesentliche Unterschiede zwischen Profilabschnitten und anderen Objekten, die von **IMAPIProp erben:** 
  
- Profilabschnitte unterstützen keine Transaktionen.
    
- Profilabschnitte unterstützen keine benannten Eigenschaften und MAPI_E_NO_SUPPORT von ihren **IMAPIProp::GetIDsFromNames-** und **IMAPIProp::GetNamesFromIDs-Implementierungen** zurück. Weitere Informationen finden Sie unter [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Da Profilabschnitte keine Transaktionen unterstützen, werden alle Änderungen, die mit Aufrufen von **IMAPIProp::CopyProps,** **CopyTo** oder **SetProps** vorgenommen werden, sofort wirksam. Weitere Informationen finden Sie unter [IMAPIProp::CopyProps](imapiprop-copyprops.md). Clients und Dienstanbieter können die **IMAPIProp::SaveChanges-Methode** eines Profilabschnitts aufrufen, und sie wird erfolgreich ausgeführt, wirkt sich jedoch nicht auf die Profilabschnittsdaten aus. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Wenn Änderungen sofort vorgenommen werden, kann sich die Implementierung der Eigenschaftenblätter auswirken, die Clients zum Anzeigen von Profileigenschaften für Benutzer verwenden. Dienstanbieter, die möchten, dass Benutzer Änderungen verschieben oder rückgängig machen können, müssen ihre Eigenschaftenblätter mit Kopien von Profilabschnitten anstelle der tatsächlichen Abschnitte implementieren. Mithilfe von Kopien können Benutzer Änderungen vornehmen und diese Änderungen später abbrechen, ohne dass die ursprünglichen Profilabschnitte unverändert bleiben. 
  
Die Reihenfolge, in der Informationen in einem Profil angezeigt werden, wirkt sich darauf aus, wie MAPI Ressourcen konfiguriert und Zuordnungen in einer Sitzung vor nimmt. Die folgenden Zuordnungen sind von der Profilreihenfolge betroffen:
  
- Standardnachrichtenspeicher
    
- Persönliches Adressbuch
    
- Standardmäßiger Suchpfad des Nachrichtenspeichers
    
- Standardmäßiger Adressbuchsuchpfad
    
- Bestellung des Transportanbieters
    
MAPI legt fest, dass der Standardnachrichtenspeicher der erste Nachrichtenspeicher im Profil ist, für den das **STATUS_DEFAULT_STORE-Flag** in seiner PR_RESOURCE_FLAGS ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt ist, was angibt, dass es sich um den Standardspeicher geben kann. Clients können diese Einstellung überschreiben, indem **SIE IMAPISession::SetDefaultStore aufrufen.** Weitere Informationen finden Sie unter [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI erstellt eine Transportreihenfolge für die Verarbeitung ausgehender und eingehender Nachrichten. Wenn sich mehrere Transportanbieter für eine Nachricht eines bestimmten Typs registriert haben, verwendet MAPI diese Reihenfolge, um zu bestimmen, welcher Anbieter die Nachricht verarbeiten soll. MAPI legt die Transportreihenfolge auf die Reihenfolge fest, in der die Transportanbieter dem Profil mit einer Ausnahme hinzugefügt wurden: Die Transporte, die das STATUS_XP_PREFER_LAST-Flag in ihrer **PR_RESOURCE_FLAGS-Eigenschaft** festlegen, werden zuletzt in der Reihenfolge positioniert. Clients können die Transportreihenfolge festlegen, indem **sie IMsgServiceAdmin::MsgServiceTransportOrder aufrufen.** Weitere Informationen finden Sie unter [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Diese Richtlinien für die Bestellung von Dienstanbietern und Nachrichtendiensten können manchmal konfliktesprovideren. Wenn ein Konflikt vor liegt, sollte der Code den Konflikt lösen. Sie können das Programm für die Nachrichtensteuerung verwenden, um ein von Ihnen erstelltes Profil zu überprüfen, um zu ermitteln, ob die Anbieter wie erwartet konfiguriert wurden.
  

