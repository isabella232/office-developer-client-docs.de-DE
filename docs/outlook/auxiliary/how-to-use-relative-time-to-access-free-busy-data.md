---
title: Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Die IFreeBusyData-Schnittstelle in der Frei/Gebucht-API verwendet ein Konzept der relative Zeit, die die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt als Weltzeit (UTC) ist und einen Wert vom Typ LONG ist.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386936"
---
# <a name="use-relative-time-to-access-freebusy-data"></a><span data-ttu-id="b9273-103">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="b9273-103">Use relative time to access free/busy data</span></span>

<span data-ttu-id="b9273-104">Die [IFreeBusyData](ifreebusydata.md) -Schnittstelle in der Frei/Gebucht-API verwendet ein Konzept der relative Zeit, die die Anzahl der Minuten seit dem 1. Januar 1601, ausgedrückt als Weltzeit (UTC) ist und ist ein Wert vom Typ **LONG**.</span><span class="sxs-lookup"><span data-stu-id="b9273-104">The [IFreeBusyData](ifreebusydata.md) interface in the Free/Busy API uses a concept of relative time, which is the number of minutes since January 1, 1601, expressed in Universal Time (UTC), and is a value of type **LONG**.</span></span> 
  
<span data-ttu-id="b9273-105">Im folgenden sind einige häufig verwendete relativen Zeitwerte:</span><span class="sxs-lookup"><span data-stu-id="b9273-105">The following are some commonly used relative time values:</span></span>
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
<span data-ttu-id="b9273-106">Verwenden Sie die vorherigen Mindest- und relative Zeitwerte zu überprüfen, dass Ihre relativen Zeitwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="b9273-106">Use the preceding maximum and minimum relative time values to help verify that your relative time values are valid.</span></span>
  
<span data-ttu-id="b9273-107">Da NTFS Dateizeiten systemintern im [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) -Format aufzeichnet, kann es im folgenden Codebeispiel wird mit der relative Zeit und **FILETIME**konvertieren praktisch sein.</span><span class="sxs-lookup"><span data-stu-id="b9273-107">Because NTFS records file times natively in [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) format, it might be handy to use the following code example to convert relative time to and from **FILETIME**.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b9273-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9273-108">See also</span></span>

- [<span data-ttu-id="b9273-109">Informationen zur Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="b9273-109">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="b9273-110">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="b9273-110">IFreeBusyData</span></span>](ifreebusydata.md)

