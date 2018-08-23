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
ms.openlocfilehash: b3850da2917dbf463590643b9e7ba8420f4ea219
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576057"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Konvertiert einen Nachrichtenspeicher interne Eintrags-ID auf einen Eintrag Bezeichner MAPI-Standardformat.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpOrigEntry_ verwiesen. 
    
 _lpOrigEntry_
  
> [in] Ein Zeiger auf die private Eintrags-ID für den Nachrichtenspeicher.
    
 _lpcbWrappedEntry_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppWrappedEntry_ verwiesen. 
    
 _lppWrappedEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintrag gepackten Bezeichner.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eintrags-ID wurde erfolgreich umbrochen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::WrapStoreEntryID** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter verwenden **WrapStoreEntryID** MAPI einen Eintrag Bezeichner für einen Nachrichtenspeicher zu erstellen, der den Speicher interne Eintrags-ID umbrochen wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn ein Client den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufruft, um die **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))-Eigenschaft und Nachrichtenspeichers abzurufen verwendet eine Eintrags-ID in einem privaten Format, rufen Sie **WrapStoreEntryID **und die Eintrags-ID auf das durch den Parameter _LppWrappedEntry_ zurückzukehren. 
  
Aufrufe der Methoden [IMSProvider::Logon](imsprovider-logon.md) und [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) abrufen immer private Eintrags-ID für den Speicher. Die gepackten Version wird nur zwischen Clientanwendungen und MAPI verwendet. 
  
Freigeben des Speichers für die Eintrags-ID mithilfe der Funktion [MAPIFreeBuffer](mapifreebuffer.md) Sie abschließend mithilfe der Eintrags-ID auf durch den Parameter _LppWrappedEntry_ zeigt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

