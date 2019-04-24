---
title: Kanonische Pidtagstatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278792"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="dcbc1-103">Kanonische Pidtagstatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dcbc1-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="dcbc1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcbc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcbc1-105">Enthält eine 32-Bit-Bitmaske von Flags, die den Ordner Status definieren.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcbc1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dcbc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcbc1-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="dcbc1-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="dcbc1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="dcbc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dcbc1-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="dcbc1-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="dcbc1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dcbc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="dcbc1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dcbc1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dcbc1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dcbc1-112">Area:</span></span>  <br/> |<span data-ttu-id="dcbc1-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="dcbc1-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcbc1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcbc1-114">Remarks</span></span>

<span data-ttu-id="dcbc1-115">Diese Eigenschaft für Ordner ist analog zur **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft für Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="dcbc1-116">Die zugehörigen Flags werden nur für die Clientanwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher aus.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="dcbc1-117">Diese Einstellungen können von Clients verwendet oder ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="dcbc1-118">Der Client kann auch eigene Werte für die vom Client definierbaren Bits dieser Eigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="dcbc1-119">Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dcbc1-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="dcbc1-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="dcbc1-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="dcbc1-121">Der Ordner ist zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-121">The folder is marked for deletion.</span></span> <span data-ttu-id="dcbc1-122">Die Clientanwendung legt dieses Flag fest.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="dcbc1-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="dcbc1-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="dcbc1-124">Der Ordner ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-124">The folder is hidden.</span></span>
    
<span data-ttu-id="dcbc1-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="dcbc1-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="dcbc1-126">Der Ordner wird beispielsweise in "Reverse Video" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="dcbc1-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="dcbc1-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="dcbc1-128">Der Ordner ist markiert.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-128">The folder is tagged.</span></span>
    
<span data-ttu-id="dcbc1-129">Nachrichtenspeicher Anbieter legen diese Eigenschaft für einen Ordner auf einen oder mehrere dieser Werte fest, und die Clients interpretieren den Status entsprechend Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="dcbc1-130">Beispielsweise kann ein Client den Ordner Status verwenden, um zwischen Ordnern in einer Hierarchietabelle visuell zu unterscheiden, sodass Ordner mit demselben Status auf die gleiche Weise angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="dcbc1-131">Hervorgehobene Ordner können in umgekehrtem Video angezeigt werden, markierte Ordner und zum Löschen markierte Ordner können mit einem sinnvollen Symbol angezeigt werden, und versteckte Ordner können verborgen werden.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="dcbc1-132">Die Bits 16 bis 31 ("0x10000" bis "0x80000000") dieser Eigenschaft stehen für die IPM-Clientanwendung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="dcbc1-133">Alle anderen Bits sind für die Verwendung durch MAPI reserviert; diejenigen, die nicht in der obigen Liste definiert sind, sollten anfänglich auf NULL festgelegt und nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dcbc1-134">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dcbc1-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcbc1-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dcbc1-135">Protocol specifications</span></span>

<span data-ttu-id="dcbc1-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcbc1-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcbc1-137">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcbc1-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcbc1-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcbc1-139">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcbc1-140">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="dcbc1-140">Header files</span></span>

<span data-ttu-id="dcbc1-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dcbc1-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcbc1-142">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="dcbc1-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="dcbc1-143">Mapitags.h</span></span>
  
> <span data-ttu-id="dcbc1-144">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="dcbc1-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcbc1-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcbc1-145">See also</span></span>



[<span data-ttu-id="dcbc1-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcbc1-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcbc1-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcbc1-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcbc1-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dcbc1-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcbc1-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dcbc1-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

