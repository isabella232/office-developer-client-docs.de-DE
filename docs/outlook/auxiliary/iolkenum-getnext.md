---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Ruft das nächste Konto in den Enumerator ab.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791130"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Ruft das nächste Konto in den Enumerator ab.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parameter

_ppunk_
  
> [in] Ein Zeiger auf eine **IUnknown** -Schnittstelle, die der Client Abfragen kann, um eine [IOlkAccount](iolkaccount.md) -Schnittstelle zu erhalten. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|S_FALSE  <br/> |Das Ende wurde der Enumerator erreicht werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die angegebene *Ppunk* Schnittstelle erbt von **IUnknown**. Der Client kann diese Schnittstelle (Verwendung von **QueryInterface**) Abfragen, um einen Zeiger auf eine Schnittstelle **IOlkAccount** erhalten und Abrufen oder Festlegen von Informationen für dieses Konto. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

