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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357841"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array aus einer oder mehreren [SPropProblem](spropproblem.md) -Strukturen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
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
  
> Die Anzahl der [SPropProblem](spropproblem.md) -Strukturen in dem vom **aProblem** -Element angegebenen Array. 
    
 **aProblem**
  
> Array von **SPropProblem** -Strukturen, die jeweils einen Eigenschafts Fehler beschreiben. 
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zur Funktionsweise der **SPropProblem** -und **SPropProblemArray** -Strukturen mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[MAPI-Strukturen](mapi-structures.md)

