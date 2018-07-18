---
title: Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Die IFreeBusyData-Schnittstelle in der Frei/Gebucht-API verwendet ein Konzept der relative Zeit, die die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt als Weltzeit (UTC) ist und einen Wert vom Typ LONG ist.
ms.openlocfilehash: b83cd46cfcc4d84d4fc3bf000dd8b0acdda545dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790946"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten

Die [IFreeBusyData](ifreebusydata.md) -Schnittstelle in der Frei/Gebucht-API verwendet ein Konzept der relative Zeit, die die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt als Weltzeit (UTC) ist und ist ein Wert vom Typ **LONG**. 
  
Im folgenden sind einige häufig verwendete relativen Zeitwerte:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Verwenden Sie die vorherigen Mindest- und relative Zeitwerte zu überprüfen, dass Ihre relativen Zeitwerte gültig sind.
  
Da NTFS Dateizeiten systemintern im [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) -Format aufzeichnet, kann es im folgenden Codebeispiel wird mit der relative Zeit und **FILETIME**konvertieren praktisch sein. 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a>Siehe auch

- [Über die Frei/Gebucht-API](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

