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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334811"
---
# <a name="filetime"></a>FILETIME

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen nicht signierten 64-Bit-Wert für Datum und Uhrzeit für eine Datei. Dieser Wert stellt die Anzahl von 100-Nanosekunden-Einheiten seit Beginn des 1. Januar 1601. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Elemente

 **dwLowDateTime**
  
> Low-Order 32 Bits des dateitime-Werts. 
    
 **dwHighDateTime**
  
> Hochwertige 32-Bits des dateitime-Werts.
    
## <a name="remarks"></a>Bemerkungen

Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME** -Struktur für ihren Wert. Eine solche Eigenschaft verfügt über **** einen FILETIME-Datentyp für das **value** -Element in der Definition in einer [SPropValue](spropvalue.md) -Struktur. 
  
Die Definition der FILETIME-Struktur befindet sich in der _Win32-Programmierreferenz_ und in der MAPI-Headerdatei Mapidefs. h. **** MAPI definiert die strukturbedingt, um sicherzustellen, dass Sie definiert wird, wenn die Win32-Definition nicht verfügbar ist. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

