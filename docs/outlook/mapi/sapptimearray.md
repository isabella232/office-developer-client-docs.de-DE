---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ebb7366dbbc49cfe38a95383f64b1195ef401fd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550148"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeitwerten.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das der **lpat-Member** verweist. 
    
 **lpat**
  
> Zeiger auf ein Array von Anwendungszeitwerten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **SAppTimeArray-Struktur** wird verwendet, um Eigenschaften vom Typ PT_MV_APPTIME zu definieren. Weitere Informationen zu PT_MV_APPTIME finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

