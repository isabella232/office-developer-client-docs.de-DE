---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423629"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="ec7d7-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="ec7d7-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="ec7d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec7d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec7d7-105">Sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-105">Locks or unlocks a message.</span></span> <span data-ttu-id="ec7d7-106">Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="ec7d7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec7d7-107">Parameters</span></span>

 <span data-ttu-id="ec7d7-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ec7d7-108">_lpMessage_</span></span>
  
> <span data-ttu-id="ec7d7-109">in Ein Zeiger auf die Nachricht zum Sperren oder entsperren.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="ec7d7-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="ec7d7-110">_ulLockState_</span></span>
  
> <span data-ttu-id="ec7d7-111">in Ein Wert, der angibt, ob die Nachricht gesperrt oder entsperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="ec7d7-112">Einer der folgenden Werte ist gültig:</span><span class="sxs-lookup"><span data-stu-id="ec7d7-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="ec7d7-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="ec7d7-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="ec7d7-114">Die Nachricht sollte gesperrt sein.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-114">The message should be locked.</span></span> 
    
<span data-ttu-id="ec7d7-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="ec7d7-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="ec7d7-116">Die Nachricht sollte entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec7d7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec7d7-117">Return value</span></span>

<span data-ttu-id="ec7d7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec7d7-118">S_OK</span></span> 
  
> <span data-ttu-id="ec7d7-119">Der Sperrstatus der Nachricht wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec7d7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec7d7-120">Remarks</span></span>

<span data-ttu-id="ec7d7-121">Mit der **IMsgStore:: SetLockState** -Methode wird eine Nachricht gesperrt oder aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="ec7d7-122">**SetLockState** kann nur vom MAPI-Spooler aufgerufen werden, wenn die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="ec7d7-123">Wenn der MAPI-Spooler **SetLockState** zum Sperren einer Nachricht aufruft, sperrt er in der Regel nur die älteste Nachricht (also die nächste Nachricht, die in der Warteschlange für den zu sendenden MAPI-Spooler steht).</span><span class="sxs-lookup"><span data-stu-id="ec7d7-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="ec7d7-124">Wenn die älteste Nachricht in der Warteschlange auf einen vorübergehend nicht verfügbaren Transportanbieter wartet und die nächste Nachricht in der Warteschlange einen anderen Transportanbieter verwendet, kann der MAPI-Spooler mit der Verarbeitung der späteren Nachricht beginnen.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="ec7d7-125">Die Verarbeitung wird gestartet, indem diese Nachricht mithilfe von **SetLockState**gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ec7d7-126">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ec7d7-126">Notes to implementers</span></span>

<span data-ttu-id="ec7d7-127">Nachdem der MAPI-Spooler **SetLockState** aufgerufen hat, wobei der Parameter _ulLockState_ auf MSG_LOCKED festgelegt ist, müssen Aufrufe an die [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) -Methode zum Abbrechen der Nachrichtenübertragung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="ec7d7-128">Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht in der **SetLockState** -Implementierung auf, sodass alle Änderungen, die an der Nachricht vorgenommen wurden, bevor der **SetLockState** -Aufruf empfangen wurde, gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ec7d7-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec7d7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec7d7-129">See also</span></span>



[<span data-ttu-id="ec7d7-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="ec7d7-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="ec7d7-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="ec7d7-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="ec7d7-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ec7d7-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

