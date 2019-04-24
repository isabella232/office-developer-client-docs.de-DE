---
title: Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9e36e0d9-a28b-5978-0e23-f76e1bf506b5
description: In diesem Thema wird gezeigt, wie die TZREG-Struktur aus dem beibehaltenen Format gelesen wird, das in der binären Eigenschaft Pidlidtimezonestruct (gespeichert ist.
ms.openlocfilehash: f59251ebc980ca10f4ddce76b34e700bc430540a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317654"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure"></a><span data-ttu-id="4f6a9-103">Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur</span><span class="sxs-lookup"><span data-stu-id="4f6a9-103">Parse a stream from a binary property to read the TZREG structure</span></span>

<span data-ttu-id="4f6a9-104">In diesem Thema wird gezeigt, wie die [TZREG](tzreg.md) -Struktur aus dem beibehaltenen Format gelesen wird, das in der binären Eigenschaft [pidlidtimezonestruct (](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4f6a9-104">This topic shows how to read the [TZREG](tzreg.md) structure from the persisted format stored in the binary property [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span>
  
```cpp
TZREG* BinToTZREG(ULONG cbReg, LPBYTE lpbReg)  
{ 
    if (!lpbReg) return NULL;  
 
    // Update this if parsing code is changed. 
    if (cbReg &amp;lt; 3*sizeof(long) + 2*sizeof(WORD) + 2*sizeof(SYSTEMTIME)) return NULL; 
 
    TZREG tzReg = {0}; 
    LPBYTE lpPtr = lpbReg; 
 
    tzReg.lBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lStandardBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lDaylightBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    lpPtr += sizeof(WORD);// reserved 
 
    tzReg.stStandardDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
    lpPtr += sizeof(WORD);// reserved 
    tzReg.stDaylightDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
 
    TZREG* ptzReg = NULL; 
    ptzReg = new TZREG; 
    if (ptzReg) 
    { 
        *ptzReg = tzReg; 
    } 
 
    return ptzReg; 
} 

```

## <a name="see-also"></a><span data-ttu-id="4f6a9-105">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f6a9-105">See also</span></span>

- [<span data-ttu-id="4f6a9-106">Lesen von Zeitzoneneigenschaften aus einem Termin</span><span class="sxs-lookup"><span data-stu-id="4f6a9-106">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

