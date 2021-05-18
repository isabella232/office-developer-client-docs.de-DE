---
title: Lesen von Zeitzoneneigenschaften aus einem Termin
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ba1b9425-6c16-cab2-da0a-a21734118098
description: In diesem Thema wird die Funktion ReadTimeZones gezeigt, die die beiden Funktionen BinToTZDEFINITION und BinToTZREG aufruft, um die Zeitzoneneigenschaften PidLidAppointmentTimeZoneDefinitionStartDisplay und PidLidTimeZoneStruct aus einem Termin zu lesen.
ms.openlocfilehash: 67755ba49c5572005c6138e34329491148a199a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317619"
---
# <a name="read-time-zone-properties-from-an-appointment"></a><span data-ttu-id="2e830-103">Lesen von Zeitzoneneigenschaften aus einem Termin</span><span class="sxs-lookup"><span data-stu-id="2e830-103">Read time zone properties from an appointment</span></span>

<span data-ttu-id="2e830-104">In diesem Thema wird eine Funktion gezeigt, die die beiden Funktionen aufruft, und , um die Zeitzoneneigenschaften  `ReadTimeZones`  `BinToTZDEFINITION`  `BinToTZREG` [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) und [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)aus einem Termin zu lesen.</span><span class="sxs-lookup"><span data-stu-id="2e830-104">This topic shows a function,  `ReadTimeZones`, that calls the two functions,  `BinToTZDEFINITION` and  `BinToTZREG`, to read the time zone properties, [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) and [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx), from an appointment.</span></span>
  
<span data-ttu-id="2e830-105">**PidLidAppointmentTimeZoneDefinitionStartDisplay** enthält einen Datenstrom, der dem dauerhaften Format einer [TZDEFINITION-Struktur](tzdefinition.md) zu ordnet, und **PidLidTimeZoneStruct** enthält einen Datenstrom, der dem dauerhaften Format einer [TZREG-Struktur](tzreg.md) zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="2e830-105">**PidLidAppointmentTimeZoneDefinitionStartDisplay** contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure, and **PidLidTimeZoneStruct** contains a stream that maps to the persisted format of a [TZREG](tzreg.md) structure.</span></span> <span data-ttu-id="2e830-106">Um die genauen **TZDEFINITION-** und **TZREG-Strukturen** zu erhalten und werden verwendet, um die Datenstromwerte dieser  `BinToTZDEFINITION` Eigenschaften entsprechend zu  `BinToTZREG` analysieren.</span><span class="sxs-lookup"><span data-stu-id="2e830-106">To obtain the exact **TZDEFINITION** and **TZREG** structures,  `BinToTZDEFINITION` and  `BinToTZREG` are used to parse the stream values of these properties appropriately.</span></span> <span data-ttu-id="2e830-107">Diese beiden Funktionen sind in Parse a stream from a binary property definiert, um die [TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md) zu lesen und einen Datenstrom aus einer binären Eigenschaft zu analysieren, um die [TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)zu lesen.</span><span class="sxs-lookup"><span data-stu-id="2e830-107">These two functions are defined in [Parse a stream from a binary property to read the TZDEFINITION structure](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md) and [Parse a stream from a binary property to read the TZREG structure](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md), respectively.</span></span> 
  
```cpp
void ReadTimeZones(LPMAPIPROP lpAppointment) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID[2] = {0}; 
    LPMAPINAMEID lpNamedID[2]; 
    lpNamedID[0] = &amp;NamedID[0]; 
    lpNamedID[1] = &amp;NamedID[1]; 
    NamedID[0].lpguid = (LPGUID)&amp;PSETID_Appointment; 
    NamedID[0].ulKind = MNID_ID; 
    NamedID[0].Kind.lID = dispidTimeZoneStruct; 
    NamedID[1].lpguid = (LPGUID)&amp;PSETID_Appointment; 
    NamedID[1].ulKind = MNID_ID; 
    NamedID[1].Kind.lID = dispidApptTZDefStartDisplay; 
    hRes = lpAppointment->GetIDsFromNames( 
        2, 
        lpNamedID, 
        NULL, 
        &amp;lpNamedPropTags); 
    if (SUCCEEDED(hRes) &amp;&amp; lpNamedPropTags) 
    { 
        SizedSPropTagArray(2,sptaTzProps) = {2, 
            CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_BINARY), 
            CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[1],PT_BINARY), 
        }; 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
        hRes = lpAppointment->GetProps( 
            (LPSPropTagArray)&amp;sptaTzProps, 
            NULL, 
            &amp;cProps, 
            &amp;lpProps); 
        if (SUCCEEDED(hRes) &amp;&amp; 2 == cProps &amp;&amp; lpProps) 
        { 
            if (PT_BINARY == PROP_TYPE(lpProps[0].ulPropTag)) 
            { 
                TZREG* ptzReg = BinToTZREG(lpProps[0].Value.bin.cb,lpProps[0].Value.bin.lpb); 
                // TODO: Do whatever is necessary with ptzReg. 
                delete ptzReg; 
            } 
            if (PT_BINARY == PROP_TYPE(lpProps[1].ulPropTag)) 
            { 
                TZDEFINITION* ptzDef = BinToTZDEFINITION(lpProps[1].Value.bin.cb,lpProps[1].Value.bin.lpb); 
                // TODO: Do whatever is necessary with ptzDef. 
                delete[] ptzDef; 
            } 
           } 
        MAPIFreeBuffer(lpProps); 
    } 
    MAPIFreeBuffer(lpNamedPropTags); 
}
```

## <a name="see-also"></a><span data-ttu-id="2e830-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e830-108">See also</span></span>

- [<span data-ttu-id="2e830-109">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="2e830-109">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

