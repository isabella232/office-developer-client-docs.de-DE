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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795550"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Hinweise

Verwenden Sie das Makro **SizedSPropProblemArray** , um ein Problem Array-Eigenschaft mit expliziten Grenzen zu erstellen. Um die neue Struktur verwenden, die als Zeiger auf eine **SPropProblemArray** -Struktur aus dem Makro **SizedSPropProblemArray** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Siehe auch

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

