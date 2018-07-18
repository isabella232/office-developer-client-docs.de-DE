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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01a65306e5e0d34ed6f1ce7231227224868ff5cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795208"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="ea514-103">PidTagStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ea514-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ea514-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea514-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea514-105">Enthält eine 32-Bit-Bitmaske aus Flags, die Ordner Status definieren.</span><span class="sxs-lookup"><span data-stu-id="ea514-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea514-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ea514-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea514-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="ea514-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="ea514-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ea514-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea514-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="ea514-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="ea514-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ea514-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea514-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea514-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea514-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ea514-112">Area:</span></span>  <br/> |<span data-ttu-id="ea514-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="ea514-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea514-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea514-114">Remarks</span></span>

<span data-ttu-id="ea514-115">Diese Eigenschaft für Ordner entspricht der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft für Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ea514-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="ea514-116">Ihre Flags werden für die Client-Anwendung bereitgestellt und wirken sich nicht auf den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="ea514-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="ea514-117">Clients verwenden oder ignorieren diese Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ea514-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="ea514-118">Der Client kann auch eine eigene Werte für die Client-definierbare Bit dieser Eigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="ea514-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="ea514-119">Für die Bitmaske kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ea514-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="ea514-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="ea514-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="ea514-121">Der Ordner ist zum Löschen gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ea514-121">The folder is marked for deletion.</span></span> <span data-ttu-id="ea514-122">Die Client-Anwendung wird dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="ea514-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="ea514-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="ea514-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="ea514-124">Der Ordner ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="ea514-124">The folder is hidden.</span></span>
    
<span data-ttu-id="ea514-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="ea514-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="ea514-126">Der Ordner ist, beispielsweise markiert in umgekehrter Reihenfolge video dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ea514-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="ea514-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="ea514-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="ea514-128">Der Ordner gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="ea514-128">The folder is tagged.</span></span>
    
<span data-ttu-id="ea514-129">Nachricht Anbieter legen Sie diese Eigenschaft auf einen Ordner auf eine oder mehrere der folgenden Werte und Clients Interpretieren des Status nach Bedarf für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ea514-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="ea514-130">Angenommen, können ein Client den Ordner Status Sie hervorheben zwischen Ordnern in einer Hierarchietabelle, Anzeigen von Ordnern mit dem gleichen Status auf die gleiche Weise verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea514-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="ea514-131">Markierten Ordner in umgekehrter video, markierte Ordner angezeigt werden können und Ordnern zum Löschen markiert mit einem aussagekräftigen Symbol angezeigt werden können und verborgene Ordner verborgen werden können.</span><span class="sxs-lookup"><span data-stu-id="ea514-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="ea514-132">Bits 16 bis 31 ("0 x 10000" durch "0 x 80000000") dieser Eigenschaft stehen für die Verwendung durch die IPM-Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="ea514-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="ea514-133">Alle anderen Bits sind MAPI für die Verwendung reserviert. die nicht in der obigen Liste definierten sollte anfänglich auf 0 (null) festgelegt und nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ea514-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea514-134">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea514-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea514-135">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ea514-135">Protocol specifications</span></span>

<span data-ttu-id="ea514-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea514-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea514-137">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ea514-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea514-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea514-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea514-139">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="ea514-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea514-140">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ea514-140">Header files</span></span>

<span data-ttu-id="ea514-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea514-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea514-142">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ea514-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea514-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea514-143">Mapitags.h</span></span>
  
> <span data-ttu-id="ea514-144">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ea514-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea514-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea514-145">See also</span></span>



[<span data-ttu-id="ea514-146">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea514-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea514-147">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea514-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea514-148">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ea514-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea514-149">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ea514-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

