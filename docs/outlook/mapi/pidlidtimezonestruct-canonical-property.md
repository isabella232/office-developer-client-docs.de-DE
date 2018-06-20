---
title: Kanonische PidLidTimeZoneStruct-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1a96cdb3aed03b9621097f1ef858a09391c0693
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793869"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="6a428-103">Kanonische PidLidTimeZoneStruct-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a428-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="6a428-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a428-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a428-105">Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) ist die beschreibt die Zeitzone für die Start- und Endzeit Tageszeit in einer Terminserie für einen Termin oder eine Besprechungsanfrage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a428-105">Contains a stream that maps to the persisted format of a [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a428-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6a428-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a428-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="6a428-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="6a428-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6a428-108">Property set:</span></span>  <br/> |<span data-ttu-id="6a428-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6a428-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6a428-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="6a428-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6a428-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="6a428-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="6a428-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6a428-112">Data type:</span></span>  <br/> |<span data-ttu-id="6a428-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6a428-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6a428-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6a428-114">Area:</span></span>  <br/> |<span data-ttu-id="6a428-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="6a428-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a428-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a428-116">Remarks</span></span>

<span data-ttu-id="6a428-117">Microsoft Office Outlook 2003 der Start- und Endzeit der frühere Versionen von Outlook und Anwendungen, die Collaboration Data Objects (CDO) 1.21 basieren, dessen Benutzer das Tool Kalender Update von Outlook oder Exchange Server nicht ausgeführt haben, Speichern einer wiederkehrende Termin oder eine Besprechungsanfrage als relative Zeit, und speichern Sie die Zeitzone, in dem die Termin- oder Besprechungsanfragen in **DispidTimeZoneStruct**erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6a428-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="6a428-118">Im Laufe der Zeit Zeitzonenregeln ändern können, was in einigen Termine und Besprechungen geplant wurden, bevor die Regeln geändert und falsche Zeiten auftreten, die Benutzer ignoriert dieses Schema jedoch.</span><span class="sxs-lookup"><span data-stu-id="6a428-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="6a428-119">Verwenden den Kalender, Neuzuordnen von Tools, die von Outlook oder Exchange Server, um die Zeit solcher Termine und Besprechungsanfragen anzupassen bereitgestellt werden sollten Benutzern und Administratoren, die nicht mit Windows Vista oder besitzen keine automatische Updates aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a428-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="6a428-120">Weitere Informationen zu diesen Kalender Basisadressen Tools und APIs, die einer Kalender, finden Sie unter [About Basisadressen Kalender für Sommerzeit programmgesteuert](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a428-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="6a428-121">Verwenden Sie das folgende little-Endian-Format bei der Analyse eines Stream-Objekts abgerufen aus **DispidTimeZoneStruct**oder, wenn die **TZREG** -Struktur in einem Stream-Objekt gespeichert, an die binäre Eigenschaft **DispidTimeZoneStruct** übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6a428-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="6a428-122">Diese Eigenschaft ist für eine Terminserie festgelegt, Zeitzone Informationen an und gibt an, wie Uhrzeitfelder zwischen lokaler Zeit und koordinierter Weltzeit (UTC) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6a428-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a428-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a428-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a428-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6a428-124">Protocol specifications</span></span>

<span data-ttu-id="6a428-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a428-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a428-126">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6a428-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a428-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a428-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a428-128">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="6a428-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a428-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6a428-129">Header files</span></span>

<span data-ttu-id="6a428-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a428-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a428-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6a428-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a428-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a428-132">See also</span></span>



[<span data-ttu-id="6a428-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a428-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a428-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a428-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a428-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6a428-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a428-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6a428-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
