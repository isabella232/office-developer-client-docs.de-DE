---
title: PidLidReminderDelta (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398004"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="f36eb-103">PidLidReminderDelta (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f36eb-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="f36eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f36eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f36eb-105">Gibt das Intervall in Minuten zwischen dem Zeitpunkt, wann die Erinnerung zuerst überfällig wird, und die Anfangszeit des Calendar-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f36eb-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f36eb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f36eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f36eb-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="f36eb-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="f36eb-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f36eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="f36eb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f36eb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f36eb-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="f36eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f36eb-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="f36eb-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="f36eb-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f36eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="f36eb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f36eb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f36eb-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f36eb-114">Area:</span></span>  <br/> |<span data-ttu-id="f36eb-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="f36eb-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f36eb-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f36eb-116">Remarks</span></span>

<span data-ttu-id="f36eb-117">Diese Eigenschaft muss auf Kalender-Objekte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f36eb-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="f36eb-118">Für alle Objekte, nicht-Kalender wird diese Eigenschaft auf "0 x 00000000" festgelegt werden und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f36eb-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="f36eb-119">Wenn eine Erinnerung für eine Instanz von sich wiederholenden Calendar-Objekt geschlossen ist, wird der Wert dieser Eigenschaft in der Berechnung der Zeit Signal an die nächste Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="f36eb-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="f36eb-120">Einzelheiten über das Erstellen von Calendar-Objekt finden Sie unter [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f36eb-120">See [[MS- OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f36eb-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f36eb-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f36eb-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f36eb-122">Protocol specifications</span></span>

<span data-ttu-id="f36eb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f36eb-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f36eb-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f36eb-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f36eb-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f36eb-125">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f36eb-126">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="f36eb-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f36eb-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f36eb-127">Header files</span></span>

<span data-ttu-id="f36eb-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f36eb-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f36eb-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f36eb-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f36eb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f36eb-130">See also</span></span>



[<span data-ttu-id="f36eb-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f36eb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f36eb-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f36eb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f36eb-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f36eb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f36eb-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f36eb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

