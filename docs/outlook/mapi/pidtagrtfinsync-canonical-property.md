---
title: Kanonische Pidtagrtfinsync (-Eigenschaft
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
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357876"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="fedd3-103">Kanonische Pidtagrtfinsync (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fedd3-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="fedd3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fedd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fedd3-105">Enthält TRUE, wenn die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft denselben Textinhalt hat wie die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fedd3-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fedd3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fedd3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fedd3-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="fedd3-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="fedd3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fedd3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fedd3-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="fedd3-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="fedd3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fedd3-110">Data type:</span></span>  <br/> |<span data-ttu-id="fedd3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fedd3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fedd3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fedd3-112">Area:</span></span>  <br/> |<span data-ttu-id="fedd3-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="fedd3-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fedd3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fedd3-114">Remarks</span></span>

<span data-ttu-id="fedd3-115">Der Wert TRUE gibt an, dass die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft, die nur-Text-Version dieser Nachricht und die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft, die RTF-Version (Rich Text Format), mit Ausnahme von Leerraum in **PR_BODY** und Formatierung in **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="fedd3-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="fedd3-116">Der Text in den beiden Versionen besteht aus denselben Zeichen in derselben Sequenz.</span><span class="sxs-lookup"><span data-stu-id="fedd3-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="fedd3-117">Der Wert FALSE gibt an, dass die beiden Versionen nicht für Textinhalte synchronisiert werden, aber von der [RTFSync](rtfsync.md) -Funktion synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="fedd3-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="fedd3-118">Eine Version wurde geändert, und die andere Version hat keine.</span><span class="sxs-lookup"><span data-stu-id="fedd3-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="fedd3-119">Kein Wert besagt, dass die beiden Versionen, wenn beide vorhanden oder jemals vorhanden waren, nicht synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="fedd3-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="fedd3-120">Eine Version wurde so radikal gelöscht oder geändert, dass eine Synchronisierung nicht mehr möglich ist.</span><span class="sxs-lookup"><span data-stu-id="fedd3-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="fedd3-121">Eine Clientanwendung, die **PR_RTF_COMPRESSED** geändert hat, sollte in dieser Eigenschaft den Wert false festlegen, um die Synchronisierung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="fedd3-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="fedd3-122">RTF-fähige Nachrichtenspeicher sollten die Synchronisierung mit **RTFSync** während eines Aufrufs von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="fedd3-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="fedd3-123">RTF-fähige Clients sollten die Einstellung von **PR_RTF_IN_SYNC** vor dem Lesen von **PR_RTF_COMPRESSED**überprüfen und **RTFSync** bei Bedarf zuerst aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fedd3-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="fedd3-124">Wenn **PR_BODY** Änderungen an einem anderen als dem Leerraum vorgenommen hat, muss der Nachrichtenspeicher **PR_RTF_IN_SYNC** löschen, um die Synchronisierung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="fedd3-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fedd3-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fedd3-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fedd3-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fedd3-126">Protocol specifications</span></span>

<span data-ttu-id="fedd3-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fedd3-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fedd3-128">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fedd3-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fedd3-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fedd3-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fedd3-130">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="fedd3-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fedd3-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="fedd3-131">Header files</span></span>

<span data-ttu-id="fedd3-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fedd3-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="fedd3-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="fedd3-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="fedd3-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fedd3-134">Mapitags.h</span></span>
  
> <span data-ttu-id="fedd3-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fedd3-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fedd3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fedd3-136">See also</span></span>



[<span data-ttu-id="fedd3-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fedd3-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fedd3-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fedd3-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fedd3-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fedd3-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fedd3-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fedd3-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

