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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572872"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array mit String-Werten, mit denen eine Eigenschaft vom Typ PT_MV_STRING8 beschrieben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array auf den Member **LppszA** zeigt. 
    
 **lppszA**
  
> Zeiger auf ein Array von Zeichenfolgen mit Null beendet 8-Bit-Zeichen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_STRING8 finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

