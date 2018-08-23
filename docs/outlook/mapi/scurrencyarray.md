---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572452"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Währungswerten, mit denen eine Eigenschaft vom Typ PT_MV_CURRENCY beschrieben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpcur** zeigt. 
    
 **lpcur**
  
> Zeiger auf ein Array von [Währung](currency.md) Strukturen, die Währungswerte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Informationen zu PT_MV_CURRENCY finden Sie unter [Liste der Eigenschaftentypen](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

