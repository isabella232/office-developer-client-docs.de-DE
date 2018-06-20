---
title: Kanonische PidLidReminderSignalTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 375cde94d0ecd989908fccbdd69710c1961fba17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793752"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="bc1c2-103">Kanonische PidLidReminderSignalTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bc1c2-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="bc1c2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc1c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc1c2-105">Gibt die Position in der Zeit, wenn eine Erinnerung von ausstehenden in überfällige wechselt.</span><span class="sxs-lookup"><span data-stu-id="bc1c2-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc1c2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc1c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc1c2-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="bc1c2-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="bc1c2-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bc1c2-108">Property set:</span></span>  <br/> |<span data-ttu-id="bc1c2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bc1c2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bc1c2-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="bc1c2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bc1c2-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="bc1c2-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="bc1c2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc1c2-112">Data type:</span></span>  <br/> |<span data-ttu-id="bc1c2-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bc1c2-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bc1c2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc1c2-114">Area:</span></span>  <br/> |<span data-ttu-id="bc1c2-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="bc1c2-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc1c2-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc1c2-116">Remarks</span></span>

<span data-ttu-id="bc1c2-117">Diese Eigenschaft muss festgelegt werden, wenn die **DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bc1c2-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="bc1c2-118">Clients müssen der Wert in koordinierter Weltzeit (UTC) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bc1c2-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc1c2-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bc1c2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc1c2-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bc1c2-120">Protocol specifications</span></span>

<span data-ttu-id="bc1c2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc1c2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc1c2-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bc1c2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc1c2-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc1c2-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc1c2-124">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="bc1c2-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc1c2-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bc1c2-125">Header files</span></span>

<span data-ttu-id="bc1c2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc1c2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc1c2-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bc1c2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc1c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc1c2-128">See also</span></span>



[<span data-ttu-id="bc1c2-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc1c2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc1c2-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc1c2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc1c2-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc1c2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc1c2-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc1c2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

