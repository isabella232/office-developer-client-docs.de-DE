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
  
Konvertiert die interne Eintrags-ID eines Nachrichtenspeichers in eine Eintrags-ID im MAPI-Standardformat.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpOrigEntry_ -Parameter verwiesen wird. 
    
 _lpOrigEntry_
  
> in Ein Zeiger auf die ID des privaten Eintrags für den Nachrichtenspeicher.
    
 _lpcbWrappedEntry_
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppWrappedEntry_ -Parameter verwiesen wird. 
    
 _lppWrappedEntry_
  
> Out Ein Zeiger auf einen Zeiger auf den eingebundenen Eintragsbezeichner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eintrags-ID wurde erfolgreich umbrochen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: WrapStoreEntryID** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter verwenden **WrapStoreEntryID** , um MAPI eine Eintrags-ID für einen Nachrichtenspeicher zu generieren, der die interne Eintrags-ID des Speichers umschließt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers zum Abrufen seiner **PR_STORE_ENTRYID** ([pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))-Eigenschaft aufruft und Ihr Nachrichtenspeicher eine Eintrags-ID in einem privaten Format verwendet, rufen Sie WrapStoreEntryID auf. ** **, und geben Sie die Eintrags-ID zurück, auf die durch den _lppWrappedEntry_ -Parameter verwiesen wird. 
  
Aufrufe der [IMSProvider:: Login](imsprovider-logon.md) -und [IMSLogon:: CompareEntryIDs](imslogon-compareentryids.md) -Methoden rufen immer den privaten Eintragsbezeichner des Speichers ab; die Wrapped-Version wird nur zwischen Clientanwendungen und MAPI verwendet. 
  
Freigeben des Speichers für die Eintrags-ID, auf die durch den _lppWrappedEntry_ -Parameter verwiesen wird, mithilfe der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, wenn Sie die Eintrags-ID nicht mehr verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

