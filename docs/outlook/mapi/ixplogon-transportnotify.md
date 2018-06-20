---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5429f98a0335ae99b719d0f15b66a95ba87430e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792889"
---
# <a name="ixplogontransportnotify"></a><span data-ttu-id="507bc-103">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="507bc-103">IXPLogon::TransportNotify</span></span>

<span data-ttu-id="507bc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="507bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="507bc-105">Signalisiert das Auftreten eines Ereignisses zu den der Transportdienst Benachrichtigung angefordert.</span><span class="sxs-lookup"><span data-stu-id="507bc-105">Signals the occurrence of an event about which the transport provider requested notification.</span></span>
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a><span data-ttu-id="507bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="507bc-106">Parameters</span></span>

 <span data-ttu-id="507bc-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="507bc-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="507bc-108">[in, out] Eine Bitmaske aus Flags, die Benachrichtigungsereignisse signalisiert.</span><span class="sxs-lookup"><span data-stu-id="507bc-108">[in, out] A bitmask of flags that signals notification events.</span></span> <span data-ttu-id="507bc-109">Die folgenden Kennzeichen können festgelegt werden, durch die MAPI-Warteschlange bei der Eingabe und müssen bei der Ausgabe unverändert zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="507bc-109">The following flags can be set by the MAPI spooler on input and must be returned unchanged on output:</span></span>
    
<span data-ttu-id="507bc-110">NOTIFY_ABORT_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="507bc-110">NOTIFY_ABORT_DEFERRED</span></span> 
  
> <span data-ttu-id="507bc-111">Benachrichtigt den Transportdienst, dass eine Nachricht für die sie Verantwortung anerkannt werden verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="507bc-111">Notifies the transport provider that a message for which it accepted responsibility is being deferred.</span></span> <span data-ttu-id="507bc-112">Nur Transportanbieter, Verzögerungen unterstützen, müssen dieses Flag unterstützen.</span><span class="sxs-lookup"><span data-stu-id="507bc-112">Only transport providers that support deferral must support this flag.</span></span> <span data-ttu-id="507bc-113">Der Parameter _LppvData_ verweist auf die Eintrags-ID der Nachricht wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="507bc-113">The  _lppvData_ parameter points to the entry identifier of the canceled message.</span></span> <span data-ttu-id="507bc-114">Nachrichten, die die MAPI-Warteschlange, nicht verarbeitet wurden können weiterhin durch Aufrufen der Methode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) verzögert werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-114">Messages that the MAPI spooler has not processed can still be deferred by calling the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method.</span></span> 
    
<span data-ttu-id="507bc-115">NOTIFY_BEGIN_INBOUND</span><span class="sxs-lookup"><span data-stu-id="507bc-115">NOTIFY_BEGIN_INBOUND</span></span> 
  
