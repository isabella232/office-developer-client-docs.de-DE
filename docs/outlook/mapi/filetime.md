---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583253"
---
# <a name="filetime"></a>FILETIME

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine nicht signierte 64-Bit-Datums- und Uhrzeitwert für eine Datei. Dieser Wert gibt die Anzahl der Einheiten von 100 Nanosekunden seit dem Start der 1. Januar 1601. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Elemente

 **dwLowDateTime**
  
> Niederwertige 32 Bit der Datei Time-Wert. 
    
 **dwHighDateTime**
  
> Obere 32 Bit der Datei Time-Wert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME** -Struktur für ihren Wert. Eine solche Eigenschaft hat einen **FILETIME** -Datentyp für den **Wert** Member in der Definition in eine [SPropValue](spropvalue.md) -Struktur. 
  
Die Definition der **FILETIME** -Struktur ist in der _Win32 Programmer's Reference_ und in der MAPI-Headerdatei Mapidefs.h. MAPI definiert die Struktur bedingt, um sicherzustellen, dass er definiert wird, wenn die Win32-Definition nicht verfügbar ist. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

