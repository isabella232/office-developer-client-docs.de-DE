---
title: PidTagSubmitFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fb048d622aaf3cfa97f380e21324749d7421603e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563688"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="494be-103">PidTagSubmitFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="494be-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="494be-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="494be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="494be-105">Enthält eine Bitmaske aus Flags, die Details zu einer Nachrichtenübermittlung angibt.</span><span class="sxs-lookup"><span data-stu-id="494be-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="494be-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="494be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="494be-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="494be-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="494be-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="494be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="494be-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="494be-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="494be-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="494be-110">Data type:</span></span>  <br/> |<span data-ttu-id="494be-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="494be-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="494be-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="494be-112">Area:</span></span>  <br/> |<span data-ttu-id="494be-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="494be-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="494be-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="494be-114">Remarks</span></span>

<span data-ttu-id="494be-115">Für die Bitmaske **PR_SUBMIT_FLAGS** kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="494be-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="494be-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="494be-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="494be-117">Die MAPI-Warteschlange hat derzeit die Nachricht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="494be-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="494be-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="494be-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="494be-119">Die Meldung erforderlich vorverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="494be-119">The message needs preprocessing.</span></span> <span data-ttu-id="494be-120">Wenn die MAPI-Warteschlange erfolgt vorverarbeitung diese Meldung, sollten sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="494be-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="494be-121">Die Nachrichtenanbieter erkennt, dass die Warteschlange, statt die Clientanwendung **SubmitMessage**aufgerufen hat, das Flag löscht und weiterhin-Nachrichtenübermittlung.</span><span class="sxs-lookup"><span data-stu-id="494be-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="494be-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="494be-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="494be-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="494be-123">Protocol specifications</span></span>

<span data-ttu-id="494be-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494be-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494be-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="494be-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="494be-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494be-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494be-127">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="494be-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="494be-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="494be-128">Header files</span></span>

<span data-ttu-id="494be-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="494be-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="494be-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="494be-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="494be-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="494be-131">Mapitags.h</span></span>
  
> <span data-ttu-id="494be-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="494be-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="494be-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="494be-133">See also</span></span>



[<span data-ttu-id="494be-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="494be-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="494be-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="494be-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="494be-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="494be-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="494be-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="494be-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="494be-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="494be-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

