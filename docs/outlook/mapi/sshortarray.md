---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99d2cfb9b4d460ed6a86235a011f9bf244aac0a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566465"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von ganzzahligen Werten ohne Vorzeichen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_SHORT zu beschreiben.
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das der **lpi-Member** verweist. 
    
 **Lpi**
  
> Zeiger auf ein Array von ganzzahligen Werten ohne Vorzeichen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_SHORT und anderen Eigenschaftstypen finden Sie unter [Property Types](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

