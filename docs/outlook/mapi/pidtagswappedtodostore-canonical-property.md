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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358905"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="df964-103">PidTagSwappedToDoStore (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df964-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="df964-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df964-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df964-105">Bestimmt die Notwendigkeit der Verarbeitung einer E-Mail nach der Übertragung.</span><span class="sxs-lookup"><span data-stu-id="df964-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df964-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="df964-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df964-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="df964-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="df964-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="df964-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df964-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="df964-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="df964-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="df964-110">Data type:</span></span>  <br/> |<span data-ttu-id="df964-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df964-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df964-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="df964-112">Area:</span></span>  <br/> |<span data-ttu-id="df964-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="df964-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df964-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df964-114">Remarks</span></span>

<span data-ttu-id="df964-115">Wenn diese Eigenschaft für eine Entwurfsnachricht festgelegt ist, muss ihr Wert auf den Wert der **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) -Eigenschaft der Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df964-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="df964-116">Weitere Informationen finden Sie [im Abschnitt [MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) "Post-Transmit Processing of a Flagged Message".</span><span class="sxs-lookup"><span data-stu-id="df964-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df964-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df964-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df964-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="df964-118">Protocol specifications</span></span>

<span data-ttu-id="df964-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df964-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df964-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="df964-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df964-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df964-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df964-122">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="df964-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="df964-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df964-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df964-124">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="df964-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df964-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="df964-125">Header files</span></span>

<span data-ttu-id="df964-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df964-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="df964-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="df964-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="df964-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df964-128">Mapitags.h</span></span>
  
> <span data-ttu-id="df964-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="df964-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df964-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df964-130">See also</span></span>



[<span data-ttu-id="df964-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df964-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df964-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="df964-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df964-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="df964-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df964-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="df964-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

