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
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282691"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropProblemArray](spropproblemarray.md) -Struktur, die eine angegebene Anzahl von [SPropProblem](spropproblem.md) -Strukturen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameter

__cprob_
  
> Die Anzahl der **SPropProblem** -Strukturen, die in die neue Struktur eingeschlossen werden sollen. 
    
__Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **SizedSPropProblemArray** -Makro, um ein Eigenschaften Problem Array mit expliziten Begrenzungen zu erstellen. Um die neue Struktur zu verwenden, die aus dem **SizedSPropProblemArray** -Makro als Zeiger auf eine **SPropProblemArray** -Struktur resultiert, führen Sie die folgenden Schritte aus: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Siehe auch

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

