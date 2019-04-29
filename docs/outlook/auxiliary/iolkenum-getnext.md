---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Ruft das nächste Konto im Enumerator ab.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405989"
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

_ppUnk_
  
> in Ein Zeiger auf eine **IUnknown** -Schnittstelle, die der Client Abfragen kann, um eine [IOlkAccount](iolkaccount.md) -Schnittstelle abzurufen. 
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|S_FALSE  <br/> |Der Enumerator hat das Ende erreicht.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die von *ppUnk* angegebene Schnittstelle erbt von **IUnknown**. Der Client kann diese Schnittstelle Abfragen (mithilfe von **IUnknown:: QueryInterface**), um einen Zeiger auf eine **IOlkAccount** -Schnittstelle abzurufen und Informationen für dieses Konto abzurufen oder festzulegen. 
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Account Management API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

