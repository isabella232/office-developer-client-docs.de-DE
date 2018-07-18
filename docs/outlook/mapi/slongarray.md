---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795566"
---
# <a name="slongarray"></a>SLongArray

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von LONG-Werttypen, mit denen eine Eigenschaft vom Typ PT_MV_LONG beschrieben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpl** zeigt. 
    
 **LPL**
  
> Zeiger auf ein Array von LONG-Werte.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_LONG finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

