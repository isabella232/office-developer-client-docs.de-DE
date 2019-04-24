---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361152"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von String-Werten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_STRING8 verwendet werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Die Anzahl der Werte im Array, auf die durch das **lppszA** -Element verwiesen wird. 
    
 **lppszA**
  
> Zeiger auf ein Array von NULL-beendeten 8-Bit-Zeichenfolgen.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_STRING8 finden Sie unter [Liste der Eigenschaftstypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

