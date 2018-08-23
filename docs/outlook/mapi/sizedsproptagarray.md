---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573621"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropTagArray](sproptagarray.md) -Struktur, die eine angegebene Anzahl von Eigenschaftentags enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parameter

__ctag_
  
> Anzahl der Eigenschaftentags in die neue Struktur enthalten sein.
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das Makro **SizedSPropTagArray** , um ein Array Tag-Eigenschaft mit expliziten Grenzen zu erstellen. 
  
Um die neue Struktur verwenden, die als Zeiger auf eine **SPropTagArray** -Struktur aus dem Makro **SizedSPropTagArray** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Siehe auch

- [SPropTagArray](sproptagarray.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

