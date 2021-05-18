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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406598"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Funktioniert mit den Eigenschaften von Profilabschnittsobjekten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Profilabschnittsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProfSect  <br/> |
|Zeigertyp:  <br/> |LPPROFSECT  <br/> |
|Transaktionsmodell:  <br/> |Nichttransaktioniert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **IProfSect-Schnittstelle** verfügt nicht über eigene eindeutige Methoden, Sie können jedoch die [IMAPIProp-Methoden](imapipropiunknown.md) des Profilabschnitts aufrufen. Es gibt einige Unterschiede zwischen der **IProfSect-Implementierung** und anderen Implementierungen von **IMAPIProp:**
  
- **IProfSect** unterstützt kein Transaktionsmodell. 
    
- **IProfSect** unterstützt keine benannten Eigenschaften. 
    
- **IProfSect** behält den Bezeichnerbereich 0x67F0, 0x67ff sichere Eigenschaften zu verwenden. 
    
Die Nichtunterstützen eines Transaktionsmodells bedeutet, dass alle Änderungen, die an einem Profilabschnitt nach Aufrufen der [Methoden IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md) vorgenommen wurden, sofort erfolgen. Aufrufe der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) sind erfolgreich, speichern jedoch keine Änderungen. 
  
Um vor Änderungen geschützt zu werden, die vorzeitig auftreten, müssen Dienstanbieter Kopien ihrer Profilabschnitte erstellen, die Benutzern über Eigenschaftenblätter angezeigt werden. Die Eigenschaftenblätter sollten mit der Kopie anstelle des echten Profilabschnitts verwendet werden. Wenn der Benutzer auf die **Schaltfläche OK** klickt, um zu überprüfen, ob die Änderungen korrekt sind, können die Änderungen im Abschnitt "Echtes Profil" gespeichert werden. 
  
Verwenden Sie das folgende Verfahren, um ein Eigenschaftenblatt mithilfe eines kopierten Profilabschnitts zu implementieren:
  
1. Öffnen Sie den Profilabschnitt, indem Sie die [IMAPISupport::OpenProfileSection-](imapisupport-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection-Methode](iprovideradmin-openprofilesection.md) aufrufen. 
    
2. Rufen Sie die [CreateIProp-Funktion](createiprop.md) auf, um ein Eigenschaftsdatenobjekt abzurufen – ein Objekt, das die **IPropData-Schnittstelle** unterstützt. 
    
3. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) des Profilabschnitts auf, um die Eigenschaften zu kopieren, die im Eigenschaftenblatt aus dem Profilabschnitt in das Eigenschaftsdatenobjekt angezeigt werden. 
    
4. Rufen Sie die [IMAPISupport::D oConfigPropSheet-Methode](imapisupport-doconfigpropsheet.md) auf, um anzuforderen, dass der Dienstanbieter ein Eigenschaftenblatt anfordert, und übergeben Sie einen Zeiger an das Eigenschaftsdatenobjekt im _lpConfigData-Parameter._ 
    
5. Wenn der Benutzer Änderungen an Konfigurationseigenschaften im Eigenschaftenblatt speichert, rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) auf, um die Eigenschaften aus dem Eigenschaftendatenobjekt zurück in den Profilabschnitt zu kopieren. 
    
Profilabschnitte unterstützen im Gegensatz zu anderen Objekten keine benannten Eigenschaften. Die [Methoden IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) geben MAPI_E_NO_SUPPORT zurück, wenn sie für ein Profilabschnittsobjekt aufgerufen werden. Wenn Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) zum Festlegen von Eigenschaftsbezeichnern im Bereich oberhalb von 0x8000 verwenden, wird der PT_ERROR-Eigenschaftstyp zurückgegeben. 
  
Profilabschnitte behalten den Bezeichnerbereich 0x67F0, 0x67FF sichere Eigenschaften zu verwenden. Dienstanbieter können diesen Bereich verwenden, um Kennwörter und andere anbieterspezifische Anmeldeinformationen zu speichern. Eigenschaften in diesem Bereich werden nicht in der vollständigen Liste der Eigenschaften zurückgegeben, wenn NULL im  _lpPropTag-Parameter_ der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) übergeben wird, noch werden sie im  _lppPropTagArray-Parameter_ der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben. Sichere Eigenschaften müssen speziell von ihren Bezeichnern angefordert werden. 
  
MAPI bietet einen Profilabschnitt mit der hart codierten Konstante MUID_PROFILE_INSTANCE als Bezeichner und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) als einzelne Eigenschaft. MAPI stellt sicher, **dass PR_SEARCH_KEY** Eigenschaftswert unter allen erstellten Profilen eindeutig ist. Verwenden **PR_SEARCH_KEY** anstelle **PR_PROFILE_NAME,** wenn die Eindeutigkeit wichtig ist, da es möglich ist, dass einem gelöschten Profil ein anderes Profil mit demselben Namen folgt. 
  
Weitere Informationen zur Verwendung von Profilabschnitten finden Sie unter [Administering Profiles and Message Services](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

