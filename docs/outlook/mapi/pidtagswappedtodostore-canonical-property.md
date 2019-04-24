---
title: Kanonische Pidtagswappedtodostore (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358905"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="e9c44-103">Kanonische Pidtagswappedtodostore (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9c44-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="e9c44-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9c44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9c44-105">Bestimmt die Notwendigkeit für die Post-Transmit-Verarbeitung einer e-Mail.</span><span class="sxs-lookup"><span data-stu-id="e9c44-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9c44-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e9c44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9c44-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="e9c44-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="e9c44-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e9c44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9c44-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="e9c44-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="e9c44-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e9c44-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9c44-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9c44-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9c44-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e9c44-112">Area:</span></span>  <br/> |<span data-ttu-id="e9c44-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="e9c44-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9c44-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9c44-114">Remarks</span></span>

<span data-ttu-id="e9c44-115">Wenn diese Eigenschaft für eine Entwurfsnachricht festgelegt ist, muss der Wert auf den Wert der **PR_STORE_ENTRYID** ([pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))-Eigenschaft der Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9c44-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="e9c44-116">Weitere Informationen finden Sie im Abschnitt [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) "nach der Übertragung der Verarbeitung einer gekennzeichneten Nachricht".</span><span class="sxs-lookup"><span data-stu-id="e9c44-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9c44-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e9c44-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9c44-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e9c44-118">Protocol specifications</span></span>

<span data-ttu-id="e9c44-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9c44-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9c44-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e9c44-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9c44-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9c44-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9c44-122">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="e9c44-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="e9c44-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9c44-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9c44-124">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="e9c44-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9c44-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e9c44-125">Header files</span></span>

<span data-ttu-id="e9c44-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e9c44-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9c44-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e9c44-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9c44-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e9c44-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e9c44-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e9c44-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9c44-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9c44-130">See also</span></span>



[<span data-ttu-id="e9c44-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9c44-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9c44-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9c44-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9c44-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e9c44-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9c44-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e9c44-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

