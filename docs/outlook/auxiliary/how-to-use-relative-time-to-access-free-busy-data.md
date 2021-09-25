---
title: Relative Zeit für den Zugriff auf Frei/Gebucht-Daten verwenden
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Die IFreeBusyData-Schnittstelle in der Frei/Gebucht-API verwendet ein Konzept der relativen Zeit, d. h. die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt in Weltzeit (UTC), und ist ein Wert vom Typ LONG .
ms.openlocfilehash: df42b3af0fa2f0e85a0c89cea060de76996f4a01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557302"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Relative Zeit für den Zugriff auf Frei/Gebucht-Daten verwenden

Die [IFreeBusyData-Schnittstelle](ifreebusydata.md) in der Frei/Gebucht-API verwendet ein Konzept der relativen Zeit, d. h. die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt in Weltzeit (UTC), und ist ein Wert vom Typ **LONG**. 
  
Nachfolgend sind einige häufig verwendete relative Zeitwerte aufgeführt:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Verwenden Sie die vorhergehenden maximalen und minimalen relativen Zeitwerte, um zu überprüfen, ob Ihre relativen Zeitwerte gültig sind.
  
Da NTFS Dateizeiten nativ im [FILETIME-Format](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) aufzeichnet, kann es hilfreich sein, das folgende Codebeispiel zum Konvertieren der relativen Zeit in und von **FILETIME** zu verwenden. 
  
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

