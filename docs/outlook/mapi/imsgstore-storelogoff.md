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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348741"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="c89c3-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="c89c3-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="c89c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c89c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c89c3-105">Aktiviert die ordnungsgemäße Abmeldung des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="c89c3-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c89c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c89c3-106">Parameters</span></span>

 <span data-ttu-id="c89c3-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="c89c3-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="c89c3-108">[in, out] Eine Bitmaske von Flags, die die Abmeldung aus dem Nachrichtenspeicher steuert.</span><span class="sxs-lookup"><span data-stu-id="c89c3-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="c89c3-109">Bei der Eingabe schließen sich alle für diesen Parameter festgelegten Flags gegenseitig aus; ein Anrufer muss nur ein Flag pro Anruf angeben.</span><span class="sxs-lookup"><span data-stu-id="c89c3-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="c89c3-110">Die folgenden Flags sind bei der Eingabe gültig:</span><span class="sxs-lookup"><span data-stu-id="c89c3-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="c89c3-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="c89c3-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="c89c3-112">Alle Transportanbieter Aktivitäten für diesen Nachrichtenspeicher sollten vor dem Abmelden angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="c89c3-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="c89c3-113">Das Steuerelement wird an den Aufrufer zurückgegeben, nachdem Activity beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c89c3-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="c89c3-114">Wenn eine Transportanbieter Aktivität stattfindet, wird die Abmeldung nicht ausgeführt, und es tritt keine Änderung des Verhaltens der MAPI-Spooler-oder Transportanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="c89c3-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="c89c3-115">Wenn sich die Transportanbieter Aktivität im Leerlauf befindet, gibt der MAPI-Spooler den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="c89c3-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="c89c3-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="c89c3-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="c89c3-117">Der Nachrichtenspeicher sollte vor dem Schließen nicht auf Nachrichten von Transportanbietern warten.</span><span class="sxs-lookup"><span data-stu-id="c89c3-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="c89c3-118">Ausgehende Nachrichten, die gesendet werden können, werden gesendet.</span><span class="sxs-lookup"><span data-stu-id="c89c3-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="c89c3-119">Wenn dieser Speicher den Standard Posteingang enthält, werden alle in-Process-Nachrichten empfangen, und dann wird der weitere Empfang deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c89c3-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="c89c3-120">Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c89c3-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="c89c3-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="c89c3-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="c89c3-122">Der Nachrichtenspeicher sollte vor dem Schließen nicht auf Informationen von Transportanbietern warten.</span><span class="sxs-lookup"><span data-stu-id="c89c3-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="c89c3-123">Nachrichten, die gerade verarbeitet werden, werden abgeschlossen, es werden jedoch keine neuen Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c89c3-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="c89c3-124">Wenn alle Aktivitäten abgeschlossen sind, gibt der MAPI-Spooler den Speicher frei, und das Steuerelement wird sofort an den Speicheranbieter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c89c3-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="c89c3-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="c89c3-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="c89c3-126">Die Abmeldung sollte genauso funktionieren, als ob das LOGOFF_NO_WAIT-Flag festgelegt ist, aber entweder die [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) oder [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode für die entsprechenden Transportanbieter aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c89c3-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="c89c3-127">Das LOGOFF_PURGE-Flag gibt nach Abschluss die Steuerung an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="c89c3-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="c89c3-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="c89c3-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="c89c3-129">Wenn eine Transportanbieter Aktivität stattfindet, sollte die Abmeldung nicht erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c89c3-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="c89c3-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="c89c3-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="c89c3-131">Eingehende Nachrichten werden gerade ankommen.</span><span class="sxs-lookup"><span data-stu-id="c89c3-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="c89c3-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="c89c3-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="c89c3-133">Ausgehende Nachrichten werden gerade gesendet.</span><span class="sxs-lookup"><span data-stu-id="c89c3-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="c89c3-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="c89c3-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="c89c3-135">Ausgehende Nachrichten sind ausstehend (das heißt, Sie befinden sich im Postausgang).</span><span class="sxs-lookup"><span data-stu-id="c89c3-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c89c3-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c89c3-136">Return value</span></span>

<span data-ttu-id="c89c3-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="c89c3-137">S_OK</span></span> 
  
> <span data-ttu-id="c89c3-138">Die Abmeldung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c89c3-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c89c3-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c89c3-139">Remarks</span></span>

<span data-ttu-id="c89c3-140">Die **IMsgStore:: StoreLogoff** -Methode übt während des Abmeldevorgangs die Steuerung der Interaktion zwischen dem Nachrichtenspeicher und den Transportanbietern aus.</span><span class="sxs-lookup"><span data-stu-id="c89c3-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="c89c3-141">Das Aufrufen von **StoreLogoff** ist nur für Nachrichtenspeicher zulässig, die nur vom Aufrufer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c89c3-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="c89c3-142">Wenn beispielsweise zwei Clients denselben Nachrichtenspeicher verwenden und einer von Ihnen **StoreLogoff**aufruft, wird der Nachrichtenspeicher sofort freigegeben, und die Steuerung wird an den aufrufenden Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c89c3-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c89c3-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c89c3-143">Notes to implementers</span></span>

<span data-ttu-id="c89c3-144">Speichern Sie die Flags, die an **StoreLogoff** übergeben werden, und übergeben Sie diese, wenn Sie die [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c89c3-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="c89c3-145">Rufen Sie **StoreLogoffTransports** erst auf, wenn der Verweiszähler des Nachrichtenspeichers auf Null sinkt.</span><span class="sxs-lookup"><span data-stu-id="c89c3-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="c89c3-146">Bei mehreren Aufrufen von **StoreLogoffTransports** werden die gespeicherten Flags einfach überschrieben.</span><span class="sxs-lookup"><span data-stu-id="c89c3-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="c89c3-147">Wenn kein Aufruf an **StoreLogoff** vorgenommen wurde, bevor der Verweiszähler des Nachrichtenspeichers 0 (null) erreicht, legen Sie das LOGOFF_ABORT-Flag im _ulFlags_ -Parameter, den Sie an **StoreLogoffTransports**übergeben.</span><span class="sxs-lookup"><span data-stu-id="c89c3-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c89c3-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c89c3-148">See also</span></span>



[<span data-ttu-id="c89c3-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c89c3-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="c89c3-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="c89c3-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="c89c3-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c89c3-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="c89c3-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c89c3-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

