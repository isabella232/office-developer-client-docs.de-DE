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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792439"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="bbab9-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="bbab9-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="bbab9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbab9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbab9-105">Fordert die ordnungsgemäße Version von eines Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="bbab9-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bbab9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbab9-106">Parameters</span></span>

 <span data-ttu-id="bbab9-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbab9-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="bbab9-108">[in, out] Eine Bitmaske aus Flags, die steuert, wie die Nachricht Store Abmeldung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="bbab9-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="bbab9-109">Bei der Eingabe sind alle Flags für diesen Parameter schließen sich gegenseitig aus. pro Aufruf kann nur eine der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bbab9-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="bbab9-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="bbab9-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="bbab9-111">Alle Anbieter transportaktivität für diesen Informationsspeicher sollten vor der Abmeldung beendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbab9-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="bbab9-112">Steuerelement wird an den Client zurückgegeben, nachdem die Aktivität beendet wurde und die MAPI-Warteschlange hat den Speicher abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="bbab9-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="bbab9-113">Wenn keine transportaktivität stattfindet, die Abmeldung tritt nicht auf, und keine Änderung in das MAPI-Warteschlange oder Transport Anbieter Verhalten tritt auf.</span><span class="sxs-lookup"><span data-stu-id="bbab9-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="bbab9-114">Wenn derzeit keine Aktivität vorhanden ist, gibt die MAPI-Warteschlange den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="bbab9-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="bbab9-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="bbab9-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="bbab9-116">Die MAPI-Warteschlange sollte lassen Sie den Speicher und sofort gesendet erst, nachdem alle ausgehender Nachrichten, der gesendet werden kann, wird die Steuerung an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="bbab9-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="bbab9-117">Weist der Nachrichtenspeicher der standardmäßige Posteingang, alle in-Process-Nachricht empfangen, und klicken Sie dann weitere Empfang ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bbab9-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="bbab9-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="bbab9-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="bbab9-119">Die MAPI-Warteschlange sollte Version den Speicher und die Steuerung an den Client zurückgegeben, unmittelbar nachdem alle ausstehenden Nachrichten abgeschlossen sind verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bbab9-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="bbab9-120">Keine neuen Nachrichten verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bbab9-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="bbab9-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="bbab9-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="bbab9-122">Funktioniert das Flag LOGOFF_NO_WAIT identisch.</span><span class="sxs-lookup"><span data-stu-id="bbab9-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="bbab9-123">Das Flag LOGOFF_PURGE gibt das Steuerelement mit dem Anrufer nach Abschluss zurück.</span><span class="sxs-lookup"><span data-stu-id="bbab9-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="bbab9-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="bbab9-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="bbab9-125">Das Abmelden sollte nicht auftreten, wenn alle Anbieter transportaktivität stattfindet.</span><span class="sxs-lookup"><span data-stu-id="bbab9-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="bbab9-126">Der Typ der Aktivität stattfinden wird als Flag auf Ausgabe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbab9-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="bbab9-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="bbab9-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="bbab9-128">Führen Sie das Abmelden kann.</span><span class="sxs-lookup"><span data-stu-id="bbab9-128">The logoff can complete.</span></span> <span data-ttu-id="bbab9-129">Das Objekt wurde für ungültig erklärt wurde, und alle mit dem Speicher zugeordnete Ressourcen veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="bbab9-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="bbab9-130">Die MAPI-Warteschlange durchgeführten oder führt alle Anfragen.</span><span class="sxs-lookup"><span data-stu-id="bbab9-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="bbab9-131">Nur die Nachrichtenspeicher **IUnknown** -Methode sollte zu diesem Zeitpunkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bbab9-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="bbab9-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="bbab9-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="bbab9-133">Eine Nachricht stammt aktuell in den Speicher mindestens einen Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="bbab9-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="bbab9-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="bbab9-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="bbab9-135">Eine Nachricht wird derzeit aus dem Speicher von Anbietern für eine oder mehrere Transport gesendet.</span><span class="sxs-lookup"><span data-stu-id="bbab9-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="bbab9-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="bbab9-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="bbab9-137">Meldungen sind in die Warteschlange für den Speicher für ausgehende derzeit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bbab9-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbab9-138">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bbab9-138">Return value</span></span>

<span data-ttu-id="bbab9-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbab9-139">S_OK</span></span> 
  
> <span data-ttu-id="bbab9-140">Das Abmelden Verfahren erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bbab9-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbab9-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbab9-141">Remarks</span></span>

<span data-ttu-id="bbab9-142">Die **IMAPISupport::StoreLogoffTransports** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="bbab9-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="bbab9-143">Nachricht-Anbieter anrufen **StoreLogoffTransports** um-Clientanwendungen können einige Steuern wie MAPI-Handles Transport Anbieter Aktivität als Nachrichtenspeicher geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="bbab9-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="bbab9-144">Weist einem anderen Prozess auf den Speicher zu öffnen, für das gleiche Profil abgemeldet werden, MAPI einen Anruf an **StoreLogoffTransports** ignoriert und das Flag LOGOFF_COMPLETE in der _LpulFlags_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbab9-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="bbab9-145">Das Verhalten des Anbieters zur Rückgabe von **StoreLogoffTransports** folgen sollte auf den Wert der _LpulFlags_, basieren die anzeigt, Systemstatus und Client-Anweisungen für die Abmeldung Verhalten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bbab9-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbab9-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="bbab9-146">Notes to callers</span></span>

 <span data-ttu-id="bbab9-147">**StoreLogoffTransports** wird normalerweise aus einem Speicheranbieter [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bbab9-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="bbab9-148">Es kann jedoch auch von der **IUnknown** -Methode des Nachrichtenspeichers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bbab9-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="bbab9-149">Implementieren Sie die **Release** -Methode des Nachrichtenspeichers, damit Sie überprüfen können, unabhängig davon, ob ein Aufruf von **StoreLogoffTransports** stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="bbab9-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="bbab9-150">Wenn Sie ein Anruf nicht aufgetreten ist, rufen Sie **StoreLogoffTransports** mit der LOGOFF_ABORT-Flag.</span><span class="sxs-lookup"><span data-stu-id="bbab9-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="bbab9-151">Der Parameter _LpulFlags_ ist auf ein Flag festgelegt, der angibt, wie der Client den Nachrichtenspeicher heruntergefahren werden, erfordert.</span><span class="sxs-lookup"><span data-stu-id="bbab9-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="bbab9-152">Bestimmen Sie die entsprechende Einstellung für _UlFlags_ basierend auf der Einstellung des entsprechenden Parameters im Aufruf **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="bbab9-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="bbab9-153">D. h., wenn ein Client mit _UlFlags_ auf LOGOFF_ORDERLY festgelegt Ihrer **StoreLogoff** -Methode aufgerufen, sollten Sie **StoreLogoffTransports** mit _UlFlags_ legen auf LOGOFF_ORDERLY aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bbab9-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="bbab9-154">Weitere Informationen zu der Nachricht Speichervorgang Abmeldung wird finden Sie unter [Herunterfahren nach unten einer Nachricht speichern-Anbieter](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bbab9-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbab9-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbab9-155">See also</span></span>



[<span data-ttu-id="bbab9-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="bbab9-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="bbab9-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="bbab9-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="bbab9-158">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbab9-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

