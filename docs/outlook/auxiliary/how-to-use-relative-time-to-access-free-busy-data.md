---
title: Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Die IFreeBusyData-Schnittstelle in der Frei/Gebucht-API verwendet ein Konzept der relativen Zeit, d. h. die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt in Weltzeit (UTC) und ist ein Wert vom Typ LONG .
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317633"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Verwenden der relativen Zeit für den Zugriff auf Frei/Gebucht-Daten

Die [IFreeBusyData-Schnittstelle](ifreebusydata.md) in der Frei/Gebucht-API verwendet ein Konzept der relativen Zeit, d. h. die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt in Weltzeit (UTC) und ist ein Wert vom Typ **LONG**. 
  
Nachfolgend finden Sie einige häufig verwendete relative Zeitwerte:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Verwenden Sie die vorherigen werte für maximale und minimale relative Zeit, um zu überprüfen, ob ihre relativen Zeitwerte gültig sind.
  
Da NTFS Dateizeiten nativ im [FILETIME-Format](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) auftreibt, ist es möglicherweise hilfreich, das folgende Codebeispiel zu verwenden, um relative Zeit in **fileTIME** zu konvertieren. 
  
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

- [Informationen zur Frei/Gebucht-API](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

