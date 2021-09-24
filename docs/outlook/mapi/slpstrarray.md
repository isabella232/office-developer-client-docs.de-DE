---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c5bc772a997b71a8adda3c11a1ac43ce1b7cee03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549994"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeichenfolgenwerten, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_STRING8 zu beschreiben.
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte in dem Array, auf das der **lppszA-Member** verweist. 
    
 **lppszA**
  
> Zeiger auf ein Array von 8-Bit-Zeichenfolgen mit Nullende.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_STRING8 finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

