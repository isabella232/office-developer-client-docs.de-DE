---
title: PidLidFExceptionalAttendees (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 544b5b5ac945eeedf787af0e311491da1f9d0217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327475"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="ed529-103">PidLidFExceptionalAttendees (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed529-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="ed529-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed529-105">Gibt an, ob es sich bei dieser Eigenschaft um ein wiederkehrendes Kalenderobjekt mit einer oder mehreren Ausnahmen handelt, und mindestens eine der eingebetteten Ausnahmenachrichten verfügt über mindestens ein RecipientRow-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed529-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed529-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ed529-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed529-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="ed529-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="ed529-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ed529-108">Property set:</span></span>  <br/> |<span data-ttu-id="ed529-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ed529-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ed529-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ed529-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ed529-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="ed529-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="ed529-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ed529-112">Data type:</span></span>  <br/> |<span data-ttu-id="ed529-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ed529-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ed529-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ed529-114">Area:</span></span>  <br/> |<span data-ttu-id="ed529-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="ed529-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed529-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed529-116">Remarks</span></span>

<span data-ttu-id="ed529-117">Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass das Kalenderobjekt entweder keine Ausnahmen hat oder keine der eingebetteten Ausnahmenachrichten RecipientRows besitzt.</span><span class="sxs-lookup"><span data-stu-id="ed529-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed529-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ed529-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed529-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ed529-119">Protocol specifications</span></span>

<span data-ttu-id="ed529-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed529-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed529-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ed529-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed529-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed529-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed529-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="ed529-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed529-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ed529-124">Header files</span></span>

<span data-ttu-id="ed529-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed529-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed529-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ed529-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed529-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed529-127">See also</span></span>



[<span data-ttu-id="ed529-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed529-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed529-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ed529-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed529-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ed529-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed529-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ed529-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

