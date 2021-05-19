---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424336"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="e7c3e-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="e7c3e-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="e7c3e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7c3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7c3e-105">Aktiviert die geordnete Abmeldung des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e7c3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7c3e-106">Parameters</span></span>

 <span data-ttu-id="e7c3e-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7c3e-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e7c3e-108">[in, out] Eine Bitmaske mit Flags, die die Abmeldung aus dem Nachrichtenspeicher steuert.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="e7c3e-109">Bei der Eingabe schließen sich alle für diesen Parameter festgelegten Flags gegenseitig aus. Ein Anrufer darf pro Anruf nur ein Flag angeben.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="e7c3e-110">Die folgenden Flags sind für die Eingabe gültig:</span><span class="sxs-lookup"><span data-stu-id="e7c3e-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="e7c3e-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="e7c3e-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="e7c3e-112">Alle Transportanbieteraktivitäten für diesen Nachrichtenspeicher sollten vor dem Abmelden beendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="e7c3e-113">Das Steuerelement wird an den Anrufer zurückgegeben, nachdem die Aktivität beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="e7c3e-114">Wenn eine Transportanbieteraktivität stattfindet, tritt die Abmeldeung nicht auf, und es tritt keine Änderung des Verhaltens des MAPI-Spoolers oder des Transportanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="e7c3e-115">Wenn sich die Aktivität des Transportanbieters im Leerlauf befindet, gibt der MAPI-Spooler den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="e7c3e-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="e7c3e-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="e7c3e-117">Der Nachrichtenspeicher sollte vor dem Schließen nicht auf Nachrichten von Transportanbietern warten.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="e7c3e-118">Ausgehende Nachrichten, die gesendet werden können, werden gesendet.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="e7c3e-119">Wenn dieser Speicher den Standardeinzug enthält, werden alle In-Process-Nachrichten empfangen, und dann wird der weitere Empfang deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="e7c3e-120">Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="e7c3e-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="e7c3e-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="e7c3e-122">Der Nachrichtenspeicher sollte nicht vor dem Schließen auf Informationen von Transportanbietern warten.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="e7c3e-123">Nachrichten, die derzeit verarbeitet werden, werden abgeschlossen, es werden jedoch keine neuen Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="e7c3e-124">Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Speicheranbieter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="e7c3e-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="e7c3e-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="e7c3e-126">Die Abmeldemethode sollte genauso funktionieren, als wäre das LOGOFF_NO_WAIT-Flag festgelegt, aber entweder die [IXPLogon::FlushQueues-](ixplogon-flushqueues.md) oder [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) für die entsprechenden Transportanbieter sollte aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="e7c3e-127">Das LOGOFF_PURGE gibt das Steuerelement nach Abschluss an den Anrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="e7c3e-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="e7c3e-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="e7c3e-129">Wenn eine Transportanbieteraktivität stattfindet, sollte die Abmeldeung nicht erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="e7c3e-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="e7c3e-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="e7c3e-131">Eingehende Nachrichten werden derzeit empfangen.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="e7c3e-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="e7c3e-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="e7c3e-133">Ausgehende Nachrichten werden gerade gesendet.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="e7c3e-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="e7c3e-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="e7c3e-135">Ausgehende Nachrichten sind ausstehend (d. h. sie befinden sich im Posteingang).</span><span class="sxs-lookup"><span data-stu-id="e7c3e-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7c3e-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7c3e-136">Return value</span></span>

<span data-ttu-id="e7c3e-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7c3e-137">S_OK</span></span> 
  
> <span data-ttu-id="e7c3e-138">Die Abmeldeung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7c3e-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7c3e-139">Remarks</span></span>

<span data-ttu-id="e7c3e-140">Die **IMsgStore::StoreLogoff-Methode** übernimmt während des Abmeldevorgangs die Kontrolle über die Interaktion von Nachrichtenspeicher und Transportanbietern.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="e7c3e-141">Das **Aufrufen von StoreLogoff** ist nur für Nachrichtenspeicher gültig, die nur vom Anrufer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="e7c3e-142">Wenn beispielsweise zwei Clients denselben Nachrichtenspeicher verwenden und einer von ihnen **StoreLogoff** aufruft, wird der Nachrichtenspeicher sofort freigegeben und das Steuerelement an den aufrufenden Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e7c3e-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e7c3e-143">Notes to implementers</span></span>

<span data-ttu-id="e7c3e-144">Speichern Sie die Flags, die an **StoreLogoff übergeben** werden, und übergeben Sie sie, wenn Sie die [IMAPISupport::StoreLogoffTransports-Methode](imapisupport-storelogofftransports.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="e7c3e-145">Rufen Sie **StoreLogoffTransports** erst auf, wenn die Referenzanzahl des Nachrichtenspeichers auf Null sinkt.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="e7c3e-146">Mehrere Aufrufe von **StoreLogoffTransports** überschreiben einfach die gespeicherten Flags.</span><span class="sxs-lookup"><span data-stu-id="e7c3e-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="e7c3e-147">Wenn kein Aufruf von **StoreLogoff** erfolgt ist, bevor die Referenzanzahl des Nachrichtenspeichers null erreicht, legen Sie das LOGOFF_ABORT-Flag im _ulFlags-Parameter_ fest, den Sie an **StoreLogoffTransports übergeben.**</span><span class="sxs-lookup"><span data-stu-id="e7c3e-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7c3e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7c3e-148">See also</span></span>



[<span data-ttu-id="e7c3e-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e7c3e-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="e7c3e-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="e7c3e-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="e7c3e-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e7c3e-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="e7c3e-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e7c3e-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

