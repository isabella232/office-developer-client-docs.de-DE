---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 914b1fb1d9cae010b3ac59ad566705d1beae6eab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567402"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert den internen Eintragsbezeichner eines Nachrichtenspeichers in einen Eintragsbezeichner im MAPI-Standardformat.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Parameter

 _cbOrigEntry_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _parameter lpOrigEntry_ verweist. 
    
 _lpOrigEntry_
  
> [in] Ein Zeiger auf den privaten Eintragsbezeichner für den Nachrichtenspeicher.
    
 _lpcbWrappedEntry_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppWrappedEntry"_ verweist. 
    
 _lppWrappedEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den umschlossenen Eintragsbezeichner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintragsbezeichner wurde erfolgreich umbrochen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::WrapStoreEntryID-Methode** ist für alle Dienstanbieter-Supportobjekte implementiert. Dienstanbieter verwenden **WrapStoreEntryID,** damit MAPI einen Eintragsbezeichner für einen Nachrichtenspeicher generiert, der den internen Eintragsbezeichner des Speichers umschließt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) Ihres Nachrichtenspeichers aufruft, um seine **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) -Eigenschaft abzurufen, und Ihr Nachrichtenspeicher einen Eintragsbezeichner in einem privaten Format verwendet, rufen Sie **WrapStoreEntryID** auf und geben Sie den Eintragsbezeichner zurück, auf den der  _lppWrappedEntry-Parameter_ verweist. 
  
Aufrufe der Methoden [IMSProvider::Logon](imsprovider-logon.md) und [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) rufen immer den privaten Eintragsbezeichner des Speichers ab. Die umschlossene Version wird nur zwischen Clientanwendungen und MAPI verwendet. 
  
Geben Sie den Speicher für den Eintragsbezeichner frei, auf den der  _Parameter "lppWrappedEntry"_ verweist, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) verwenden, wenn Sie den Eintragsbezeichner nicht mehr verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

