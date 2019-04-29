---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Ruft die Reihenfolge der angegebenen Kategorie von Konten ab.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424623"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Ruft die Reihenfolge der angegebenen Kategorie von Konten ab.
  
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
  
> in Die Kategorie-Klassen-ID, für die die Bestellung abgerufen werden soll. Der Wert muss eine der folgenden sein:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  Out Die Anzahl der Konten. 
    
_prgAccts_
  
> Out Ein Zeiger auf ein Array von Konten.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Argument ist ungültig.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode reserviert der Aufrufer nur einen Array Zeiger *prgAccts* , aber kein Speicher für das Array, an dem *prgAccts* Punkt. Nach der Rückgabe dieser Methode muss der Aufrufer [IOlkAccountManager:: freier Arbeitsspeicher](iolkaccountmanager-freememory.md) verwenden, um den für *prgAccts* reservierten Arbeitsspeicher freizugeben. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

