---
title: PidTagStatus (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278792"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="2f370-103">PidTagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2f370-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="2f370-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f370-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f370-105">Enthält eine 32-Bit-Bitmaske mit Flags, die den Ordnerstatus definieren.</span><span class="sxs-lookup"><span data-stu-id="2f370-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f370-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2f370-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f370-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="2f370-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="2f370-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2f370-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2f370-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="2f370-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="2f370-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2f370-110">Data type:</span></span>  <br/> |<span data-ttu-id="2f370-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2f370-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2f370-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2f370-112">Area:</span></span>  <br/> |<span data-ttu-id="2f370-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="2f370-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f370-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2f370-114">Remarks</span></span>

<span data-ttu-id="2f370-115">Diese Eigenschaft für Ordner entspricht der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft für Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2f370-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="2f370-116">Die Flags werden nur für die Clientanwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher aus.</span><span class="sxs-lookup"><span data-stu-id="2f370-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="2f370-117">Clients können diese Einstellungen verwenden oder ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2f370-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="2f370-118">Der Client kann auch eigene Werte für die clientdefinierbaren Bits dieser Eigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="2f370-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="2f370-119">Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2f370-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="2f370-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="2f370-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="2f370-121">Der Ordner wird zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="2f370-121">The folder is marked for deletion.</span></span> <span data-ttu-id="2f370-122">Die Clientanwendung legt dieses Flag fest.</span><span class="sxs-lookup"><span data-stu-id="2f370-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="2f370-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="2f370-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="2f370-124">Der Ordner ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2f370-124">The folder is hidden.</span></span>
    
<span data-ttu-id="2f370-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="2f370-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="2f370-126">Der Ordner wird z. B. im Umgekehrten Video hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="2f370-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="2f370-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="2f370-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="2f370-128">Der Ordner ist markiert.</span><span class="sxs-lookup"><span data-stu-id="2f370-128">The folder is tagged.</span></span>
    
<span data-ttu-id="2f370-129">Nachrichtenspeicheranbieter legen diese Eigenschaft für einen Ordner auf einen oder mehrere dieser Werte festgelegt, und Clients interpretieren den Status entsprechend ihren Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2f370-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="2f370-130">Ein Client kann z. B. den Ordnerstatus verwenden, um visuell zwischen Ordnern in einer Hierarchietabelle zu unterscheiden, und Ordner mit demselben Status auf die gleiche Weise anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2f370-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="2f370-131">Hervorgehobene Ordner können im Reversevideo angezeigt werden, markierte Ordner und Ordner, die zum Löschen markiert sind, können mit einem aussagekräftigen Symbol angezeigt werden, und ausgeblendete Ordner können ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f370-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="2f370-132">Bits 16 bis 31 ("0x10000" bis "0x80000000") dieser Eigenschaft stehen für die Verwendung durch die IPM-Clientanwendung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2f370-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="2f370-133">Alle anderen Bits sind für die Verwendung durch MAPI reserviert. Diejenigen, die in der vorherigen Liste nicht definiert sind, sollten zunächst auf Null festgelegt und nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2f370-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f370-134">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2f370-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f370-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2f370-135">Protocol specifications</span></span>

<span data-ttu-id="2f370-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f370-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f370-137">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2f370-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f370-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f370-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f370-139">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="2f370-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f370-140">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2f370-140">Header files</span></span>

<span data-ttu-id="2f370-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f370-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f370-142">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2f370-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="2f370-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2f370-143">Mapitags.h</span></span>
  
> <span data-ttu-id="2f370-144">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2f370-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f370-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f370-145">See also</span></span>



[<span data-ttu-id="2f370-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f370-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f370-147">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2f370-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f370-148">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2f370-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f370-149">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2f370-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

