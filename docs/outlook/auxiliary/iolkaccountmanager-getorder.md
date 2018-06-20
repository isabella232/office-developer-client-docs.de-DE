---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Ruft die Reihenfolge der angegebenen Kategorie von Konten.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791099"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Ruft die Reihenfolge der angegebenen Kategorie von Konten.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Parameter

_pclsidCategory_
  
> [in] Die Kategorie Klassen-ID für die die Reihenfolge abgerufen. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out] Die Anzahl der Konten. 
    
_prgAccts_
  
> [out] Ein Zeiger auf ein Array von Konten.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode weist der Anrufer nur ein Array Zeiger *PrgAccts* jedoch kein Speicher für Arrays, an den *PrgAccts* zeigt. Nachdem diese Methode zurückgegeben wird, muss der Aufrufer [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) verwenden, um Arbeitsspeicher für *PrgAccts* freizugeben. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

