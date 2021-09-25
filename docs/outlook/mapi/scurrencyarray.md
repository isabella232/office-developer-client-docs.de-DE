---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 37847a0c2d5f4dcea96e7b3a7af6094e94a78791
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586754"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Währungswerten, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_CURRENCY zu beschreiben. 
  
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
  
> Anzahl der Werte im Array, auf das vom **lpcur-Element** verwiesen wird. 
    
 **lpcur**
  
> Zeiger auf ein Array von [CURRENCY-Strukturen,](currency.md) die die Währungswerte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Informationen zu PT_MV_CURRENCY finden Sie unter [Liste der Eigenschaftstypen.](property-types.md) 
  
## <a name="see-also"></a>Siehe auch



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

