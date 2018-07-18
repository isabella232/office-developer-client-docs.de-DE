---
title: PidLidReminderFileParameter (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderFileParameter
api_type:
- COM
ms.assetid: 1009f0ea-6f35-484d-b04d-5b6e844c14dd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1cfb8f7070a8001e94fa70e90c52635c9b8be122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793745"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="63862-103">PidLidReminderFileParameter (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="63862-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="63862-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63862-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63862-105">Gibt den Dateinamen des Sounds, die ein Client wiedergegeben werden soll, wenn die Erinnerung für dieses Objekt überfällig wird.</span><span class="sxs-lookup"><span data-stu-id="63862-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63862-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="63862-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63862-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="63862-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="63862-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="63862-108">Property set:</span></span>  <br/> |<span data-ttu-id="63862-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="63862-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="63862-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="63862-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63862-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="63862-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="63862-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="63862-112">Data type:</span></span>  <br/> |<span data-ttu-id="63862-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63862-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="63862-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="63862-114">Area:</span></span>  <br/> |<span data-ttu-id="63862-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="63862-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63862-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63862-116">Remarks</span></span>

<span data-ttu-id="63862-117">Wenn diese Eigenschaft nicht vorhanden ist, kann der Client einen Standardwert verwenden.</span><span class="sxs-lookup"><span data-stu-id="63862-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63862-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="63862-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63862-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="63862-119">Protocol specifications</span></span>

<span data-ttu-id="63862-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63862-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63862-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="63862-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63862-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63862-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63862-123">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="63862-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63862-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="63862-124">Header files</span></span>

<span data-ttu-id="63862-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63862-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="63862-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="63862-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63862-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63862-127">See also</span></span>



[<span data-ttu-id="63862-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="63862-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63862-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="63862-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63862-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="63862-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63862-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="63862-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

