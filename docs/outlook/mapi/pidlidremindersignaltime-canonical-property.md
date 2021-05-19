---
title: PidLidReminderSignalTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350855"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="34b6d-103">PidLidReminderSignalTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="34b6d-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="34b6d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34b6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34b6d-105">Gibt den Zeitpunkt an, zu dem eine Erinnerung von ausstehend zu überfällig überfällig wird.</span><span class="sxs-lookup"><span data-stu-id="34b6d-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34b6d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="34b6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34b6d-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="34b6d-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="34b6d-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="34b6d-108">Property set:</span></span>  <br/> |<span data-ttu-id="34b6d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="34b6d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="34b6d-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="34b6d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="34b6d-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="34b6d-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="34b6d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="34b6d-112">Data type:</span></span>  <br/> |<span data-ttu-id="34b6d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="34b6d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="34b6d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="34b6d-114">Area:</span></span>  <br/> |<span data-ttu-id="34b6d-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="34b6d-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34b6d-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34b6d-116">Remarks</span></span>

<span data-ttu-id="34b6d-117">Diese Eigenschaft muss festgelegt werden, wenn **die eigenschaft dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) TRUE ist.</span><span class="sxs-lookup"><span data-stu-id="34b6d-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="34b6d-118">Clients müssen den Wert in koordinierter Weltzeit (Coordinated Universal Time, UTC) festlegen.</span><span class="sxs-lookup"><span data-stu-id="34b6d-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="34b6d-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34b6d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34b6d-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="34b6d-120">Protocol specifications</span></span>

<span data-ttu-id="34b6d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34b6d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34b6d-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="34b6d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34b6d-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34b6d-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34b6d-124">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="34b6d-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34b6d-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="34b6d-125">Header files</span></span>

<span data-ttu-id="34b6d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34b6d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="34b6d-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="34b6d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34b6d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34b6d-128">See also</span></span>



[<span data-ttu-id="34b6d-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34b6d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34b6d-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="34b6d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34b6d-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="34b6d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34b6d-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="34b6d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

