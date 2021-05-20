---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430448"
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpOrigEntry-Parameter_ verweist. 
    
 _lpOrigEntry_
  
> [in] Ein Zeiger auf den privaten Eintragsbezeichner für den Nachrichtenspeicher.
    
 _lpcbWrappedEntry_
  
> [out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppWrappedEntry-Parameter_ verweist. 
    
 _lppWrappedEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf die umschlossene Eintrags-ID.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintragsbezeichner wurde erfolgreich umschlossen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::WrapStoreEntryID-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter verwenden **WrapStoreEntryID,** damit MAPI einen Eintragsbezeichner für einen Nachrichtenspeicher generiert, der den internen Eintragsbezeichner des Informationsspeichers umschließt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) ihres Nachrichtenspeichers aufruft, um seine **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))-Eigenschaft abzurufen, und ihr Nachrichtenspeicher einen Eintragsbezeichner in einem privaten Format verwendet, rufen Sie **WrapStoreEntryID** auf, und geben Sie den Eintragsbezeichner zurück, auf den der  _lppWrappedEntry-Parameter_ verweist. 
  
Aufrufe der [Methoden IMSProvider::Logon](imsprovider-logon.md) und [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) rufen immer den privaten Eintragsbezeichner des Speichers ab. die umschlossene Version wird nur zwischen Clientanwendungen und MAPI verwendet. 
  
Gibt den Arbeitsspeicher für den Eintragsbezeichner frei, auf den der  _lppWrappedEntry-Parameter_ verweist, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) verwenden, wenn Sie mit der Eingabe-ID fertig sind. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

