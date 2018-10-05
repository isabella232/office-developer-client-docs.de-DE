---
title: PidTagSwappedToDoStore (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393859"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="40607-103">PidTagSwappedToDoStore (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40607-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="40607-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40607-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40607-105">Bestimmt die Notwendigkeit für die Verarbeitung einer e-Mail nach dem übertragen.</span><span class="sxs-lookup"><span data-stu-id="40607-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40607-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="40607-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40607-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="40607-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="40607-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="40607-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40607-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="40607-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="40607-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="40607-110">Data type:</span></span>  <br/> |<span data-ttu-id="40607-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="40607-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="40607-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="40607-112">Area:</span></span>  <br/> |<span data-ttu-id="40607-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="40607-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40607-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40607-114">Remarks</span></span>

<span data-ttu-id="40607-115">Wenn diese Eigenschaft auf den Entwurf einer Nachricht festgelegt ist, muss der Wert auf den Wert der **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))-Eigenschaft der Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="40607-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="40607-116">Weitere Informationen finden Sie unter [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) im Abschnitt "nach dem Übertragen einer Nachricht Flagged verarbeiten."</span><span class="sxs-lookup"><span data-stu-id="40607-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="40607-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40607-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40607-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="40607-118">Protocol specifications</span></span>

<span data-ttu-id="40607-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40607-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40607-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="40607-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="40607-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40607-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40607-122">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="40607-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="40607-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40607-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40607-124">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="40607-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40607-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="40607-125">Header files</span></span>

<span data-ttu-id="40607-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40607-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="40607-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="40607-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="40607-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="40607-128">Mapitags.h</span></span>
  
> <span data-ttu-id="40607-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="40607-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40607-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40607-130">See also</span></span>



[<span data-ttu-id="40607-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40607-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40607-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40607-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40607-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="40607-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40607-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="40607-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

