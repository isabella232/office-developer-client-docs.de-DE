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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316479"
---
# <a name="rtfsync"></a><span data-ttu-id="8adac-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="8adac-103">RTFSync</span></span>

<span data-ttu-id="8adac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8adac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8adac-105">Stellt sicher, dass der RTF-Nachrichten Text (Rich Text Format) mit der nur-Text-Version übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8adac-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="8adac-106">Diese Funktion muss aufgerufen werden, bevor die RTF-Version gelesen und die RTF-Version geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="8adac-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8adac-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8adac-107">Header file:</span></span>  <br/> |<span data-ttu-id="8adac-108">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8adac-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8adac-109">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8adac-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="8adac-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="8adac-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="8adac-111">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8adac-111">Called by:</span></span>  <br/> |<span data-ttu-id="8adac-112">RTF-fähige Clientanwendungen und Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="8adac-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="8adac-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8adac-113">Parameters</span></span>

<span data-ttu-id="8adac-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="8adac-114">_lpMessage_</span></span>
  
> <span data-ttu-id="8adac-115">in Zeiger auf die zu aktualisierende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8adac-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="8adac-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8adac-116">_ulFlags_</span></span>
  
> <span data-ttu-id="8adac-117">in Bitmaske der Flags, mit denen die RTF-oder nur-Text-Version der Nachricht angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8adac-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="8adac-118">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8adac-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="8adac-119">RTF_SYNC_BODY_CHANGED: die nur-Text-Version der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="8adac-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="8adac-120">RTF_SYNC_RTF_CHANGED: die RTF-Version der Nachricht wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="8adac-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="8adac-121">Alle anderen Bits im _ulFlags_ -Parameter sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8adac-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="8adac-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="8adac-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="8adac-123">Out Zeiger auf eine Variable, die angibt, ob eine aktualisierte Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8adac-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="8adac-124">TRUE, wenn eine aktualisierte Nachricht vorhanden ist, andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="8adac-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8adac-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8adac-125">Return value</span></span>

<span data-ttu-id="8adac-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="8adac-126">S_OK</span></span> 
  
> <span data-ttu-id="8adac-127">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8adac-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8adac-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8adac-128">Remarks</span></span>

<span data-ttu-id="8adac-129">Wenn die **PR_RTF_IN_SYNC** ([pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))-Eigenschaft fehlt oder false ist, bevor Sie die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft lesen, sollte die **RTFSync** -Funktion mit dem RTF_SYNC_BODY_ aufgerufen werden. GEÄNDERTer Flagsatz.</span><span class="sxs-lookup"><span data-stu-id="8adac-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="8adac-130">Wenn das STORE_RTF_OK-Flag nicht in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festgelegt ist, sollte diese Funktion mit dem RTF_SYNC_RTF_CHANGED-Flag nach dem Ändern von **PR_RTF_COMPRESSED**aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8adac-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="8adac-131">Wenn sowohl **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)) als auch **PR_RTF_COMPRESSED** geändert wurden, sollte die **RTFSync** -Funktion mit beiden Flags festgelegt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8adac-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="8adac-132">Wenn der Wert des _lpfMessageUpdated_ -Parameters auf true festgelegt ist, sollte die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode für die Nachricht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8adac-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="8adac-133">Wenn **SaveChanges** nicht aufgerufen wird, werden die Änderungen nicht in der Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8adac-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="8adac-134">Nachrichtenspeicher Anbieter können **RTFSync** verwenden, um die **PR_BODY** -und **PR_RTF_COMPRESSED** -Eigenschaften zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="8adac-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="8adac-135">Weitere Informationen finden Sie unter [Unterstützung von RTF-Text für Nachrichtenspeicher Anbieter](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="8adac-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8adac-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8adac-136">See also</span></span>

- [<span data-ttu-id="8adac-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="8adac-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

