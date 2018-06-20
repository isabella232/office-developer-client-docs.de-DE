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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795474"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpcur** zeigt. 
    
 **lpcur**
  
> Zeiger auf ein Array von [Währung](currency.md) Strukturen, die Währungswerte enthalten. 
    
## <a name="remarks"></a>Hinweise

Informationen zu PT_MV_CURRENCY finden Sie unter [Liste der Eigenschaftentypen](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[WÄHRUNG](currency.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

