---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c0653caec5f3cac531206e1bb9c4330cac5f3133
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792781"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Betrifft**: Outlook 
  
Funktioniert mit den Eigenschaften des Profils Section-Objekten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Profil Section-Objekten  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProfSect  <br/> |
|Zeigertyp:  <br/> |LPPROFSECT  <br/> |
|Transaktionsmodell:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle hat keinen eindeutigen Methoden.
  
|**Erforderliche Eigenschaften**|**Zugriff**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die Schnittstelle **IProfSect** hat keinen eindeutigen Methoden eigenen, aber Sie können das Profil des Abschnitts [IMAPIProp](imapipropiunknown.md) Methoden aufrufen. Es gibt einige Unterschiede zwischen den **IProfSect** Implementierung und Implementierungen **IMAPIProp**:
  
- Ein Transaktionsmodell unterstützt **IProfSect** nicht. 
    
- **IProfSect** unterstützt keine benannte Eigenschaften. 
    
- **IProfSect** reserviert Bezeichner Bereich 0x67F0 zu 0x67ff sicheren Eigenschaften. 
    
Nicht unterstützt, eine Transaktionsmodell bedeutet, dass alle Änderungen vorgenommen wurden, die ein Profil im folgenden Abschnitt zu den [IMAPIProp::CopyProps](imapiprop-copyprops.md) aufruft und [IMAPIProp::CopyTo](imapiprop-copyto.md) Methoden unmittelbar ausgeführt. Aufrufe der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode erfolgreich ausgeführt, aber nicht tatsächlich Änderungen speichern. 
  
Um von Änderungen geschützt werden, die vorzeitig auftreten, müssen Dienstanbieter Kopien der Abschnitte, deren Profil erstellen, die Benutzer über Eigenschaftenseiten angezeigt werden. Die Eigenschaftenseiten sollte mit der Kopie, anstatt Abschnitts realen Profile funktionieren. Wenn der Benutzer klickt auf die Schaltfläche **OK** , um sicherzustellen, dass die Änderungen korrekt sind, können die Änderungen in den Profilabschnitt realen gespeichert werden. 
  
Zur Implementierung von einem Eigenschaftenfenster unter Verwendung eines Abschnitts kopierte Profil verwenden Sie die folgende Schritte aus:
  
1. Öffnen Sie den Profilabschnitt, durch die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode aufrufen. 
    
2. Rufen Sie die [CreateIProp](createiprop.md) -Funktion zum Abrufen einer Eigenschaft Datenobjekt – ein Objekt, das die **IPropData** -Schnittstelle unterstützt. 
    
3. Rufen Sie den Profilabschnitt [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode zum Kopieren Sie der Eigenschaften, die auf der Eigenschaftenseite auf die Daten Property-Objekt aus dem Profilabschnitt angezeigt wird. 
    
4. Rufen Sie die [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) -Methode, um anzufordern, dass der Dienstanbieter Anzeigen eines Eigenschaftenblatts und einen Zeiger auf das Eigenschaftenobjekt Daten im _LpConfigData_ -Parameter übergeben. 
    
5. Wenn der Benutzer Änderungen auf die Konfigurationseigenschaften im Eigenschaftenfenster speichert, rufen Sie die [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um die Eigenschaften aus der Eigenschaftenobjekt Daten zurück in den Profilabschnitt kopieren. 
    
Profil Abschnitte, im Gegensatz zu anderen Objekten unterstützen keine benannte Eigenschaften. Die Methoden [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) zurück MAPI_E_NO_SUPPORT, wenn sie auf ein Profil Section-Objekt aufgerufen werden. Wenn Sie im Bereich über 0 x 8000 Eigenschaftenbezeichner festlegen die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode verwenden, werden der Typ der PT_ERROR-Eigenschaft zurückgegeben. 
  
Profil Abschnitte reservieren Bezeichner Bereich 0x67F0 zu 0x67FF sicheren Eigenschaften. Dienstanbieter können diesen Bereich zum Speichern von Kennwörtern und anderen anbieterspezifische Anmeldeinformationen verwenden. Eigenschaften in diesem Bereich werden nicht in die vollständige Liste der Eigenschaften zurückgegeben, wenn NULL im _LpPropTag_ -Parameter der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode übergeben wird, noch werden sie in der _LppPropTagArray_ -Parameter, der die [zurückgegeben IMAPIProp::GetPropList](imapiprop-getproplist.md) Methode. Schützen von Eigenschaften müssen insbesondere anhand der dazugehörigen Bezeichner angefordert werden. 
  
MAPI stellt einen Profilabschnitt mit hartcodierten Konstante MUID_PROFILE_INSTANCE als Bezeichner und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) als ihre einzige Eigenschaft bereit. MAPI wird sichergestellt, dass der Wert der **PR_SEARCH_KEY** -Eigenschaft für alle erstellten Profile eindeutig sein wird. Verwenden Sie **PR_SEARCH_KEY** anstelle **PR_PROFILE_NAME** , wenn die Eindeutigkeit wichtig ist, da es zu einem anderen Profil mit dem gleichen Namen folgen gelöschten Profil möglich ist. 
  
Weitere Informationen zur Verwendung von Profil Abschnitten finden Sie unter [Verwalten von Benutzerprofilen und Message-Dienste](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

