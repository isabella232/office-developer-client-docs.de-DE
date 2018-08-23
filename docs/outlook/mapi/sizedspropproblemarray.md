---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594614"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropProblemArray](spropproblemarray.md) -Struktur, die eine angegebene Anzahl von [SPropProblem](spropproblem.md) Strukturen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameter

__cprob_
  
> Anzahl der **SPropProblem** Strukturen, die in die neue Struktur eingeschlossen werden. 
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das Makro **SizedSPropProblemArray** , um ein Problem Array-Eigenschaft mit expliziten Grenzen zu erstellen. Um die neue Struktur verwenden, die als Zeiger auf eine **SPropProblemArray** -Struktur aus dem Makro **SizedSPropProblemArray** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Siehe auch

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

