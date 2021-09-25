---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Ruft das nächste Konto im Enumerator ab.
ms.openlocfilehash: 7d49faa7bb6be4b0ee76eb36f47a6971dc5b1ad9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557141"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Ruft das nächste Konto im Enumerator ab.
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parameter

_ppunk_
  
> [in] Ein Zeiger auf eine **IUnknown-Schnittstelle,** die der Client abfragen kann, um eine [IOlkAccount-Schnittstelle](iolkaccount.md) abzurufen. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|S_FALSE  <br/> |Der Enumerator hat das Ende erreicht.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die durch *Ppunk* angegebene Schnittstelle erbt von **IUnknown.** Der Client kann diese Schnittstelle (mit **IUnknown::QueryInterface)** abfragen, um einen Zeiger auf eine **IOlkAccount-Schnittstelle** abzurufen und Informationen für dieses Konto abzurufen oder festzulegen. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

