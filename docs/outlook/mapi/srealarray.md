---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795615"
---
# <a name="srealarray"></a>SRealArray

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von Float-Werten, mit denen eine Eigenschaft vom Typ PT_MV_R4 beschrieben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpflt** zeigt. 
    
 **lpflt**
  
> Zeiger auf ein Array von Float-Werten.
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu den Eigenschaftentyp PT_MV_R4 finden Sie unter [Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

