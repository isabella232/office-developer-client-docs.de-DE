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
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573033"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Werten Ganzzahl ohne Vorzeichen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_SHORT zu beschreiben.
  
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
  
> Anzahl der Werte im Array auf den Member **Lpi** zeigt. 
    
 **lpi**
  
> Zeiger auf ein Array von Werten Ganzzahl ohne Vorzeichen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_SHORT und anderer Eigenschaftsarten finden Sie unter [Eigenschaftentypen](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

