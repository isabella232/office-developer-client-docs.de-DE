---
title: Kanonische PidLidAppointmentStateFlags-Eigenschaft
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
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793428"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="d516a-103">Kanonische PidLidAppointmentStateFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d516a-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d516a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d516a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d516a-105">Gibt ein Bitfeld, das den Status des Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d516a-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d516a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d516a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d516a-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="d516a-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="d516a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d516a-108">Property set:</span></span>  <br/> |<span data-ttu-id="d516a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d516a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d516a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d516a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d516a-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="d516a-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="d516a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d516a-112">Data type:</span></span>  <br/> |<span data-ttu-id="d516a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d516a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d516a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d516a-114">Area:</span></span>  <br/> |<span data-ttu-id="d516a-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="d516a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d516a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d516a-116">Remarks</span></span>

<span data-ttu-id="d516a-117">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d516a-117">This property is not required.</span></span> <span data-ttu-id="d516a-118">Im folgenden sind die einzelnen Flags, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="d516a-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="d516a-119">M (AsfMeeting, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="d516a-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="d516a-120">Dieses Kennzeichen gibt an, dass das Objekt einer Besprechung oder bezüglich Besprechungen-Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="d516a-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="d516a-121">R (AsfReceived, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="d516a-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="d516a-122">Dieses Kennzeichen gibt an, dass das dargestellte Objekt aus einer anderen Person empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d516a-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="d516a-123">C (AsfCanceled, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="d516a-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="d516a-124">Dieses Kennzeichen gibt an, dass das Besprechung-Objekt, das durch das Objekt dargestellten abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="d516a-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d516a-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d516a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d516a-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d516a-126">Protocol specifications</span></span>

<span data-ttu-id="d516a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d516a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d516a-128">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d516a-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d516a-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d516a-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d516a-130">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d516a-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d516a-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d516a-131">Header files</span></span>

<span data-ttu-id="d516a-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d516a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d516a-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d516a-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d516a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d516a-134">See also</span></span>



[<span data-ttu-id="d516a-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d516a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d516a-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d516a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d516a-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d516a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d516a-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d516a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

