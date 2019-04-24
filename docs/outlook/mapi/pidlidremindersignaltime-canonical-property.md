---
title: Kanonische Pidlidremindersignaltime (-Eigenschaft
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
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350855"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="a12d7-103">Kanonische Pidlidremindersignaltime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a12d7-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="a12d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a12d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a12d7-105">Gibt den Zeitpunkt an, zu dem eine Erinnerung von Ausstehend zu überfällig wechselt.</span><span class="sxs-lookup"><span data-stu-id="a12d7-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a12d7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a12d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a12d7-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="a12d7-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="a12d7-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="a12d7-108">Property set:</span></span>  <br/> |<span data-ttu-id="a12d7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a12d7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a12d7-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="a12d7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a12d7-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="a12d7-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="a12d7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a12d7-112">Data type:</span></span>  <br/> |<span data-ttu-id="a12d7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a12d7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a12d7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a12d7-114">Area:</span></span>  <br/> |<span data-ttu-id="a12d7-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="a12d7-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a12d7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a12d7-116">Remarks</span></span>

<span data-ttu-id="a12d7-117">Diese Eigenschaft muss festgelegt werden, wenn die **dispidReminderSet** ([pidlidreminderset (](pidlidreminderset-canonical-property.md))-Eigenschaft true ist.</span><span class="sxs-lookup"><span data-stu-id="a12d7-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="a12d7-118">Clients müssen den Wert in koordinierter weltZeit (UTC) festlegen.</span><span class="sxs-lookup"><span data-stu-id="a12d7-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a12d7-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a12d7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a12d7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a12d7-120">Protocol specifications</span></span>

<span data-ttu-id="a12d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a12d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a12d7-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="a12d7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a12d7-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a12d7-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a12d7-124">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="a12d7-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a12d7-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a12d7-125">Header files</span></span>

<span data-ttu-id="a12d7-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a12d7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a12d7-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a12d7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a12d7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a12d7-128">See also</span></span>



[<span data-ttu-id="a12d7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a12d7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a12d7-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a12d7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a12d7-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a12d7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a12d7-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a12d7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

