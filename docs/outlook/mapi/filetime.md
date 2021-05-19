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
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409503"
---
# <a name="filetime"></a>FILETIME

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen nicht signierten 64-Bit-Datums- und Uhrzeitwert für eine Datei. Dieser Wert stellt die Anzahl von 100 Nanosekundeneinheiten seit Dem 1. Januar 1601 dar. 
  
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
  
> Niedrige Reihenfolge 32 Bit des Dateizeitwerts. 
    
 **dwHighDateTime**
  
> 32 Bit des Dateizeitwerts in hoher Reihenfolge.
    
## <a name="remarks"></a>Hinweise

Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME-Struktur** für ihren Wert. Eine solche Eigenschaft verfügt über einen **FILETIME-Datentyp** für das **Value-Element** in seiner Definition in einer [SPropValue-Struktur.](spropvalue.md) 
  
Die Definition der **FILETIME-Struktur** befindet sich in  _der Win32-Programmerreferenz_ und in der MAPI-Headerdatei Mapidefs.h. MAPI definiert die Struktur bedingt, um sicherzustellen, dass sie definiert ist, wenn die Win32-Definition nicht verfügbar ist. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

