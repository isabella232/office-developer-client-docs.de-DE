---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea314971e43450235bab8af806ad810a718bd6f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550001"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) Strukturen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_I8 zu beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das vom **lpli-Element** verwiesen wird. 
    
 **lpli**
  
> Zeiger auf ein Array von **LARGE_INTEGER** Strukturen, die die ganzzahligen Werte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_18 finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

