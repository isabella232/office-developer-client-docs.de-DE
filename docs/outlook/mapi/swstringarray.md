---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795684"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von Zeichenfolgen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_UNICODE zu beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Zeichenfolgen im Array auf den Member **LppszW** zeigt. 
    
 **lppszW**
  
> Zeiger auf ein Array von Zeichenfolgen mit Unicode-Zeichen Null beendet.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

