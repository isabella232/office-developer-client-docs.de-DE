---
title: PidTagRtfInSync (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383058"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="14fe1-103">PidTagRtfInSync (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="14fe1-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="14fe1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14fe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14fe1-105">Enthält True, wenn die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft auf denselben Textinhalt wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft für diese Nachricht verfügt.</span><span class="sxs-lookup"><span data-stu-id="14fe1-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14fe1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="14fe1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14fe1-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="14fe1-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="14fe1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="14fe1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14fe1-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="14fe1-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="14fe1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="14fe1-110">Data type:</span></span>  <br/> |<span data-ttu-id="14fe1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="14fe1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="14fe1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="14fe1-112">Area:</span></span>  <br/> |<span data-ttu-id="14fe1-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="14fe1-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14fe1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14fe1-114">Remarks</span></span>

<span data-ttu-id="14fe1-115">Der Wert "true" bedeutet, denen die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, die nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die Version von Rich Text Format (RTF), mit Ausnahme von identisch sind Leerzeichen in **PR_BODY** und Formatierungen im **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="14fe1-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="14fe1-116">Der Text in den beiden Versionen umfasst die gleichen Zeichen in der gleichen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="14fe1-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="14fe1-117">Der Wert FALSE bedeutet, dass die beiden Versionen für Textinhalt nicht synchronisiert sind, jedoch werden von der Funktion [RTFSync](rtfsync.md) synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="14fe1-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="14fe1-118">Eine Version geändert wurde und die andere Version hat nicht.</span><span class="sxs-lookup"><span data-stu-id="14fe1-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="14fe1-119">Kein Wert bedeutet, dass die beiden Versionen, wenn beide vorhanden sind oder jemals vorhanden waren, synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="14fe1-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="14fe1-120">Eine Version wurde gelöscht oder geändert, sodass Produktivitätssteigerungen, dass die Synchronisierung nicht mehr möglich ist.</span><span class="sxs-lookup"><span data-stu-id="14fe1-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="14fe1-121">Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat sollte der Wert in dieser Eigenschaft zum Erzwingen der Synchronisierung FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="14fe1-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="14fe1-122">RTF-fähigen Nachrichtenspeicher sollten die Synchronisierung mit **RTFSync** während eines Anrufs [IMAPIProp::SaveChanges](imapiprop-savechanges.md) durchführen.</span><span class="sxs-lookup"><span data-stu-id="14fe1-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="14fe1-123">RTF-fähigen Clients sollte die Einstellung von **PR_RTF_IN_SYNC** vor dem Lesen **PR_RTF_COMPRESSED**überprüfen, und rufen Sie **RTFSync** zuerst bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="14fe1-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="14fe1-124">Wenn **PR_BODY** Änderungen an einen anderen Wert als deren Leerraum wurde, muss der Nachrichtenspeicher **PR_RTF_IN_SYNC** , um die Synchronisierung zu beenden löschen.</span><span class="sxs-lookup"><span data-stu-id="14fe1-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="14fe1-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="14fe1-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14fe1-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="14fe1-126">Protocol specifications</span></span>

<span data-ttu-id="14fe1-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14fe1-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14fe1-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="14fe1-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14fe1-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14fe1-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14fe1-130">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="14fe1-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14fe1-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="14fe1-131">Header files</span></span>

<span data-ttu-id="14fe1-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14fe1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="14fe1-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="14fe1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="14fe1-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14fe1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="14fe1-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="14fe1-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14fe1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14fe1-136">See also</span></span>



[<span data-ttu-id="14fe1-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14fe1-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14fe1-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14fe1-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14fe1-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="14fe1-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14fe1-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="14fe1-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

