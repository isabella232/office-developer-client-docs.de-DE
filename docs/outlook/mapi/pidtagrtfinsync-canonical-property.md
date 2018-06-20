---
title: Kanonische PidTagRtfInSync-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795016"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="6cee4-103">Kanonische PidTagRtfInSync-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6cee4-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="6cee4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6cee4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6cee4-105">Enthält True, wenn die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft auf denselben Textinhalt wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft für diese Nachricht verfügt.</span><span class="sxs-lookup"><span data-stu-id="6cee4-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6cee4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6cee4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cee4-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="6cee4-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="6cee4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6cee4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6cee4-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="6cee4-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="6cee4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6cee4-110">Data type:</span></span>  <br/> |<span data-ttu-id="6cee4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6cee4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6cee4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6cee4-112">Area:</span></span>  <br/> |<span data-ttu-id="6cee4-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="6cee4-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cee4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6cee4-114">Remarks</span></span>

<span data-ttu-id="6cee4-115">Der Wert "true" bedeutet, denen die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, die nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die Version von Rich Text Format (RTF), mit Ausnahme von identisch sind Leerzeichen in **PR_BODY** und Formatierungen im **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="6cee4-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="6cee4-116">Der Text in den beiden Versionen umfasst die gleichen Zeichen in der gleichen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="6cee4-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="6cee4-117">Der Wert FALSE bedeutet, dass die beiden Versionen für Textinhalt nicht synchronisiert sind, jedoch werden von der Funktion [RTFSync](rtfsync.md) synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6cee4-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="6cee4-118">Eine Version geändert wurde und die andere Version hat nicht.</span><span class="sxs-lookup"><span data-stu-id="6cee4-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="6cee4-119">Kein Wert bedeutet, dass die beiden Versionen, wenn beide vorhanden sind oder jemals vorhanden waren, synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6cee4-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="6cee4-120">Eine Version wurde gelöscht oder geändert, sodass Produktivitätssteigerungen, dass die Synchronisierung nicht mehr möglich ist.</span><span class="sxs-lookup"><span data-stu-id="6cee4-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="6cee4-121">Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat sollte der Wert in dieser Eigenschaft zum Erzwingen der Synchronisierung FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6cee4-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="6cee4-122">RTF-fähigen Nachrichtenspeicher sollten die Synchronisierung mit **RTFSync** während eines Anrufs [IMAPIProp::SaveChanges](imapiprop-savechanges.md) durchführen.</span><span class="sxs-lookup"><span data-stu-id="6cee4-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="6cee4-123">RTF-fähigen Clients sollte die Einstellung von **PR_RTF_IN_SYNC** vor dem Lesen **PR_RTF_COMPRESSED**überprüfen, und rufen Sie **RTFSync** zuerst bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="6cee4-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="6cee4-124">Wenn **PR_BODY** Änderungen an einen anderen Wert als deren Leerraum wurde, muss der Nachrichtenspeicher **PR_RTF_IN_SYNC** , um die Synchronisierung zu beenden löschen.</span><span class="sxs-lookup"><span data-stu-id="6cee4-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6cee4-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6cee4-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cee4-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6cee4-126">Protocol specifications</span></span>

<span data-ttu-id="6cee4-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cee4-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cee4-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6cee4-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6cee4-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cee4-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cee4-130">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="6cee4-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cee4-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6cee4-131">Header files</span></span>

<span data-ttu-id="6cee4-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cee4-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cee4-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6cee4-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="6cee4-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6cee4-134">Mapitags.h</span></span>
  
> <span data-ttu-id="6cee4-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6cee4-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cee4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cee4-136">See also</span></span>



[<span data-ttu-id="6cee4-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cee4-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cee4-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cee4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cee4-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6cee4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cee4-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6cee4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
