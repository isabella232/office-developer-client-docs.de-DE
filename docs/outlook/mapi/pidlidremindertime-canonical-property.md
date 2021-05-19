---
title: PidLidReminderTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358709"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="c9ce8-103">PidLidReminderTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c9ce8-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="c9ce8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9ce8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9ce8-105">Gibt die Anfangssignalzeit für eine Erinnerung an.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9ce8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c9ce8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9ce8-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="c9ce8-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="c9ce8-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c9ce8-108">Property set:</span></span>  <br/> |<span data-ttu-id="c9ce8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c9ce8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c9ce8-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c9ce8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c9ce8-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="c9ce8-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="c9ce8-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c9ce8-112">Data type:</span></span>  <br/> |<span data-ttu-id="c9ce8-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c9ce8-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c9ce8-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c9ce8-114">Area:</span></span>  <br/> |<span data-ttu-id="c9ce8-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="c9ce8-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9ce8-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9ce8-116">Remarks</span></span>

<span data-ttu-id="c9ce8-117">Bei Kalenderobjekten stellt diese Eigenschaft den Zeitpunkt dar, zu dem der Benutzer zu spät kommt, d. h. die Startzeit des Termins.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="c9ce8-118">Clients müssen den Wert in koordinierter Weltzeit (Coordinated Universal Time, UTC) festlegen.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9ce8-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c9ce8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9ce8-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c9ce8-120">Protocol specifications</span></span>

<span data-ttu-id="c9ce8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9ce8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9ce8-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9ce8-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9ce8-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9ce8-124">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9ce8-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c9ce8-125">Header files</span></span>

<span data-ttu-id="c9ce8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9ce8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9ce8-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9ce8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9ce8-128">See also</span></span>



[<span data-ttu-id="c9ce8-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9ce8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9ce8-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ce8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9ce8-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c9ce8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9ce8-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c9ce8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

