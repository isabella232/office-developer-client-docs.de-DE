---
title: Kanonische Pidlidreminderdelta (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315890"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="13c7e-103">Kanonische Pidlidreminderdelta (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="13c7e-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="13c7e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13c7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13c7e-105">Gibt das Intervall in Minuten zwischen dem Zeitpunkt an, zu dem die Erinnerung zuerst überfällig wird, und der Startzeit des Calendar-Objekts.</span><span class="sxs-lookup"><span data-stu-id="13c7e-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13c7e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="13c7e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13c7e-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="13c7e-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="13c7e-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="13c7e-108">Property set:</span></span>  <br/> |<span data-ttu-id="13c7e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="13c7e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="13c7e-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="13c7e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13c7e-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="13c7e-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="13c7e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="13c7e-112">Data type:</span></span>  <br/> |<span data-ttu-id="13c7e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="13c7e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="13c7e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="13c7e-114">Area:</span></span>  <br/> |<span data-ttu-id="13c7e-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="13c7e-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13c7e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13c7e-116">Remarks</span></span>

<span data-ttu-id="13c7e-117">Diese Eigenschaft muss für Calendar-Objekte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="13c7e-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="13c7e-118">Für alle nicht-Calendar-Objekte sollte diese Eigenschaft auf "0x00000000" festgelegt werden und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="13c7e-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="13c7e-119">Wenn eine Erinnerung für eine Instanz eines wiederkehrenden Kalenderobjekts geschlossen wird, wird der Wert dieser Eigenschaft bei der Berechnung der Signal Zeit für die nächste Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="13c7e-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="13c7e-120">Weitere Informationen zur Erstellung von Kalenderobjekten finden Sie unter [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="13c7e-120">See [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13c7e-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13c7e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13c7e-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="13c7e-122">Protocol specifications</span></span>

<span data-ttu-id="13c7e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c7e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c7e-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="13c7e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13c7e-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c7e-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c7e-126">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="13c7e-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13c7e-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="13c7e-127">Header files</span></span>

<span data-ttu-id="13c7e-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="13c7e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="13c7e-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="13c7e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13c7e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13c7e-130">See also</span></span>



[<span data-ttu-id="13c7e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13c7e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13c7e-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13c7e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13c7e-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="13c7e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13c7e-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="13c7e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

