---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61a66d406ba22722e12cbcb8f1ab9d1ae0cc8362
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564232"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierungen zurück, um weiteren Zugriff zu ermöglichen.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Containers, Messagingbenutzers oder der Verteilerliste.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das geöffnete Objekt verwendet werden soll. Wenn NULL übergeben wird, wird der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben. Bei Containern ist die Standardschnittstelle [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList : IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser : IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den für den Benutzer maximal zulässigen Netzwerkberechtigungen und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützte Berechtigungen verfügt, sollte das Objekt mit schreibgeschützter Berechtigung geöffnet werden.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht es der **OpenEntry-Methode,** erfolgreich zurückzugeben, möglicherweise bevor der aufrufende Client vollständig auf das Objekt zugegriffen hat. Wenn nicht auf das Objekt zugegriffen wird, kann ein nachfolgender Objektaufruf einen Fehler auslösen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschütztem Zugriff geöffnet, und Clients sollten nicht davon ausgehen, dass die Lese-/Schreibberechtigung erteilt wurde.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="remarks"></a>HinwBemerkungeneise

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder verfügt der Benutzer über unzureichende Berechtigungen zum Öffnen des Objekts, oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibberechtigung zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Der durch  _lpEntryID_ angegebene Eintragsbezeichner stellt kein Objekt dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Eintragsbezeichner im  _LpEntryID-Parameter_ weist kein vom Adressbuchanbieter erkanntes Format auf. 
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI ruft die **OpenEntry-Methode** auf, um einen Container, einen Messagingbenutzer oder eine Verteilerliste zu öffnen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Bevor mapi Ihre **OpenEntry-Methode** aufruft, wird ermittelt, ob der Eintragsbezeichner im  _lpEntryID-Parameter_ Ihnen gehört und nicht einem anderen Anbieter. Die MAPI vergleicht dazu die [MAPIUID-Struktur](mapiuid.md) im Eintragsbezeichner mit der **MAPIUID,** die Sie registriert haben, indem Sie die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) beim Start aufrufen. 
  
Öffnen Sie das Objekt schreibgeschützt, es sei denn, das flag MAPI_MODIFY oder MAPI_BEST_ACCESS ist im  _ulFlags-Parameter_ festgelegt. Wenn Sie keine Änderung für das angeforderte Objekt zulassen, öffnen Sie das Objekt überhaupt nicht, und geben Sie MAPI_E_NO_ACCESS zurück. 
  
Wenn MAPI NULL für  _lpEntryID_ übergibt, öffnen Sie den Stammcontainer in Ihrer Containerhierarchie.
  
Das Objekt, das Sie öffnen möchten, ist möglicherweise ein Objekt, das von einem anderen Anbieter kopiert wurde. In diesem Fall wird die **Eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt. Wenn das Objekt diese Eigenschaft unterstützt, rufen Sie die [IMAPISupport::OpenTemplateID-Methode](imapisupport-opentemplateid.md) auf, um eine Bindung an Code für diesen Eintrag im fremdanbieter durchzuführen, und übergeben **Sie PR_TEMPLATEID** im _LpTemplateID-Parameter_ und 0 im _ulTemplateFlags-Parameter._ **IMAPISupport::OpenTemplateID** übergibt diese Informationen in einem Aufruf an die [IABLogon::OpenTemplateID-Methode](iablogon-opentemplateid.md) des fremden Anbieters an den fremdanbieter. Wenn **IMAPISupport::OpenTemplateID** einen Fehler auslöst, in der Regel, weil der fremde Anbieter nicht verfügbar oder nicht im Profil enthalten ist, versuchen Sie, den ungebundenen Eintrag als schreibgeschützt zu behandeln. Weitere Informationen zum Öffnen von Fremdadressbucheinträgen finden Sie unter ["Hostadressbuchanbieter"](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon : IUnknown](iablogoniunknown.md)

