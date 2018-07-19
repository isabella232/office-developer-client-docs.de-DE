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
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792638"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="7ef5d-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="7ef5d-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="7ef5d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ef5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ef5d-105">Ermöglicht das ordnungsgemäße Abmelden des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7ef5d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ef5d-106">Parameters</span></span>

 <span data-ttu-id="7ef5d-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ef5d-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="7ef5d-108">[in, out] Eine Bitmaske aus Flags, die aus dem Nachrichtenspeicher Abmeldung steuert.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="7ef5d-109">Bei der Eingabe sind alle Flags für diesen Parameter festlegen schließen sich gegenseitig aus. ein Anrufer muss nur ein Flag pro Aufruf angeben.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="7ef5d-110">Die folgenden Kennzeichen sind bei der Eingabe gültig:</span><span class="sxs-lookup"><span data-stu-id="7ef5d-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="7ef5d-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="7ef5d-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="7ef5d-112">Alle Anbieter transportaktivität für diesen Nachrichtenspeicher sollten vor der Abmeldung beendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="7ef5d-113">Steuerelement wird mit dem Anrufer zurückgegeben, nachdem Aktivität beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="7ef5d-114">Wenn alle Anbieter transportaktivität stattfindet, die Abmeldung tritt nicht auf, und keine Änderung des Verhaltens der MAPI-Warteschlange oder Transport Anbieter tritt auf.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="7ef5d-115">Wenn der Anbieter transportaktivität im Leerlauf befindet, gibt die MAPI-Warteschlange den Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="7ef5d-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="7ef5d-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="7ef5d-117">Der Nachrichtenspeicher sollte nicht für Nachrichten von Anbietern vor dem Schließen Transport warten.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="7ef5d-118">Ausgehende Nachrichten, die gesendet werden können, werden gesendet.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="7ef5d-119">Wenn dieser Speicher der standardmäßige Posteingang enthält, werden alle Nachrichten in-Process empfangen, und klicken Sie dann weitere Empfang deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="7ef5d-120">Wenn alle Aktivitäten abgeschlossen ist, die MAPI-Warteschlange gibt den Speicher und Steuerelement wird mit dem Anrufer sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="7ef5d-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="7ef5d-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="7ef5d-122">Der Nachrichtenspeicher sollten Informationen von Transport Anbietern vor dem Schließen nicht warten.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="7ef5d-123">Nachrichten, die aktuell verarbeitet werden abgeschlossen sind, jedoch keine neuen Nachrichten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="7ef5d-124">Wenn alle Aktivitäten abgeschlossen ist, die MAPI-Warteschlange gibt den Speicher und Steuerung sofort auf den Anbieter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="7ef5d-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="7ef5d-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="7ef5d-126">Das Abmelden sollte dieselbe funktionieren das Flag LOGOFF_NO_WAIT festgelegt ist, wobei jedoch die [IXPLogon::FlushQueues](ixplogon-flushqueues.md) oder [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode für die entsprechenden Transportanbieter sollte aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="7ef5d-127">Das Flag LOGOFF_PURGE gibt das Steuerelement mit dem Anrufer nach Abschluss zurück.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="7ef5d-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="7ef5d-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="7ef5d-129">Wenn alle Anbieter transportaktivität stattfindet, sollte das Abmelden nicht erfolgen.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="7ef5d-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="7ef5d-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="7ef5d-131">Eingehende Nachrichten werden derzeit erhältlich.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="7ef5d-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="7ef5d-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="7ef5d-133">Ausgehende Nachrichten werden gerade gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="7ef5d-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="7ef5d-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="7ef5d-135">Ausgehende Nachrichten werden ausstehende (d. h., sie sind in den Postausgang).</span><span class="sxs-lookup"><span data-stu-id="7ef5d-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ef5d-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ef5d-136">Return value</span></span>

<span data-ttu-id="7ef5d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ef5d-137">S_OK</span></span> 
  
> <span data-ttu-id="7ef5d-138">Die Abmeldung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ef5d-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ef5d-139">Remarks</span></span>

<span data-ttu-id="7ef5d-140">Die **IMsgStore::StoreLogoff** -Methode beim Ausrichten ausübt Steuerelement über die Interaktion der Nachricht speichern und transport-Anbieter während des Abmeldevorgangs.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="7ef5d-141">Aufrufen von **StoreLogoff** gilt nur für Nachrichtenspeicher, die nur vom Anrufer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="7ef5d-142">Beispielsweise wenn zwei Clients den gleichen Nachrichtenspeicher verwenden und einer von ihnen **StoreLogoff**aufruft, der Nachrichtenspeicher wird sofort freigegeben und wird die Steuerung an den aufrufenden Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7ef5d-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7ef5d-143">Notes to implementers</span></span>

<span data-ttu-id="7ef5d-144">Speichern Sie die Kennzeichen, die an **StoreLogoff** übergeben werden, und übergeben Sie diese Option, wenn Sie die [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="7ef5d-145">Rufen Sie nicht **StoreLogoffTransports** , bis der Nachrichtenspeicher Referenzzähler auf Null fällt.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="7ef5d-146">Mehrere Aufrufe von **StoreLogoffTransports** überschreiben einfach die gespeicherten Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="7ef5d-147">Wenn kein Aufruf an **StoreLogoff** vorgenommen wurde vor der Meldung des Informationsspeichers Referenzzähler 0 (null) erreicht, legen Sie das Flag LOGOFF_ABORT im _UlFlags_ -Parameter, den an **StoreLogoffTransports**übergeben.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ef5d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ef5d-148">See also</span></span>



[<span data-ttu-id="7ef5d-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7ef5d-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="7ef5d-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="7ef5d-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="7ef5d-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="7ef5d-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="7ef5d-152">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7ef5d-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