> <span data-ttu-id="507bc-116">Die MAPI-Warteschlange kann jetzt eingehende Nachrichten für diesen Anbieter Transport akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="507bc-116">The MAPI spooler can now accept inbound messages for this transport provider session.</span></span> <span data-ttu-id="507bc-117">Die MAPI-Warteschlange ruft regelmäßig die [IXPLogon::Poll](ixplogon-poll.md) -Methode, wenn der Adressbuchhierarchie das Flag LOGON_SP_POLL mit dem Aufruf von [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) bei der Anmeldung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="507bc-117">The MAPI spooler regularly calls the [IXPLogon::Poll](ixplogon-poll.md) method if the transport provider set the LOGON_SP_POLL flag with the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) call at logon.</span></span> <span data-ttu-id="507bc-118">Nachdem das Flag NOTIFY_BEGIN_INBOUND festgelegt ist, berücksichtigt die MAPI-Warteschlange das NOTIFY_NEWMAIL-Flag, das im Aufruf der [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="507bc-118">Once the NOTIFY_BEGIN_INBOUND flag is set, the MAPI spooler honors the NOTIFY_NEWMAIL flag passed in the call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method.</span></span> <span data-ttu-id="507bc-119">Die Status-Tabellenzeile für die Sitzung mit dem Transport sollte vor der Rückgabe durch Aufrufen der Methode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-119">The status table row for the transport provider session should be updated before returning by calling the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method.</span></span> <span data-ttu-id="507bc-120">Die Flags NOTIFY_BEGIN_INBOUND und NOTIFY_END_INBOUND schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="507bc-120">The NOTIFY_BEGIN_INBOUND and NOTIFY_END_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="507bc-121">NOTIFY_BEGIN_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="507bc-121">NOTIFY_BEGIN_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="507bc-122">Signalisiert der Adressbuchhierarchie, um eingehende Nachrichten so schnell wie möglich zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="507bc-122">Signals the transport provider to cycle through inbound messages as quickly as possible.</span></span> <span data-ttu-id="507bc-123">Um die Einhaltung dieser Benachrichtigung sollte der Adressbuchhierarchie STATUS_INBOUND_FLUSH Flag in der Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)), dessen Status Tabellenzeile festlegen, als er mithilfe von **ModifyStatusRow kann**.</span><span class="sxs-lookup"><span data-stu-id="507bc-123">To comply with this notification, the transport provider should set the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status table row as soon as it can, by using **ModifyStatusRow**.</span></span> <span data-ttu-id="507bc-124">Ein eingehender messaging Zyklus ist abgeschlossen, wenn der Anbieter bestimmt, dass sie alle heruntergeladen hat, die er kann, oder sie einen Aufruf der **TransportNotify** -Methode mit dem Flag NOTIFY_END_INBOUND_FLUSH erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="507bc-124">An inbound messaging cycle is complete when the provider determines it has downloaded all it can, or when it has received a **TransportNotify** method call with the NOTIFY_END_INBOUND_FLUSH flag set.</span></span> <span data-ttu-id="507bc-125">Bis zum Ende des eingehenden messaging Zyklus sollte der Anbieter nicht die [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) -Methode aufrufen oder anderweitig abgeben Zyklen für das Betriebssystem, um die Geschwindigkeit Übermittlung eingehender Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="507bc-125">Until the end of the inbound messaging cycle, the provider should not call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method or otherwise relinquish cycles to the operating system to speed delivery of incoming messages.</span></span> <span data-ttu-id="507bc-126">Dies ist akzeptabel, da die MAPI-Warteschlange in der Regel NOTIFY_BEGIN_INBOUND_FLUSH nur in der Antwort auf einen Benutzer an, über eine Clientanwendung verwendet, um alle Nachrichten jetzt übermitteln.</span><span class="sxs-lookup"><span data-stu-id="507bc-126">This is acceptable because the MAPI spooler typically uses NOTIFY_BEGIN_INBOUND_FLUSH only in response to a user's request, via a client application, to deliver all messages now.</span></span> <span data-ttu-id="507bc-127">Am Ende der eingehenden Schreibvorgang wurde sollte der Anbieter **SpoolerNotify** zum Deaktivieren Sie der Kennzeichen STATUS_INBOUND_FLUSH in der Statuszeile der **PR_STATUS_CODE** -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="507bc-127">At the end of the inbound flush operation, the provider should use **SpoolerNotify** to clear the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** property of its status row.</span></span> 
    
<span data-ttu-id="507bc-128">NOTIFY_BEGIN_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="507bc-128">NOTIFY_BEGIN_OUTBOUND</span></span> 
  
> <span data-ttu-id="507bc-129">Ausgehende Vorgänge können nun für diesen Anbieter Transport auftreten.</span><span class="sxs-lookup"><span data-stu-id="507bc-129">Outbound operations can now occur for this transport provider session.</span></span> <span data-ttu-id="507bc-130">Wenn vorhanden alle Nachrichten sind, die für diesen Anbieter gesendet werden, folgt ein Aufruf der [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="507bc-130">If there are any messages to be sent for this provider, a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method follows.</span></span> <span data-ttu-id="507bc-131">Die Tabellenzeile Status für diese Sitzung sollten vor der Rückgabe aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-131">The status table row for this session should be updated before returning.</span></span> <span data-ttu-id="507bc-132">Die Flags NOTIFY_BEGIN_OUTBOUND und NOTIFY_END_OUTBOUND schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="507bc-132">The NOTIFY_BEGIN_OUTBOUND and NOTIFY_END_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="507bc-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="507bc-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="507bc-134">Verhält sich das Flag NOTIFY_BEGIN_INBOUND_FLUSH, aber bezieht sich auf ausgehende Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="507bc-134">Works similarly to the NOTIFY_BEGIN_INBOUND_FLUSH flag, but refers to outbound messages.</span></span> <span data-ttu-id="507bc-135">Das Flag des geeigneten Status ist STATUS_OUTBOUND_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="507bc-135">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
<span data-ttu-id="507bc-136">NOTIFY_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="507bc-136">NOTIFY_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="507bc-137">Die MAPI-Warteschlange muss Weiterleiten der Nachricht kündigen, für die der _LppvData_ Parameter verweist auf den 32-Bit-Wert aus der **IXPLogon::SubmitMessage** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="507bc-137">The MAPI spooler must cancel transfer of the message for which the  _lppvData_ parameter points to the 32-bit value from the **IXPLogon::SubmitMessage** method call.</span></span> <span data-ttu-id="507bc-138">Das Flag NOTIFY_CANCEL_MESSAGE kann festgelegt werden, ohne der Adressbuchhierarchie zurückgibt **SubmitMessage**, **IXPLogon::StartMessage**oder **IXPLogon::EndMessage** -Methode aufrufen, die die Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="507bc-138">The NOTIFY_CANCEL_MESSAGE flag can be set without the transport provider having returned from the **SubmitMessage**, **IXPLogon::StartMessage**, or **IXPLogon::EndMessage** method call that is associated with the message.</span></span> <span data-ttu-id="507bc-139">Der Transportdienst muss so bald wie möglich aus der Einstiegspunkt zurückgeben, die die Nachricht wurde abgebrochen behandelt.</span><span class="sxs-lookup"><span data-stu-id="507bc-139">The transport provider must return as soon as possible from the entry point that is handling the canceled message.</span></span> <span data-ttu-id="507bc-140">Für eine eingehende Nachricht, die zurzeit verarbeitet wird, sollte der Adressbuchhierarchie speichern die eingehende Nachricht, wo sie derzeit gespeichert ist und das Dokument zum nächsten geeigneten Zeitpunkt erneut übermitteln.</span><span class="sxs-lookup"><span data-stu-id="507bc-140">For an inbound message that is currently being processed, the transport provider should save the incoming message wherever it is presently stored and deliver it again at the next convenient time.</span></span> <span data-ttu-id="507bc-141">Die Nachricht-Objektdaten, die bereits für die eingehende Nachricht gespeichert werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="507bc-141">The message object data already stored for the incoming message is discarded.</span></span> <span data-ttu-id="507bc-142">Wenn der Adressbuchhierarchie keine dieser 32-Bit-Wert jederzeit **StartMessage** oder **SubmitMessage** aktualisiert wurden, ist der Wert 0 für ausgehende Nachrichten und 1 für eingehende Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="507bc-142">If the transport provider did not update this 32-bit value at the **StartMessage** or **SubmitMessage** time, the value is 0 for outbound messages and 1 for inbound messages.</span></span> 
    
<span data-ttu-id="507bc-143">NOTIFY_END_INBOUND</span><span class="sxs-lookup"><span data-stu-id="507bc-143">NOTIFY_END_INBOUND</span></span> 
  
> <span data-ttu-id="507bc-144">Eingehende Vorgänge müssen für diesen Anbieter Transport diese erlöschen.</span><span class="sxs-lookup"><span data-stu-id="507bc-144">Inbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="507bc-145">Die MAPI-Warteschlange nicht mehr mit der **Umfrage** -Methode und NOTIFY_NEWMAIL für diese Sitzung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="507bc-145">The MAPI spooler ceases to use the **Poll** method and ignores NOTIFY_NEWMAIL for this session.</span></span> <span data-ttu-id="507bc-146">In-Process-Nachrichten müssen abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-146">In-process messages should be completed.</span></span> <span data-ttu-id="507bc-147">Die Status-Tabellenzeile für die Sitzung Transport sollte durch Aufrufen von [ModifyStatusRow](imapisupport-modifystatusrow.md) vor der Rückgabe aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-147">The status table row for the transport session should be updated by calling [ModifyStatusRow](imapisupport-modifystatusrow.md) before returning.</span></span> <span data-ttu-id="507bc-148">Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_INBOUND schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="507bc-148">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="507bc-149">NOTIFY_END_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="507bc-149">NOTIFY_END_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="507bc-150">Der Transportdienst aus dem eingehende flush-Modus betrachten benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="507bc-150">Notifies the transport provider to come out of inbound flush mode.</span></span> <span data-ttu-id="507bc-151">Der Transportdienst sollten nicht beendet, herunterladen, aber herunterladen im Hintergrund ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="507bc-151">The transport provider should not stop downloading, but downloading should be done in the background.</span></span> <span data-ttu-id="507bc-152">Die Status-Tabellenzeile für die Sitzung Transport sollte durch Aufrufen von **ModifyStatusRow** beim Einhalten der Adressbuchhierarchie dieser Benachrichtigung kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-152">The status table row for the transport session should be updated by calling **ModifyStatusRow** when the transport provider can comply with this notification.</span></span> 
    
<span data-ttu-id="507bc-153">NOTIFY_END_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="507bc-153">NOTIFY_END_OUTBOUND</span></span> 
  
> <span data-ttu-id="507bc-154">Ausgehende Vorgänge müssen für diesen Anbieter Transport diese erlöschen.</span><span class="sxs-lookup"><span data-stu-id="507bc-154">Outbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="507bc-155">Die MAPI-Warteschlange nicht mehr **SubmitMessage** aufrufen und ignoriert die **SpoolerNotify** NOTIFY_READYTOSEND-Flag.</span><span class="sxs-lookup"><span data-stu-id="507bc-155">The MAPI spooler ceases to call **SubmitMessage** and ignores the **SpoolerNotify** NOTIFY_READYTOSEND flag.</span></span> <span data-ttu-id="507bc-156">Wenn es eine ausgehende Nachricht gerade gesendet wird ist, nicht beendet werden soll. Verwenden Sie das NOTIFY_CANCEL_MESSAGE-Flag, um Übermittlung einer Nachricht zu beenden.</span><span class="sxs-lookup"><span data-stu-id="507bc-156">If there is an outbound message currently being sent, it should not be stopped; to stop delivery of a message, use the NOTIFY_CANCEL_MESSAGE flag.</span></span> <span data-ttu-id="507bc-157">Die Tabellenzeile Status für diese Sitzung sollte durch Aufrufen von **ModifyStatusRow** vor der Rückgabe aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="507bc-157">The status table row for this session should be updated by calling **ModifyStatusRow** before returning.</span></span> <span data-ttu-id="507bc-158">Die Flags NOTIFY_END_INBOUND und NOTIFY_BEGIN_OUTBOUND schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="507bc-158">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="507bc-159">NOTIFY_END_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="507bc-159">NOTIFY_END_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="507bc-160">Works bezieht sich auf ähnliche Weise auf NOTIFY_END_INBOUND_FLUSH, aber auf ausgehende Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="507bc-160">Works similarly to NOTIFY_END_INBOUND_FLUSH, but refers to outbound messages.</span></span> <span data-ttu-id="507bc-161">Das Flag des geeigneten Status ist STATUS_OUTBOUND_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="507bc-161">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
 <span data-ttu-id="507bc-162">_lppvData_</span><span class="sxs-lookup"><span data-stu-id="507bc-162">_lppvData_</span></span>
  
> <span data-ttu-id="507bc-163">[out] Ein Zeiger auf einen Zeiger auf Daten.</span><span class="sxs-lookup"><span data-stu-id="507bc-163">[out] A pointer to a pointer to event-specific data.</span></span> <span data-ttu-id="507bc-164">Weitere Informationen dazu, welche _LppvData_ gibt an finden Sie in der Beschreibung für den Parameter _LpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="507bc-164">For more information about what  _lppvData_ specifies, see the description for the  _lpulFlags_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="507bc-165">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="507bc-165">Return value</span></span>

<span data-ttu-id="507bc-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="507bc-166">S_OK</span></span> 
  
> <span data-ttu-id="507bc-167">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="507bc-167">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="507bc-168">Hinweise</span><span class="sxs-lookup"><span data-stu-id="507bc-168">Remarks</span></span>

<span data-ttu-id="507bc-169">Die MAPI-Warteschlange die **IXPLogon::TransportNotify** -Methode aufgerufen, um der Adressbuchhierarchie über Ereignisse signalisieren für die Benachrichtigung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="507bc-169">The MAPI spooler calls the **IXPLogon::TransportNotify** method to signal the transport provider about events for which notification has been requested.</span></span> <span data-ttu-id="507bc-170">Diese Ereignisse enthalten eine MAPI-Warteschlange Anforderung zur Übertragung einer Nachricht, Anfang oder Ende eingehende oder ausgehende Transport-Vorgänge und Anfang oder Ende eines Vorgangs zum Löschen einer Warteschlange eingehende oder ausgehende Nachrichten Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="507bc-170">These events include a MAPI spooler request to cancel a message transfer, the beginning or ending of inbound or outbound transport operations, and the beginning or ending of an operation to clear an inbound or outbound message queue.</span></span> 
  
<span data-ttu-id="507bc-171">Wenn der Benutzer versucht, eine Nachricht abzubrechen, die zuvor der Adressbuchhierarchie zurückgestellt wurde, ruft die MAPI-Warteschlange **TransportNotify**, in dem NOTIFY_ABORT_DEFERRED und NOTIFY_CANCEL_MESSAGE-Flag in _UlFlags_übergeben.</span><span class="sxs-lookup"><span data-stu-id="507bc-171">When the user tries to cancel a message that the transport provider has previously deferred, the MAPI spooler calls **TransportNotify**, passing in both the NOTIFY_ABORT_DEFERRED and NOTIFY_CANCEL_MESSAGE flags in  _ulFlags_.</span></span> <span data-ttu-id="507bc-172">Wenn die MAPI-Warteschlange meldet sich ab und immer Nachrichten in der Warteschlange noch, übergibt sie nur NOTIFY_ABORT_DEFERRED in _UlFlags_ beim **TransportNotify**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="507bc-172">If the MAPI spooler is logging off and still has messages in the queue, it passes only NOTIFY_ABORT_DEFERRED in  _ulFlags_ when it calls **TransportNotify**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="507bc-173">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="507bc-173">Notes to implementers</span></span>

<span data-ttu-id="507bc-174">Der Anbieter muss Zugriff auf seine Daten für dieses Anrufs synchronisieren, da die MAPI-Warteschlange diese Methode für ein anderes Fenster aus einem anderen Thread der Ausführung oder aus einer Prozedur aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="507bc-174">The provider must synchronize access to its data on this call, because the MAPI spooler can invoke this method from another thread of execution or from a procedure for a different window.</span></span> <span data-ttu-id="507bc-175">Dies tritt wahrscheinlich auf, wenn die MAPI-Warteschlange den Abbruch einer Nachricht signalisiert, dass der Adressbuchhierarchie senden gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="507bc-175">This will most likely occur when the MAPI spooler signals the cancellation of a message that the transport provider has started sending.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="507bc-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="507bc-176">See also</span></span>

- [<span data-ttu-id="507bc-177">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="507bc-177">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md) 
- [<span data-ttu-id="507bc-178">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="507bc-178">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md) 
- [<span data-ttu-id="507bc-179">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="507bc-179">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md) 
- [<span data-ttu-id="507bc-180">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="507bc-180">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md) 
- [<span data-ttu-id="507bc-181">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="507bc-181">IXPLogon::Poll</span></span>](ixplogon-poll.md)
- [<span data-ttu-id="507bc-182">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="507bc-182">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
- [<span data-ttu-id="507bc-183">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="507bc-183">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
- [<span data-ttu-id="507bc-184">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="507bc-184">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="507bc-185">IXPLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="507bc-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)
