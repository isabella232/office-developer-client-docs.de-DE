---
title: Kanonische PidTagSubmitFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795238"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="0a9ee-103">Kanonische PidTagSubmitFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0a9ee-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="0a9ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a9ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a9ee-105">Enthält eine Bitmaske aus Flags, die Details zu einer Nachrichtenübermittlung angibt.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a9ee-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0a9ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a9ee-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0a9ee-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="0a9ee-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="0a9ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a9ee-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="0a9ee-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="0a9ee-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0a9ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a9ee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0a9ee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0a9ee-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0a9ee-112">Area:</span></span>  <br/> |<span data-ttu-id="0a9ee-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="0a9ee-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a9ee-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a9ee-114">Remarks</span></span>

<span data-ttu-id="0a9ee-115">Für die Bitmaske **PR_SUBMIT_FLAGS** kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0a9ee-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="0a9ee-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="0a9ee-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="0a9ee-117">Die MAPI-Warteschlange hat derzeit die Nachricht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="0a9ee-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="0a9ee-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="0a9ee-119">Die Meldung erforderlich vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-119">The message needs preprocessing.</span></span> <span data-ttu-id="0a9ee-120">Wenn die MAPI-Warteschlange erfolgt vorverarbeitung diese Meldung, sollten sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="0a9ee-121">Die Nachrichtenanbieter erkennt, dass die Warteschlange, statt die Clientanwendung **SubmitMessage**aufgerufen hat, das Flag löscht und weiterhin-Nachrichtenübermittlung.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="0a9ee-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a9ee-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a9ee-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0a9ee-123">Protocol specifications</span></span>

<span data-ttu-id="0a9ee-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a9ee-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a9ee-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a9ee-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a9ee-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a9ee-127">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a9ee-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0a9ee-128">Header files</span></span>

<span data-ttu-id="0a9ee-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a9ee-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a9ee-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a9ee-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a9ee-131">Mapitags.h</span></span>
  
> <span data-ttu-id="0a9ee-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0a9ee-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a9ee-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a9ee-133">See also</span></span>



[<span data-ttu-id="0a9ee-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="0a9ee-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="0a9ee-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a9ee-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a9ee-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a9ee-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a9ee-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0a9ee-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a9ee-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0a9ee-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

