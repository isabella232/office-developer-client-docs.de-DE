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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345430"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="d572b-103">PidLidAppointmentAuxiliaryFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d572b-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d572b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d572b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d572b-105">Gibt ein Bitfeld an, das den Hilfsstatus des Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d572b-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d572b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d572b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d572b-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="d572b-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="d572b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="d572b-108">Property set:</span></span>  <br/> |<span data-ttu-id="d572b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d572b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d572b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d572b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d572b-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="d572b-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="d572b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d572b-112">Data type:</span></span>  <br/> |<span data-ttu-id="d572b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d572b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d572b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d572b-114">Area:</span></span>  <br/> |<span data-ttu-id="d572b-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="d572b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d572b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d572b-116">Remarks</span></span>

<span data-ttu-id="d572b-117">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d572b-117">This property is not required.</span></span> <span data-ttu-id="d572b-118">Unten sind die einzelnen Flags aufgeführt, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="d572b-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="d572b-119">C (auxApptFlagCopied, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d572b-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="d572b-120">Dieses Flag gibt an, dass das Kalenderobjekt aus einem anderen Kalenderordner kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d572b-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="d572b-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d572b-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="d572b-122">Dieses Flag für eine Besprechungsanfrage gibt an, dass der Client oder Server eine Besprechungsantwort zurück an den Organisator senden soll, wenn eine Antwort ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d572b-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="d572b-123">F (auxApptFlagForwarded, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d572b-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="d572b-124">Dieses Flag für eine Besprechungsanfrage gibt an, dass es weitergeleitet wurde (einschließlich der Weiterleitung durch den Organisator), anstatt eine Einladung des Organisators zu sein.</span><span class="sxs-lookup"><span data-stu-id="d572b-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d572b-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d572b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d572b-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d572b-126">Protocol specifications</span></span>

<span data-ttu-id="d572b-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d572b-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d572b-128">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d572b-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d572b-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d572b-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d572b-130">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="d572b-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d572b-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d572b-131">Header files</span></span>

<span data-ttu-id="d572b-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d572b-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d572b-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d572b-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d572b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d572b-134">See also</span></span>



[<span data-ttu-id="d572b-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d572b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d572b-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d572b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d572b-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d572b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d572b-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d572b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

