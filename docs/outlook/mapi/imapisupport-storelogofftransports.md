---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421382"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="7471d-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="7471d-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="7471d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7471d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7471d-105">Fordert die ordnungsgemäße Freigabe eines Nachrichtenspeichers an.</span><span class="sxs-lookup"><span data-stu-id="7471d-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7471d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7471d-106">Parameters</span></span>

 <span data-ttu-id="7471d-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="7471d-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7471d-108">[in, out] Eine Bitmaske von Flags, die die Anzeige des Nachrichtenspeichers steuert.</span><span class="sxs-lookup"><span data-stu-id="7471d-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="7471d-109">Bei der Eingabe schließen sich alle Flags für diesen Parameter gegenseitig aus; nur eines der folgenden Flags kann pro Aufruf festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7471d-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="7471d-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="7471d-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="7471d-111">Jede Transportanbieter Aktivität für diesen Speicher sollte vor dem Abmelden angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="7471d-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="7471d-112">Das Steuerelement wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und der MAPI-Spooler sich vom Speicher abgemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="7471d-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="7471d-113">Wenn eine Transportaktivität stattfindet, wird die Abmeldung nicht ausgeführt, und es tritt keine Änderung des MAPI-Spoolers oder des Transportanbieter Verhaltens auf.</span><span class="sxs-lookup"><span data-stu-id="7471d-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="7471d-114">Wenn derzeit keine Aktivität vorhanden ist, gibt der MAPI-Spooler den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="7471d-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="7471d-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="7471d-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="7471d-116">Der MAPI-Spooler sollte den Store freigeben und sofort die Steuerung an den Client zurückgeben, nachdem alle zu sendenden ausgehenden e-Mails gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7471d-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="7471d-117">Wenn der Nachrichtenspeicher den Standard Posteingang hat, werden alle in-Process-Nachrichten empfangen, und dann wird der weitere Empfang deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7471d-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="7471d-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="7471d-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="7471d-119">Der MAPI-Spooler sollte den Speicher freigeben und sofort die Steuerung an den Client zurückgeben, nachdem alle ausstehenden Nachrichten verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="7471d-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="7471d-120">Es sollten keine neuen Nachrichten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7471d-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="7471d-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="7471d-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="7471d-122">Funktioniert wie das LOGOFF_NO_WAIT-Flag.</span><span class="sxs-lookup"><span data-stu-id="7471d-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="7471d-123">Das LOGOFF_PURGE-Flag gibt nach Abschluss die Steuerung an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="7471d-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="7471d-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="7471d-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="7471d-125">Die Abmeldung sollte nicht auftreten, wenn eine Transportanbieter Aktivität stattfindet.</span><span class="sxs-lookup"><span data-stu-id="7471d-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="7471d-126">Die Art der Aktivität, die stattfindet, wird als Flag für die Ausgabe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7471d-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="7471d-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="7471d-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="7471d-128">Die Abmeldung kann abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7471d-128">The logoff can complete.</span></span> <span data-ttu-id="7471d-129">Alle dem Speicher zugeordneten Ressourcen wurden freigegeben, und das Objekt wurde für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="7471d-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="7471d-130">Der MAPI-Spooler hat alle Anforderungen ausgeführt oder führt Sie aus.</span><span class="sxs-lookup"><span data-stu-id="7471d-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="7471d-131">Nur die **IUnknown:: Release** -Methode des Nachrichtenspeichers sollte an dieser Stelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7471d-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="7471d-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="7471d-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="7471d-133">Eine Nachricht kommt derzeit von einem oder mehreren Transportanbietern in den Store.</span><span class="sxs-lookup"><span data-stu-id="7471d-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="7471d-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="7471d-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="7471d-135">Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern aus dem Store gesendet.</span><span class="sxs-lookup"><span data-stu-id="7471d-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="7471d-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="7471d-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="7471d-137">Es befinden sich derzeit Nachrichten in der ausgehenden Warteschlange für den Speicher.</span><span class="sxs-lookup"><span data-stu-id="7471d-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7471d-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7471d-138">Return value</span></span>

<span data-ttu-id="7471d-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="7471d-139">S_OK</span></span> 
  
> <span data-ttu-id="7471d-140">Die Abmelde Prozedur war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7471d-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7471d-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7471d-141">Remarks</span></span>

<span data-ttu-id="7471d-142">Die **IMAPISupport:: StoreLogoffTransports** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="7471d-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="7471d-143">Nachrichtenspeicher Anbieter rufen **StoreLogoffTransports** auf, um Clientanwendungen zu steuern, wie MAPI die Transportanbieter Aktivität verarbeitet, wenn der Nachrichtenspeicher geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="7471d-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="7471d-144">Wenn ein anderer Prozess den zu speichernden Speicher für dasselbe Profil geöffnet hat, ignoriert MAPI einen Aufruf von **StoreLogoffTransports** und gibt das Flag LOGOFF_COMPLETE im _lpulFlags_ -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="7471d-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="7471d-145">Das Verhalten des Speicheranbieters nach der Rückgabe von **StoreLogoffTransports** sollte auf dem Wert von _lpulFlags_basieren, der den Systemstatus angibt und Client Anweisungen für das Verhalten der Abmeldung vermittelt.</span><span class="sxs-lookup"><span data-stu-id="7471d-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7471d-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7471d-146">Notes to callers</span></span>

 <span data-ttu-id="7471d-147">**StoreLogoffTransports** wird in der Regel von der [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) -Methode eines Speicheranbieters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7471d-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="7471d-148">Sie kann jedoch auch über die **IUnknown:: Release** -Methode des Nachrichtenspeichers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7471d-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="7471d-149">Implementieren Sie die **Release** -Methode des Nachrichtenspeichers, damit Sie überprüfen können, ob ein Aufruf von **StoreLogoffTransports** aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7471d-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="7471d-150">Wenn kein Anruf aufgetreten ist, rufen Sie **StoreLogoffTransports** mit dem LOGOFF_ABORT-Kennzeichen Satz auf.</span><span class="sxs-lookup"><span data-stu-id="7471d-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="7471d-151">Der Parameter _lpulFlags_ wird auf ein Flag festgelegt, das angibt, wie der Nachrichtenspeicher heruntergefahren werden muss.</span><span class="sxs-lookup"><span data-stu-id="7471d-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="7471d-152">Bestimmen Sie die entsprechende Einstellung für _ulFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf von **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="7471d-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="7471d-153">Das heißt, wenn ein Client Ihre **StoreLogoff** -Methode mit _ulFlags_ auf LOGOFF_ORDERLY festgelegt aufgerufen, sollten Sie **StoreLogoffTransports** mit _ulFlags_ auf LOGOFF_ORDERLY festgelegt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7471d-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="7471d-154">Weitere Informationen zum ABMELDEPROZESS für den Nachrichtenspeicher finden Sie unter [Herunterfahren eines Nachrichtenspeicher Anbieters](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7471d-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7471d-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7471d-155">See also</span></span>



[<span data-ttu-id="7471d-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="7471d-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="7471d-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7471d-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="7471d-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7471d-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

