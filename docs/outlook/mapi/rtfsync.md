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
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436209"
---
# <a name="rtfsync"></a><span data-ttu-id="91daa-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="91daa-103">RTFSync</span></span>

<span data-ttu-id="91daa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91daa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91daa-105">Stellt sicher, dass der Rich Text Format (RTF)-Nachrichtentext der Nur-Text-Version entspricht.</span><span class="sxs-lookup"><span data-stu-id="91daa-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="91daa-106">Sie müssen diese Funktion aufrufen, bevor Sie die RTF-Version lesen und die RTF-Version ändern.</span><span class="sxs-lookup"><span data-stu-id="91daa-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91daa-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="91daa-107">Header file:</span></span>  <br/> |<span data-ttu-id="91daa-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="91daa-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="91daa-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="91daa-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="91daa-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="91daa-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="91daa-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="91daa-111">Called by:</span></span>  <br/> |<span data-ttu-id="91daa-112">RTF-bewusste Clientanwendungen und Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="91daa-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="91daa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="91daa-113">Parameters</span></span>

<span data-ttu-id="91daa-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="91daa-114">_lpMessage_</span></span>
  
> <span data-ttu-id="91daa-115">[in] Zeiger auf die zu aktualisierende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91daa-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="91daa-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91daa-116">_ulFlags_</span></span>
  
> <span data-ttu-id="91daa-117">[in] Bitmaske von Flags, die verwendet werden, um die RTF- oder Nur-Text-Version der Nachricht anzugeben, hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="91daa-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="91daa-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="91daa-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="91daa-119">RTF_SYNC_BODY_CHANGED: Die Nur-Text-Version der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="91daa-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="91daa-120">RTF_SYNC_RTF_CHANGED: Die RTF-Version der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="91daa-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="91daa-121">Alle anderen Bits im  _ulFlags-Parameter_ sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="91daa-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="91daa-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="91daa-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="91daa-123">[out] Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht vor liegt.</span><span class="sxs-lookup"><span data-stu-id="91daa-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="91daa-124">TRUE, wenn eine aktualisierte Nachricht vor liegt, andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="91daa-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91daa-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91daa-125">Return value</span></span>

<span data-ttu-id="91daa-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="91daa-126">S_OK</span></span> 
  
> <span data-ttu-id="91daa-127">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="91daa-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91daa-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91daa-128">Remarks</span></span>

<span data-ttu-id="91daa-129">Wenn die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) -Eigenschaft fehlt oder FALSE ist, vor dem Lesen der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) -Eigenschaft sollte die **RTFSync** -Funktion mit dem flag set RTF_SYNC_BODY_CHANGED aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="91daa-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="91daa-130">Wenn das STORE_RTF_OK in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft nicht festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED-Flag nach dem Ändern von **PR_RTF_COMPRESSED aufgerufen werden.**</span><span class="sxs-lookup"><span data-stu-id="91daa-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="91daa-131">Wenn sowohl **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) als **auch** PR_RTF_COMPRESSED geändert wurden, sollte die **RTFSync-Funktion** mit beiden Flags aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="91daa-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="91daa-132">Wenn der Wert des  _Parameters lpfMessageUpdated_ auf TRUE festgelegt ist, sollte die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die Nachricht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="91daa-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="91daa-133">Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="91daa-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="91daa-134">Nachrichtenspeicheranbieter können **RTFSync** verwenden, um die eigenschaften **PR_BODY** und **PR_RTF_COMPRESSED** zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="91daa-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="91daa-135">Weitere Informationen finden Sie unter [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="91daa-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91daa-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91daa-136">See also</span></span>

- [<span data-ttu-id="91daa-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="91daa-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

