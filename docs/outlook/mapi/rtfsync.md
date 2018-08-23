---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 706c628241e519642209a271dce62d21b16938e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565739"
---
# <a name="rtfsync"></a><span data-ttu-id="5242d-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="5242d-103">RTFSync</span></span>

<span data-ttu-id="5242d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5242d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5242d-105">Stellt sicher, dass der Nachrichtentext Rich Text Format (RTF), die nur-Text-Version übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5242d-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="5242d-106">Es ist erforderlich, das diesen Funktionsaufruf vor dem Lesen der RTF-Version und nach dem Ändern der RTF-Version.</span><span class="sxs-lookup"><span data-stu-id="5242d-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5242d-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5242d-107">Header file:</span></span>  <br/> |<span data-ttu-id="5242d-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5242d-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5242d-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5242d-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5242d-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5242d-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5242d-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5242d-111">Called by:</span></span>  <br/> |<span data-ttu-id="5242d-112">RTF-fähigen Clientanwendungen und Nachricht speichern-Anbieter</span><span class="sxs-lookup"><span data-stu-id="5242d-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="5242d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5242d-113">Parameters</span></span>

<span data-ttu-id="5242d-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5242d-114">_lpMessage_</span></span>
  
> <span data-ttu-id="5242d-115">[in] Zeiger auf die Nachricht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5242d-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="5242d-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5242d-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5242d-117">[in] Bitmaske aus Flags verwendet, um anzugeben, die RTF oder nur-Text-Version der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5242d-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="5242d-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5242d-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="5242d-119">RTF_SYNC_BODY_CHANGED: Die Textversion der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5242d-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="5242d-120">RTF_SYNC_RTF_CHANGED: Die RTF-Version der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5242d-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="5242d-121">Alle anderen Bits im _UlFlags_ -Parameter sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5242d-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="5242d-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="5242d-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="5242d-123">[out] Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5242d-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="5242d-124">True, wenn es eine aktualisierte Meldung, sonst FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="5242d-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5242d-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5242d-125">Return value</span></span>

<span data-ttu-id="5242d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="5242d-126">S_OK</span></span> 
  
> <span data-ttu-id="5242d-127">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5242d-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5242d-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5242d-128">Remarks</span></span>

<span data-ttu-id="5242d-129">Wenn die Eigenschaft **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) fehlt oder ist FALSE, bevor Sie mit der RTF_SYNC_BODY_ Lesen der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) die **RTFSync** -Funktion aufgerufen werden soll -Kennzeichens geändert.</span><span class="sxs-lookup"><span data-stu-id="5242d-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="5242d-130">Wenn das Flag STORE_RTF_OK in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft nicht festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED-Flag festlegen, nach dem Ändern der **PR_RTF_COMPRESSED**aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5242d-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="5242d-131">Wenn **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) und **PR_RTF_COMPRESSED** geändert haben, sollte die **RTFSync** -Funktion mit beiden Flags aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5242d-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="5242d-132">Wenn der Wert des Parameters _LpfMessageUpdated_ auf TRUE festgelegt ist, sollte die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode für die Nachricht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5242d-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="5242d-133">Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5242d-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="5242d-134">**RTFSync** können Nachricht-Anbieter die Eigenschaften **PR_BODY** und **PR_RTF_COMPRESSED** synchronisiert halten.</span><span class="sxs-lookup"><span data-stu-id="5242d-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="5242d-135">Weitere Informationen finden Sie unter [Unterstützung von RTF-Text für die Nachricht-Anbieter](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="5242d-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5242d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5242d-136">See also</span></span>

- [<span data-ttu-id="5242d-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="5242d-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

