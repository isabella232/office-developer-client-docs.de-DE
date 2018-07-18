---
title: PidLidAppointmentAuxiliaryFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cac9c735403e6cb65dfe3111a2246a8387339339
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793338"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="698ed-103">PidLidAppointmentAuxiliaryFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="698ed-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="698ed-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="698ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="698ed-105">Gibt ein Bitfeld, das den Hilfs Status des Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="698ed-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="698ed-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="698ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="698ed-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="698ed-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="698ed-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="698ed-108">Property set:</span></span>  <br/> |<span data-ttu-id="698ed-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="698ed-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="698ed-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="698ed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="698ed-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="698ed-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="698ed-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="698ed-112">Data type:</span></span>  <br/> |<span data-ttu-id="698ed-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="698ed-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="698ed-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="698ed-114">Area:</span></span>  <br/> |<span data-ttu-id="698ed-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="698ed-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="698ed-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="698ed-116">Remarks</span></span>

<span data-ttu-id="698ed-117">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="698ed-117">This property is not required.</span></span> <span data-ttu-id="698ed-118">Im folgenden sind die einzelnen Flags, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="698ed-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="698ed-119">C (AuxApptFlagCopied, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="698ed-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="698ed-120">Dieses Kennzeichen gibt an, dass das Calendar-Objekt aus einer anderen Kalenderordner kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="698ed-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="698ed-121">R (AuxApptFlagForceMtgResponse, 0 x 00000002)</span><span class="sxs-lookup"><span data-stu-id="698ed-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="698ed-122">Dieses Kennzeichen auf eine Besprechungsanfrage gibt an, dass der Client oder Server gesendet wird eine Antwort auf Besprechungsanfrage wieder an den Organisator beim eine Antwort ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="698ed-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="698ed-123">F (AuxApptFlagForwarded, 0 x 00000004)</span><span class="sxs-lookup"><span data-stu-id="698ed-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="698ed-124">Dieses Flag auf eine Besprechungsanfrage bedeutet, dass sie weitergeleitet wurde (einschließlich vom Organisator weitergeleiteten), sondern wird eine Einladung aus organisieren.</span><span class="sxs-lookup"><span data-stu-id="698ed-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="698ed-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="698ed-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="698ed-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="698ed-126">Protocol specifications</span></span>

<span data-ttu-id="698ed-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="698ed-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="698ed-128">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="698ed-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="698ed-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="698ed-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="698ed-130">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="698ed-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="698ed-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="698ed-131">Header files</span></span>

<span data-ttu-id="698ed-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="698ed-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="698ed-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="698ed-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="698ed-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="698ed-134">See also</span></span>



[<span data-ttu-id="698ed-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="698ed-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="698ed-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="698ed-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="698ed-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="698ed-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="698ed-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="698ed-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

