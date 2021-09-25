---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 160fdc7ecc27a2a2a14882090f674441655540f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609495"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Doubles, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_DOUBLE zu beschreiben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte in dem Array, auf das vom **lpdbl-Element** verwiesen wird. 
    
 **lpdbl**
  
> Zeiger auf ein Array mit doppelten Werten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_DOUBLE finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

