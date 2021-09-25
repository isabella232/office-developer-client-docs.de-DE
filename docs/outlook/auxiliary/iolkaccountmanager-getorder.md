---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Ruft die Reihenfolge der angegebenen Kontenkategorie ab.
ms.openlocfilehash: 3a680e7a40197a3edf22e78d4e35ac981802a193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617111"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Ruft die Reihenfolge der angegebenen Kontenkategorie ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Parameter

_pclsidCategory_
  
> [in] Die Kategorieklassen-ID, für die die Bestellung abgerufen werden soll. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out] Die Anzahl der Konten. 
    
_prgAccts_
  
> [out] Ein Zeiger auf ein Array von Konten.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode weist der Aufrufer nur einen Arrayzeiger  *prgAccts*  zu, aber keinen Speicher für das Array, auf das  *prgAccts*  zeigt. Nachdem diese Methode zurückgegeben wurde, muss der Aufrufer [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) verwenden, um den für  *prgAccts reservierten*  Speicher freizugeben. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

