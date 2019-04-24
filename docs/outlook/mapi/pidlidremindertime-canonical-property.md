---
title: Kanonische Pidlidremindertime (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358709"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="9d40a-103">Kanonische Pidlidremindertime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9d40a-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="9d40a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d40a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d40a-105">Gibt die anfängliche Signal Zeit für eine Erinnerung an.</span><span class="sxs-lookup"><span data-stu-id="9d40a-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d40a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9d40a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d40a-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="9d40a-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="9d40a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="9d40a-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d40a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9d40a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9d40a-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="9d40a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d40a-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="9d40a-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="9d40a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9d40a-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d40a-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9d40a-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9d40a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9d40a-114">Area:</span></span>  <br/> |<span data-ttu-id="9d40a-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="9d40a-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d40a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d40a-116">Remarks</span></span>

<span data-ttu-id="9d40a-117">Bei Calendar-Objekten stellt diese Eigenschaft die Uhrzeit dar, zu der der Benutzer zu spät kommt, wobei es sich um die Startzeit des Termins handelt.</span><span class="sxs-lookup"><span data-stu-id="9d40a-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="9d40a-118">Clients müssen den Wert in koordinierter weltZeit (UTC) festlegen.</span><span class="sxs-lookup"><span data-stu-id="9d40a-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9d40a-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d40a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d40a-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9d40a-120">Protocol specifications</span></span>

<span data-ttu-id="9d40a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d40a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d40a-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="9d40a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d40a-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d40a-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d40a-124">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="9d40a-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d40a-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9d40a-125">Header files</span></span>

<span data-ttu-id="9d40a-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9d40a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d40a-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9d40a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d40a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d40a-128">See also</span></span>



[<span data-ttu-id="9d40a-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d40a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d40a-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d40a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d40a-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9d40a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d40a-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9d40a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

