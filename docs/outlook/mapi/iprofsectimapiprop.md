---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3046e8e71af92015ca5fd40e8a81c2afa8db89ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571570"
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
|Transaktionsmodell:  <br/> |Nicht übersetzt  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **IProfSect-Schnittstelle** verfügt über keine eigenen eindeutigen Methoden, Sie können jedoch die [IMAPIProp-Methoden](imapipropiunknown.md) des Profilabschnitts aufrufen. Es gibt einige Unterschiede zwischen der **IProfSect-Implementierung** und anderen Implementierungen von **IMAPIProp:**
  
- **IProfSect** unterstützt kein Transaktionsmodell. 
    
- **IProfSect** unterstützt keine benannten Eigenschaften. 
    
- **IProfSect** reserviert den Bezeichnerbereich 0x67F0, um sichere Eigenschaften zu 0x67ff. 
    
Wenn ein Transaktionsmodell nicht unterstützt wird, werden alle Änderungen, die an einem Profilabschnitt vorgenommen wurden, nachdem die Methoden [IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md) aufgerufen wurden, sofort ausgeführt. Aufrufe der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) sind erfolgreich, speichern aber keine Änderungen. 
  
Um vor vorzeitig auftretenden Änderungen geschützt zu werden, müssen Dienstanbieter Kopien ihrer Profilabschnitte erstellen, die Benutzern über Eigenschaftenblätter angezeigt werden. Die Eigenschaftenblätter sollten mit der Kopie und nicht mit dem echten Profilabschnitt funktionieren. Wenn der Benutzer auf die **SCHALTFLÄCHE "OK"** klickt, um zu überprüfen, ob die Änderungen korrekt sind, können die Änderungen im echten Profilabschnitt gespeichert werden. 
  
Gehen Sie folgendermaßen vor, um ein Eigenschaftenblatt mithilfe eines kopierten Profilabschnitts zu implementieren:
  
1. Öffnen Sie den Profilabschnitt, indem Sie die [IMAPISupport::OpenProfileSection-](imapisupport-openprofilesection.md) oder [IProviderAdmin::OpenProfileSection-Methode](iprovideradmin-openprofilesection.md) aufrufen. 
    
2. Rufen Sie die [CreateIProp-Funktion](createiprop.md) auf, um ein Eigenschaftsdatenobjekt abzurufen – ein Objekt, das die **IPropData-Schnittstelle** unterstützt. 
    
3. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) des Profilabschnitts auf, um die Eigenschaften, die auf dem Eigenschaftenblatt angezeigt werden, aus dem Profilabschnitt in das Eigenschaftendatenobjekt zu kopieren. 
    
4. Rufen Sie die [IMAPISupport::D oConfigPropSheet-Methode](imapisupport-doconfigpropsheet.md) auf, um anzufordern, dass der Dienstanbieter ein Eigenschaftenblatt anzeigt, und übergeben Sie einen Zeiger auf das Eigenschaftsdatenobjekt im _lpConfigData-Parameter._ 
    
5. Wenn der Benutzer Änderungen an Konfigurationseigenschaften im Eigenschaftenfenster speichert, rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) auf, um die Eigenschaften aus dem Eigenschaftendatenobjekt zurück in den Profilabschnitt zu kopieren. 
    
Profilabschnitte unterstützen im Gegensatz zu anderen Objekten keine benannten Eigenschaften. Die [IMAPIProp::GetIDsFromNames-](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs-Methoden](imapiprop-getnamesfromids.md) geben MAPI_E_NO_SUPPORT zurück, wenn sie für ein Profilabschnittsobjekt aufgerufen werden. Wenn Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) verwenden, um Eigenschaftsbezeichner im Bereich über 0x8000 festzulegen, wird der PT_ERROR Eigenschaftentyp zurückgegeben. 
  
Profilabschnitte reservieren den Bezeichnerbereich 0x67F0, um sichere Eigenschaften zu 0x67FF. Dienstanbieter können diesen Bereich zum Speichern von Kennwörtern und anderen anbieterspezifischen Anmeldeinformationen verwenden. Eigenschaften in diesem Bereich werden weder in der vollständigen Liste der Eigenschaften zurückgegeben, wenn NULL im  _lpPropTag-Parameter_ der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) übergeben wird, noch werden sie im  _lppPropTagArray-Parameter_ der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben. Sichere Eigenschaften müssen speziell von ihren Bezeichnern angefordert werden. 
  
MAPI stellt einen Profilabschnitt mit der hartcodierten Konstante MUID_PROFILE_INSTANCE als Bezeichner und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) als einzelne Eigenschaft dar. MAPI stellt sicher, dass der wert der **PR_SEARCH_KEY-Eigenschaft** unter allen erstellten Profilen eindeutig ist. Verwenden Sie **PR_SEARCH_KEY** anstelle **von PR_PROFILE_NAME,** wenn Eindeutigkeit wichtig ist, da es möglich ist, dass auf ein gelöschtes Profil ein anderes Profil mit demselben Namen folgt. 
  
Weitere Informationen zur Verwendung von Profilabschnitten finden Sie unter [Verwalten von Profilen und Nachrichtendiensten.](administering-profiles-and-message-services.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

