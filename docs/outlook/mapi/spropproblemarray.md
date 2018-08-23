---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e71658922b6cb80dadc7e034a51c10189c4207ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568497"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Strukturen für eine oder mehrere [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Elemente

 **cProblem**
  
> Anzahl der [SPropProblem](spropproblem.md) Strukturen in der durch das **aProblem** -Element angegebenen Arrays. 
    
 **aProblem**
  
> Array von **SPropProblem** -Strukturen, jeder, einen Eigenschaftsfehler beschreibt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zur Funktionsweise von der Strukturen **SPropProblem** und **SPropProblemArray** mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[MAPI-Strukturen](mapi-structures.md)

