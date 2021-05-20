---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429614"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array nicht signierter ganzzahliger Werte, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_SHORT.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array, auf die das **lpi-Element verweist.** 
    
 **lpi**
  
> Zeiger auf ein Array nicht signierter ganzzahliger Werte.
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu PT_MV_SHORT und anderen Eigenschaftentypen finden Sie unter [Property Types](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

