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
  
Kann mit den Eigenschaften von profile section-Objekten verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Profile section-Objekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProfSect  <br/> |
|Zeigertyp:  <br/> |LPPROFSECT  <br/> |
|Transaktionsmodell:  <br/> |Nicht durchgeführten  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle hat keine eindeutigen Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **IProfSect** -Schnittstelle hat keine eigenen eindeutigen Methoden, aber Sie können die [IMAPIProp](imapipropiunknown.md) -Methoden des profile-Abschnitts aufrufen. Es gibt einige Unterschiede zwischen der **IProfSect** -Implementierung und anderen Implementierungen von **IMAPIProp**:
  
- **IProfSect** unterstützt kein Transaktionsmodell. 
    
- **IProfSect** unterstützt keine benannten Eigenschaften. 
    
- **IProfSect** reserviert den bezeichnerbereich 0x67F0 zu 0x67ff für sichere Eigenschaften. 
    
Nicht die Unterstützung eines Transaktionsmodells bewirkt, dass alle Änderungen, die an einem Profil Abschnitt vorgenommen wurden, nach Aufrufen der Methoden [IMAPIProp:: CopyProps](imapiprop-copyprops.md) und [IMAPIProp:: CopyTo](imapiprop-copyto.md) sofort stattfinden. Aufrufe der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode sind erfolgreich, speichern jedoch tatsächlich keine Änderungen. 
  
Um vor Änderungen zu schützen, die vorzeitig auftreten, müssen Dienstanbieter Kopien Ihrer Profilabschnitte erstellen, die Benutzern über Eigenschaftenblätter angezeigt werden. Die Eigenschaftenblätter sollten mit der Kopie statt mit dem Abschnitt Real profile funktionieren. Wenn der Benutzer auf die Schaltfläche **OK** klickt, um zu überprüfen, ob die Änderungen korrekt sind, können die Änderungen im Abschnitt Real Profile gespeichert werden. 
  
Gehen Sie folgendermaßen vor, um ein Eigenschaftenfenster mithilfe eines kopierten Profil Abschnitts zu implementieren:
  
1. Öffnen Sie den Profil Abschnitt, indem Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -oder [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) -Methode aufrufen. 
    
2. Rufen Sie die [CreateIProp](createiprop.md) -Funktion auf, um ein Property-Datenobjekt abzurufen, ein Objekt, das die **IPropData** -Schnittstelle unterstützt. 
    
3. Rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode des profile-Abschnitts auf, um die Eigenschaften zu kopieren, die im Eigenschaftenfenster aus dem Profil Abschnitt in das Datenobjekt der Eigenschaft angezeigt werden. 
    
4. Rufen Sie die [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode auf, um anzufordern, dass der Dienstanbieter ein Eigenschaftenfenster anzeigt, und übergeben Sie einen Zeiger auf das Datenobjekt der Eigenschaft im _lpConfigData_ -Parameter. 
    
5. Wenn der Benutzer Änderungen an den Konfigurationseigenschaften im Eigenschaftenblatt speichert, rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode auf, um die Eigenschaften aus dem Eigenschaftendaten Objekt zurück in den Profil Abschnitt zu kopieren. 
    
Profilabschnitte unterstützen im Gegensatz zu anderen Objekten keine benannten Eigenschaften. Die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) -Methoden geben MAPI_E_NO_SUPPORT zurück, wenn Sie für ein profile section-Objekt aufgerufen werden. Wenn Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode verwenden, um Eigenschaftenbezeichner im 0X8000-Wert festzulegen, wird der PT_ERROR-Eigenschaftentyp zurückgegeben. 
  
Profilabschnitte reservieren Sie den bezeichnerbereich 0x67F0 zu 0x67FF für sichere Eigenschaften. Dienstanbieter können diese Bereiche verwenden, um Kennwörter und andere anbieterspezifische Anmeldeinformationen zu speichern. Eigenschaften in diesem Bereichen werden nicht in der vollständigen Liste der Eigenschaften zurückgegeben, wenn NULL im _lpPropTag_ -Parameter der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode übergeben wird, noch werden Sie im _lppPropTagArray_ -Parameter des [ IMAPIProp::](imapiprop-getproplist.md) Getproplist-Methode. Sichere Eigenschaften müssen speziell durch ihre Bezeichner angefordert werden. 
  
MAPI liefert einen Profil Abschnitt mit der hartcodierten Konstanten MUID_PROFILE_INSTANCE als Bezeichner und **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) als einzelne Eigenschaft. MAPI stellt sicher, dass der Wert der **PR_SEARCH_KEY** -Eigenschaft für alle erstellten Profile eindeutig ist. Verwenden Sie **PR_SEARCH_KEY** anstelle von **PR_PROFILE_NAME** , wenn Eindeutigkeit wichtig ist, da ein gelöschtes Profil von einem anderen Profil mit demselben Namen gefolgt werden kann. 
  
Weitere Informationen zur Verwendung von Profil Abschnitten finden Sie unter [Verwalten von Profilen und Nachrichtendiensten](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

