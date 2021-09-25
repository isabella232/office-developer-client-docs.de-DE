---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f68d703a9bdab23f07f5f53af0f35b69384526cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566556"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array aus einer oder mehreren [SPropProblem-Strukturen.](spropproblem.md) 
  
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

## <a name="members"></a>Members

 **cProblem**
  
> Anzahl der [SPropProblem-Strukturen](spropproblem.md) im Array, das durch das **aProblem-Element** angegeben wird. 
    
 **aProblem**
  
> Array von **SPropProblem-Strukturen,** die jeweils einen Eigenschaftsfehler beschreiben. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen dazu, wie die **Strukturen SPropProblem** und **SPropProblemArray** mit Fehlern im Zusammenhang mit Eigenschaften arbeiten, finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[MAPI-Strukturen](mapi-structures.md)

