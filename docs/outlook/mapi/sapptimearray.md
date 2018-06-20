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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795417"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von Zeitwerte an.
  
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
  
> Anzahl der Werte im Array auf den Member **Lpat** zeigt. 
    
 **lpat**
  
> Zeiger auf ein Array von Zeitwerte für die Anwendung. 
    
## <a name="remarks"></a>Hinweise

Die Struktur **SAppTimeArray** wird verwendet, um die Eigenschaften des Typs PT_MV_APPTIME definieren. Weitere Informationen zu PT_MV_APPTIME finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)

