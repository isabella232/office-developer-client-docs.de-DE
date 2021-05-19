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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357876"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="36697-103">PidTagRtfInSync (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="36697-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="36697-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36697-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36697-105">Enthält **TRUE, wenn die PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) denselben Textinhalt wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft für diese Nachricht hat.</span><span class="sxs-lookup"><span data-stu-id="36697-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36697-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="36697-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36697-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="36697-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="36697-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="36697-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36697-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="36697-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="36697-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="36697-110">Data type:</span></span>  <br/> |<span data-ttu-id="36697-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="36697-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="36697-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="36697-112">Area:</span></span>  <br/> |<span data-ttu-id="36697-113">E-Mails</span><span class="sxs-lookup"><span data-stu-id="36697-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36697-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36697-114">Remarks</span></span>

<span data-ttu-id="36697-115">Der Wert TRUE bedeutet, dass die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, die Nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft, die Rich Text Format (RTF)-Version, mit Ausnahme von Leerzeichen in **PR_BODY** und Formatierung in **PR_RTF_COMPRESSED identisch sind.**</span><span class="sxs-lookup"><span data-stu-id="36697-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="36697-116">Der Text in den beiden Versionen besteht aus denselben Zeichen in derselben Sequenz.</span><span class="sxs-lookup"><span data-stu-id="36697-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="36697-117">Der Wert FALSE bedeutet, dass die beiden Versionen nicht für Textinhalte synchronisiert werden, sondern von der [RTFSync-Funktion synchronisiert werden](rtfsync.md) können.</span><span class="sxs-lookup"><span data-stu-id="36697-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="36697-118">Eine Version wurde geändert, die andere version nicht.</span><span class="sxs-lookup"><span data-stu-id="36697-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="36697-119">Kein Wert bedeutet, dass die beiden Versionen, sofern vorhanden oder jemals vorhanden, nicht synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="36697-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="36697-120">Eine Version wurde so radikal gelöscht oder geändert, dass eine Synchronisierung nicht mehr möglich ist.</span><span class="sxs-lookup"><span data-stu-id="36697-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="36697-121">Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat, sollte in dieser Eigenschaft den Wert FALSE festlegen, um die Synchronisierung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="36697-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="36697-122">RTF-benachrichtigungsspeicher sollten die Synchronisierung mithilfe von **RTFSync** während eines [IMAPIProp::SaveChanges-Aufrufs](imapiprop-savechanges.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="36697-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="36697-123">RTF- aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span><span class="sxs-lookup"><span data-stu-id="36697-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="36697-124">Wenn **PR_BODY** änderungen an einem anderen Leerzeichen als dem Leerzeichen vorgenommen haben, muss der Nachrichtenspeicher PR_RTF_IN_SYNC **löschen,** um die Synchronisierung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="36697-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="36697-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="36697-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36697-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="36697-126">Protocol specifications</span></span>

<span data-ttu-id="36697-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36697-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36697-128">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="36697-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="36697-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36697-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36697-130">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="36697-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36697-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="36697-131">Header files</span></span>

<span data-ttu-id="36697-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36697-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="36697-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="36697-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="36697-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="36697-134">Mapitags.h</span></span>
  
> <span data-ttu-id="36697-135">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="36697-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36697-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36697-136">See also</span></span>



[<span data-ttu-id="36697-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="36697-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36697-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="36697-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36697-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="36697-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36697-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="36697-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

