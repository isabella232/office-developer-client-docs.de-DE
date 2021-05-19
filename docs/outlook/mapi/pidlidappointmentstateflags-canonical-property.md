---
title: PidLidAppointmentStateFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345360"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="12fca-103">PidLidAppointmentStateFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="12fca-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="12fca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12fca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12fca-105">Gibt ein Bitfeld an, das den Status des Objekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="12fca-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12fca-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="12fca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12fca-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="12fca-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="12fca-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="12fca-108">Property set:</span></span>  <br/> |<span data-ttu-id="12fca-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="12fca-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="12fca-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="12fca-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="12fca-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="12fca-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="12fca-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="12fca-112">Data type:</span></span>  <br/> |<span data-ttu-id="12fca-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="12fca-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="12fca-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="12fca-114">Area:</span></span>  <br/> |<span data-ttu-id="12fca-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="12fca-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12fca-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="12fca-116">Remarks</span></span>

<span data-ttu-id="12fca-117">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="12fca-117">This property is not required.</span></span> <span data-ttu-id="12fca-118">Unten sind die einzelnen Flags aufgeführt, die festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="12fca-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="12fca-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12fca-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="12fca-120">Dieses Flag gibt an, dass es sich bei dem Objekt um ein Besprechungsobjekt oder ein besprechungsbezogenes Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="12fca-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="12fca-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="12fca-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="12fca-122">Dieses Flag gibt an, dass das dargestellte Objekt von einer anderen Person empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="12fca-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="12fca-123">C (asfCanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="12fca-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="12fca-124">Dieses Flag gibt an, dass das durch das Objekt dargestellte Besprechungsobjekt abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="12fca-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="12fca-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="12fca-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12fca-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="12fca-126">Protocol specifications</span></span>

<span data-ttu-id="12fca-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12fca-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12fca-128">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="12fca-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12fca-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12fca-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12fca-130">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="12fca-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12fca-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="12fca-131">Header files</span></span>

<span data-ttu-id="12fca-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12fca-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="12fca-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="12fca-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12fca-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12fca-134">See also</span></span>



[<span data-ttu-id="12fca-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12fca-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12fca-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="12fca-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12fca-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="12fca-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12fca-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="12fca-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

