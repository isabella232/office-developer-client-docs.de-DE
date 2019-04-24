---
title: Kanonische Pidlidappointmentstateflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345360"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="cc24f-103">Kanonische Pidlidappointmentstateflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc24f-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="cc24f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc24f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc24f-105">Gibt ein Bitfeld an, das den Status des Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cc24f-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc24f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cc24f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc24f-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="cc24f-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="cc24f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="cc24f-108">Property set:</span></span>  <br/> |<span data-ttu-id="cc24f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="cc24f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="cc24f-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="cc24f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cc24f-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="cc24f-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="cc24f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cc24f-112">Data type:</span></span>  <br/> |<span data-ttu-id="cc24f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc24f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc24f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cc24f-114">Area:</span></span>  <br/> |<span data-ttu-id="cc24f-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="cc24f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc24f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc24f-116">Remarks</span></span>

<span data-ttu-id="cc24f-117">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cc24f-117">This property is not required.</span></span> <span data-ttu-id="cc24f-118">Nachfolgend finden Sie die einzelnen Flags, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="cc24f-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="cc24f-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="cc24f-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="cc24f-120">Dieses Flag gibt an, dass das Objekt ein Besprechungsobjekt oder ein Besprechungs bezogenes Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="cc24f-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="cc24f-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="cc24f-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="cc24f-122">Dieses Kennzeichen gibt an, dass das dargestellte Objekt von einer anderen Person empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc24f-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="cc24f-123">C (asfCanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="cc24f-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="cc24f-124">Dieses Flag gibt an, dass das vom Objekt dargestellte Besprechungsobjekt abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc24f-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="cc24f-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cc24f-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc24f-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cc24f-126">Protocol specifications</span></span>

<span data-ttu-id="cc24f-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc24f-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc24f-128">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="cc24f-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc24f-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc24f-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc24f-130">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="cc24f-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc24f-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cc24f-131">Header files</span></span>

<span data-ttu-id="cc24f-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cc24f-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc24f-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cc24f-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc24f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc24f-134">See also</span></span>



[<span data-ttu-id="cc24f-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc24f-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc24f-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc24f-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc24f-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cc24f-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc24f-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cc24f-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

