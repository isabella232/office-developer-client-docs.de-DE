---
title: PidLidTimeZoneStruct (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346375"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="effef-103">PidLidTimeZoneStruct (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="effef-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="effef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="effef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="effef-105">Enthält einen Datenstrom, der dem dauerhaften Format einer [TZREG-Struktur](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) zu ordnet, der die Zeitzone beschreibt, die für die Start- und Endzeit einer Termin- oder Besprechungsserie verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="effef-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="effef-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="effef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="effef-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="effef-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="effef-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="effef-108">Property set:</span></span>  <br/> |<span data-ttu-id="effef-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="effef-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="effef-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="effef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="effef-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="effef-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="effef-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="effef-112">Data type:</span></span>  <br/> |<span data-ttu-id="effef-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="effef-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="effef-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="effef-114">Area:</span></span>  <br/> |<span data-ttu-id="effef-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="effef-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="effef-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="effef-116">Remarks</span></span>

<span data-ttu-id="effef-117">Microsoft Office Outlook 2003, frühere Versionen von Outlook und Anwendungen, die auf CDO (Collaboration Data Objects) 1.21 basieren, deren Benutzer das von Outlook oder Exchange Server bereitgestellte Kalenderaktualisierungstool nicht ausgeführt haben, speichern die Start- und Endzeit eines Termins oder einer Besprechungsserie als relative Zeit, und speichern Sie die Zeitzone, in der die Termin- oder Besprechungsanfrage in **dispidTimeZoneStruct** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="effef-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="effef-118">Dieses Schema ignoriert jedoch, dass sich im Laufe der Zeit Zeitzonenregeln ändern können, was zu einigen Terminen und Besprechungen führt, die Benutzer vor der Änderung der Regeln geplant haben und zu falschen Zeiten auftreten.</span><span class="sxs-lookup"><span data-stu-id="effef-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="effef-119">Benutzer und Administratoren, die Windows Vista nicht ausgeführt werden oder die keine automatischen Updates aktiviert haben, sollten die kalenderbasierungstools verwenden, die von Outlook oder Exchange Server bereitgestellt werden, um die Uhrzeit solcher Termine und Besprechungsanfragen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="effef-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="effef-120">Weitere Informationen zu diesen Tools und APIs zum Neubasieren von Kalendern finden Sie unter Informationen zur programmgesteuerten Neubasierung von Kalendern für [Sommerzeit.](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="effef-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="effef-121">Verwenden Sie das folgende Little-Endian-Format, wenn Sie einen Datenstrom aus **dispidTimeZoneStruct** oder die **TZREG-Struktur** in einem Datenstrom beibehalten, um einen Commit für die **binäre Eigenschaft dispidTimeZoneStruct** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="effef-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="effef-122">Diese Eigenschaft wird für eine Serienserie festgelegt, um Zeitzoneninformationen anzugeben, und gibt an, wie Zeitfelder zwischen Ortszeit und koordinierter Weltzeit (Coordinated Universal Time, UTC) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="effef-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="effef-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="effef-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="effef-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="effef-124">Protocol specifications</span></span>

<span data-ttu-id="effef-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="effef-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="effef-126">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="effef-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="effef-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="effef-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="effef-128">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="effef-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="effef-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="effef-129">Header files</span></span>

<span data-ttu-id="effef-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="effef-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="effef-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="effef-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="effef-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="effef-132">See also</span></span>



[<span data-ttu-id="effef-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="effef-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="effef-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="effef-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="effef-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="effef-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="effef-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="effef-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

