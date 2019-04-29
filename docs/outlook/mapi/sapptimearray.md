---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430385"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeitwerten.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Die Anzahl der Werte im Array, auf die durch das **lpat** -Element verwiesen wird. 
    
 **lpat**
  
> Zeiger auf ein Array von Anwendungszeit Werten. 
    
## <a name="remarks"></a>Bemerkungen

Die **SAppTimeArray** -Struktur wird verwendet, um Eigenschaften vom Typ PT_MV_APPTIME zu definieren. Weitere Informationen zu PT_MV_APPTIME finden Sie unter [Liste der Eigenschaftstypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

