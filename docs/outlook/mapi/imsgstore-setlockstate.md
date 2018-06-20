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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792628"
---
# <a name="imsgstoresetlockstate"></a><span data-ttu-id="3ad3c-103">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="3ad3c-103">IMsgStore::SetLockState</span></span>

  
  
<span data-ttu-id="3ad3c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ad3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ad3c-105">Sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-105">Locks or unlocks a message.</span></span> <span data-ttu-id="3ad3c-106">Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a><span data-ttu-id="3ad3c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ad3c-107">Parameters</span></span>

 <span data-ttu-id="3ad3c-108">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3ad3c-108">_lpMessage_</span></span>
  
> <span data-ttu-id="3ad3c-109">[in] Ein Zeiger auf die Nachricht zu sperren oder entsperren.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-109">[in] A pointer to the message to lock or unlock.</span></span>
    
 <span data-ttu-id="3ad3c-110">_ulLockState_</span><span class="sxs-lookup"><span data-stu-id="3ad3c-110">_ulLockState_</span></span>
  
> <span data-ttu-id="3ad3c-111">[in] Ein Wert, der angibt, ob die Nachricht gesperrt oder entsperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-111">[in] A value that indicates whether the message should be locked or unlocked.</span></span> <span data-ttu-id="3ad3c-112">Einer der folgenden Werte ist gültig:</span><span class="sxs-lookup"><span data-stu-id="3ad3c-112">One of the following values is valid:</span></span>
    
<span data-ttu-id="3ad3c-113">MSG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="3ad3c-113">MSG_LOCKED</span></span> 
  
> <span data-ttu-id="3ad3c-114">Die Nachricht sollte gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-114">The message should be locked.</span></span> 
    
<span data-ttu-id="3ad3c-115">MSG_UNLOCKED</span><span class="sxs-lookup"><span data-stu-id="3ad3c-115">MSG_UNLOCKED</span></span> 
  
> <span data-ttu-id="3ad3c-116">Die Nachricht muss aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-116">The message should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ad3c-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3ad3c-117">Return value</span></span>

<span data-ttu-id="3ad3c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ad3c-118">S_OK</span></span> 
  
> <span data-ttu-id="3ad3c-119">Der Sperrstatus der Nachricht wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-119">The lock state of the message was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ad3c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3ad3c-120">Remarks</span></span>

<span data-ttu-id="3ad3c-121">Die **IMsgStore::SetLockState** -Methode sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-121">The **IMsgStore::SetLockState** method locks or unlocks a message.</span></span> <span data-ttu-id="3ad3c-122">**SetLockState** kann nur durch die MAPI-Warteschlange aufgerufen werden, während sie die Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-122">**SetLockState** can be called only by the MAPI spooler while it is sending the message.</span></span> 
  
<span data-ttu-id="3ad3c-123">In der Regel, wenn die Warteschlange MAPI **SetLockState** So sperren Sie eine Nachricht aufruft, sperrt er nur die älteste Nachricht (d. h., die nächste Nachricht in der Warteschlange für die MAPI-Warteschlange senden).</span><span class="sxs-lookup"><span data-stu-id="3ad3c-123">Usually, when the MAPI spooler calls **SetLockState** to lock a message, it locks only the oldest message (that is, the next message queued for the MAPI spooler to send).</span></span> <span data-ttu-id="3ad3c-124">Wenn der ältesten Nachrichten in der Warteschlange darauf, dass eines Transportdienstes vorübergehend nicht verfügbar wartet, und die nächste Nachricht in der Warteschlange ein anderen Transportdienstes verwendet, kann die MAPI-Warteschlange verarbeitet die Nachricht spätere beginnen.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-124">If the oldest message in the queue is waiting for a temporarily unavailable transport provider, and the next message in the queue uses a different transport provider, the MAPI spooler can begin processing the later message.</span></span> <span data-ttu-id="3ad3c-125">Verarbeitung beginnt durch das Sperren dieser Nachricht mithilfe von **SetLockState**.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-125">It begins processing by locking that message by using **SetLockState**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ad3c-126">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="3ad3c-126">Notes to implementers</span></span>

<span data-ttu-id="3ad3c-127">Nachdem die MAPI-Warteschlange mit der _UlLockState_ -Parameter auf MSG_LOCKED **SetLockState** aufgerufen, müssen Aufrufe an die [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) -Methode die Nachricht Übertragung abzubrechen fehl.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-127">After the MAPI spooler has called **SetLockState** with the  _ulLockState_ parameter set to MSG_LOCKED, calls to the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method to cancel the message's transmission must fail.</span></span> 
  
<span data-ttu-id="3ad3c-128">Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode in der Implementierung **SetLockState** , sodass alle Änderungen, die an die Nachricht vorgenommen wurden, bevor der Anruf **SetLockState** eingegangen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3ad3c-128">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method in your **SetLockState** implementation so that any changes that were made to the message before the **SetLockState** call was received are saved.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ad3c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ad3c-129">See also</span></span>



[<span data-ttu-id="3ad3c-130">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="3ad3c-130">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="3ad3c-131">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="3ad3c-131">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="3ad3c-132">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3ad3c-132">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

