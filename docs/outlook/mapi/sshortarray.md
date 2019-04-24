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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344499"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Ganzzahlwerten ohne Vorzeichen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_SHORT verwendet werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Die Anzahl der Werte im Array, auf die durch das **LPI** -Element verwiesen wird. 
    
 **LPI**
  
> Zeiger auf ein Array von Ganzzahlwerten ohne Vorzeichen.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_SHORT und anderen Eigenschaftstypen finden Sie unter [Property Types](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

