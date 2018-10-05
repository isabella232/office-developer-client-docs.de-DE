---
title: PidLidFInvited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c2ddb5da9202e9cf0d1c78da1c1ad085ef9687c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386152"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="59b04-103">PidLidFInvited (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="59b04-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="59b04-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59b04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59b04-105">Gibt an, ob Einladungen für die Besprechung gesendet wurden, die diese Besprechung darstellt.</span><span class="sxs-lookup"><span data-stu-id="59b04-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59b04-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="59b04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59b04-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="59b04-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="59b04-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="59b04-108">Property set:</span></span>  <br/> |<span data-ttu-id="59b04-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="59b04-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="59b04-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="59b04-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="59b04-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="59b04-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="59b04-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="59b04-112">Data type:</span></span>  <br/> |<span data-ttu-id="59b04-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="59b04-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="59b04-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="59b04-114">Area:</span></span>  <br/> |<span data-ttu-id="59b04-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="59b04-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59b04-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59b04-116">Remarks</span></span>

<span data-ttu-id="59b04-117">Den Wert FALSE oder das fehlen diese Eigenschaft gibt an, dass eine Besprechungsanfrage nie gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="59b04-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="59b04-118">Der Wert TRUE gibt an, dass eine Besprechungsanfrage gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="59b04-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="59b04-119">Dieser Wert auf eine Besprechung auf TRUE festgelegt ist, muss es nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="59b04-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59b04-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="59b04-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59b04-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="59b04-121">Protocol specifications</span></span>

<span data-ttu-id="59b04-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59b04-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59b04-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="59b04-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59b04-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59b04-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59b04-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="59b04-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59b04-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="59b04-126">Header files</span></span>

<span data-ttu-id="59b04-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59b04-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="59b04-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="59b04-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59b04-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59b04-129">See also</span></span>



[<span data-ttu-id="59b04-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59b04-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59b04-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59b04-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59b04-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="59b04-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59b04-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="59b04-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

