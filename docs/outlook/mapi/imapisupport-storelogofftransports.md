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
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="8265b-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="8265b-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="8265b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8265b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8265b-105">Fordert die geordnete Freigabe eines Nachrichtenspeichers an.</span><span class="sxs-lookup"><span data-stu-id="8265b-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8265b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8265b-106">Parameters</span></span>

 <span data-ttu-id="8265b-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8265b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8265b-108">[in, out] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtenspeicher abmeldet.</span><span class="sxs-lookup"><span data-stu-id="8265b-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="8265b-109">Bei der Eingabe schließen sich alle Flags für diesen Parameter gegenseitig aus. Pro Anruf kann nur eines der folgenden Kennzeichen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8265b-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="8265b-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="8265b-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="8265b-111">Alle Transportanbieteraktivitäten für diesen Speicher sollten vor dem Abmelden beendet werden.</span><span class="sxs-lookup"><span data-stu-id="8265b-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="8265b-112">Das Steuerelement wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und der MAPI-Spooler den Speicher abgemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="8265b-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="8265b-113">Wenn eine Transportaktivität stattfindet, tritt die Abmeldeung nicht auf, und das Verhalten des MAPI-Spoolers oder des Transportanbieters wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="8265b-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="8265b-114">Wenn derzeit keine Aktivität besteht, gibt der MAPI-Spooler den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="8265b-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="8265b-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="8265b-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="8265b-116">Der MAPI-Spooler sollte den Speicher freigegeben und die Steuerung sofort an den Client zurückgeben, nachdem alle ausgehenden E-Mails gesendet wurden, die gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8265b-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="8265b-117">Wenn der Nachrichtenspeicher über den Standardeinzug verfügt, wird jede In-Process-Nachricht empfangen, und dann wird der weitere Empfang deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8265b-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="8265b-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="8265b-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="8265b-119">Der MAPI-Spooler sollte den Speicher los lassen und die Steuerung unmittelbar nach Abschluss der Verarbeitung ausstehender Nachrichten an den Client zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8265b-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="8265b-120">Es sollten keine neuen Nachrichten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8265b-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="8265b-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="8265b-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="8265b-122">Funktioniert genauso wie das LOGOFF_NO_WAIT Flag.</span><span class="sxs-lookup"><span data-stu-id="8265b-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="8265b-123">Das LOGOFF_PURGE gibt das Steuerelement nach Abschluss an den Anrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="8265b-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="8265b-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="8265b-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="8265b-125">Die Abmeldeung sollte nicht auftreten, wenn eine Transportanbieteraktivität stattfindet.</span><span class="sxs-lookup"><span data-stu-id="8265b-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="8265b-126">Der Typ der Aktivität, die stattfindet, wird als Flag für die Ausgabe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8265b-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="8265b-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="8265b-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="8265b-128">Die Abmeldeung kann abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8265b-128">The logoff can complete.</span></span> <span data-ttu-id="8265b-129">Alle dem Speicher zugeordneten Ressourcen wurden freigegeben, und das Objekt wurde ungültig.</span><span class="sxs-lookup"><span data-stu-id="8265b-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="8265b-130">Der MAPI-Spooler hat alle Anforderungen ausgeführt oder führt diese aus.</span><span class="sxs-lookup"><span data-stu-id="8265b-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="8265b-131">Nur die **IUnknown::Release-Methode** des Nachrichtenspeichers sollte an diesem Punkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8265b-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="8265b-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="8265b-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="8265b-133">Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern in den Store gesendet.</span><span class="sxs-lookup"><span data-stu-id="8265b-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="8265b-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="8265b-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="8265b-135">Eine Nachricht wird derzeit von einem oder mehreren Transportanbietern aus dem Store gesendet.</span><span class="sxs-lookup"><span data-stu-id="8265b-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="8265b-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="8265b-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="8265b-137">Derzeit befinden sich Nachrichten in der ausgehenden Warteschlange für den Speicher.</span><span class="sxs-lookup"><span data-stu-id="8265b-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8265b-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8265b-138">Return value</span></span>

<span data-ttu-id="8265b-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="8265b-139">S_OK</span></span> 
  
> <span data-ttu-id="8265b-140">Die Abmeldeprozedur war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8265b-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8265b-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8265b-141">Remarks</span></span>

<span data-ttu-id="8265b-142">Die **IMAPISupport::StoreLogoffTransports-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="8265b-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8265b-143">Nachrichtenspeicheranbieter rufen **StoreLogoffTransports** auf, um Clientanwendungen die Kontrolle darüber zu geben, wie MAPI transport provider activity as a message store is closing behandelt.</span><span class="sxs-lookup"><span data-stu-id="8265b-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="8265b-144">Wenn ein anderer Prozess den Speicher geöffnet hat, der für dasselbe Profil geöffnet werden soll, ignoriert MAPI einen Aufruf von **StoreLogoffTransports** und gibt das Flag LOGOFF_COMPLETE im  _lpulFlags-Parameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="8265b-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="8265b-145">Das Verhalten des Speicheranbieters nach der Rückgabe von **StoreLogoffTransports** sollte auf dem Wert von  _lpulFlags_ basieren, der den Systemstatus angibt und Clientanweisungen für das Abmeldeverhalten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="8265b-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8265b-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8265b-146">Notes to callers</span></span>

 <span data-ttu-id="8265b-147">**StoreLogoffTransports** wird in der Regel von der [IMsgStore::StoreLogoff-Methode](imsgstore-storelogoff.md) eines Speicheranbieters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8265b-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="8265b-148">Sie kann jedoch auch von der **IUnknown::Release-Methode des** Nachrichtenspeichers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8265b-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="8265b-149">Implementieren Sie **die Release-Methode** Ihres Nachrichtenspeichers, damit Sie überprüfen können, ob ein Aufruf von **StoreLogoffTransports** stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="8265b-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="8265b-150">Wenn kein Anruf erfolgt ist, rufen **Sie StoreLogoffTransports** mit dem LOGOFF_ABORT auf.</span><span class="sxs-lookup"><span data-stu-id="8265b-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="8265b-151">Der  _lpulFlags-Parameter_ ist auf ein Flag festgelegt, das angibt, wie der Client das Herunterfahren des Nachrichtenspeichers erfordert.</span><span class="sxs-lookup"><span data-stu-id="8265b-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="8265b-152">Bestimmen Sie die entsprechende Einstellung für  _ulFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf von **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="8265b-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="8265b-153">Das heißt, wenn ein Client Ihre **StoreLogoff-Methode** mit  _ulFlags_ auf LOGOFF_ORDERLY festgelegt hat, sollten Sie **StoreLogoffTransports** aufrufen, wenn  _ulFlags_ auf LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="8265b-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="8265b-154">Weitere Informationen zum Abmeldevorgang des Nachrichtenspeichers finden Sie unter [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8265b-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8265b-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8265b-155">See also</span></span>



[<span data-ttu-id="8265b-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="8265b-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="8265b-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="8265b-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="8265b-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8265b-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

