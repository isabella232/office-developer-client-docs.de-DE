---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423769"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="b0016-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="b0016-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="b0016-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0016-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0016-105">Benachrichtigt den MAPI-Spooler über eine Statusänderung oder eine Dienstanforderung.</span><span class="sxs-lookup"><span data-stu-id="b0016-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="b0016-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0016-106">Parameters</span></span>

 <span data-ttu-id="b0016-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0016-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b0016-108">[in] Eine Bitmaske mit Flags, die den Typ der Benachrichtigung angibt.</span><span class="sxs-lookup"><span data-stu-id="b0016-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="b0016-109">Transportanbieter können alle Flags mit Ausnahme von NOTIFY_NEWMAIL_RECEIVED. Nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind für Nachrichtenspeicheranbieter gültig.</span><span class="sxs-lookup"><span data-stu-id="b0016-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="b0016-110">Die folgenden Kennzeichen sind für den  _ulFlags-Parameter_ gültig:</span><span class="sxs-lookup"><span data-stu-id="b0016-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="b0016-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b0016-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="b0016-112">Registriert eine Anforderung zum Ändern der Konfiguration des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="b0016-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="b0016-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="b0016-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="b0016-114">Beim Transportanbieter ist ein nicht behebbarer Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b0016-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="b0016-115">Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR  _den Parameter lpvData_ für Transportanbieteraufrufe verwenden, schließen sich diese Flags gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="b0016-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="b0016-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="b0016-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="b0016-117">Fordert einen kritischen Abschnitt für den Transportanbieter an.</span><span class="sxs-lookup"><span data-stu-id="b0016-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="b0016-118">Der  _lpvData-Parameter_ ist nicht definiert und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b0016-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="b0016-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="b0016-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="b0016-120">Der MAPI-Spooler sollte alle neu empfangenen Nachrichten zum nächsten verfügbaren Zeitpunkt herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b0016-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="b0016-121">Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0016-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="b0016-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="b0016-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="b0016-123">Im Nachrichtenspeicher wurde eine neue Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="b0016-123">A new message has been received in the message store.</span></span> <span data-ttu-id="b0016-124">Der  _lpvData-Parameter_ zeigt auf [eine NEWMAIL_NOTIFICATION,](newmail_notification.md) die die Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b0016-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="b0016-125">Dieses Flag wird für Nachrichtenspeicheranbieter verwendet, die eng mit Transportanbietern gekoppelt sind und ignoriert werden, wenn der Speicheranbieter mit dem MAPI_NO_MAIL angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b0016-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="b0016-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="b0016-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="b0016-127">Gibt einen kritischen Abschnitt frei, der mit einem vorherigen Aufruf von **SpoolerNotify** mit  _ulFlags_ auf NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="b0016-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="b0016-128">Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0016-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="b0016-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="b0016-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="b0016-130">Der Transport- oder Nachrichtenspeicheranbieter kann Nachrichten senden.</span><span class="sxs-lookup"><span data-stu-id="b0016-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="b0016-131">Der  _lpvData-Parameter_ ist nicht definiert und sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0016-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="b0016-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="b0016-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="b0016-133">Nun sollte eine zuvor verzögerte Nachricht gesendet werden, und der Transportanbieter sollte benachrichtigt werden, wenn die Nachricht mithilfe eines Aufrufs der [IXPLogon::SubmitMessage-Methode](ixplogon-submitmessage.md) zugestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0016-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="b0016-134">Der Eintragsbezeichner der verzögerten Nachricht ist in einer [SBinary-Struktur](sbinary.md) enthalten, auf die von _lpvData verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="b0016-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="b0016-135">Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR  _lpvData-Parameter_ verwenden, schließen sich diese Flags gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="b0016-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="b0016-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="b0016-136">_lpvData_</span></span>
  
> <span data-ttu-id="b0016-137">[in] Ein Zeiger auf zugeordnete Daten, die auf eine Benachrichtigung anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="b0016-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="b0016-138">Der  _lpvData-Parameter_ verweist nur dann auf gültige Daten, wenn die folgenden Flags festgelegt sind (_lpvData_ ist NULL, wenn  _ulFlags_ auf die anderen Benachrichtigungstypen festgelegt ist):</span><span class="sxs-lookup"><span data-stu-id="b0016-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="b0016-139">**_ulFlags-Einstellung_**</span><span class="sxs-lookup"><span data-stu-id="b0016-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="b0016-140">**_lpvData-Wert_**</span><span class="sxs-lookup"><span data-stu-id="b0016-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0016-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="b0016-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="b0016-142">Informationen zum Fehler.</span><span class="sxs-lookup"><span data-stu-id="b0016-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="b0016-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="b0016-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="b0016-144">Eine **NEWMAIL_NOTIFICATION,** die Informationen zur neu zugestellten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="b0016-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="b0016-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="b0016-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="b0016-146">Eine **SBinary-Struktur,** die den Eintragsbezeichner der verzögerten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="b0016-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="b0016-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0016-147">Return value</span></span>

<span data-ttu-id="b0016-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0016-148">S_OK</span></span> 
  
> <span data-ttu-id="b0016-149">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b0016-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0016-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0016-150">Remarks</span></span>

<span data-ttu-id="b0016-151">Die **IMAPISupport::SpoolerNotify-Methode** wird für Nachrichtenspeicher- und Transportanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="b0016-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="b0016-152">Diese Anbieter rufen **SpoolerNotify auf,** um den MAPI-Spooler über eine Statusänderung oder eine Dienstanforderung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="b0016-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="b0016-153">**SpoolerNotify** wird hauptsächlich von Transportanbietern aufgerufen und kann jederzeit während der Sitzung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b0016-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="b0016-154">Hinweise zu Transportanbietern</span><span class="sxs-lookup"><span data-stu-id="b0016-154">Notes to Transport Providers</span></span>

<span data-ttu-id="b0016-155">Wenn Sie ihre Konfiguration des Transportanbieters geändert haben, rufen **Sie SpoolerNotify** auf, und legen Sie  _ulFlags auf_ NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="b0016-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="b0016-156">**SpoolerNotify** antwortet, indem die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) zum Abfragen einer Änderung der unterstützten Adresstypen aufruft.</span><span class="sxs-lookup"><span data-stu-id="b0016-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="b0016-157">Wenn Sie einen kritischen Abschnitt benötigen, um eine unterbrechungsfreie Verarbeitung sicherzustellen, rufen **Sie SpoolerNotify** auf, wenn  _ulFlags_ auf NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="b0016-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="b0016-158">Durch Festlegen dieses Kennzeichens wird der MAPI-Spooler darüber informiert, dass er die [Methoden IXPLogon::Idle](ixplogon-idle.md) und [IXPLogon::P oll](ixplogon-poll.md) nicht aufrufen sollte.</span><span class="sxs-lookup"><span data-stu-id="b0016-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="b0016-159">Wenn Sie einen kritischen Abschnitt geöffnet haben, geben MAPI_E_BUSY zurück, wenn die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b0016-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="b0016-160">Wenn Sie den kritischen Abschnitt abgeschlossen haben, rufen Sie **SpoolerNotify** erneut auf, und  _ulFlags_ ist auf NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="b0016-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="b0016-161">Wenn Ihr Remotetransportanbieter beispielsweise Nachrichten hochladet, müssen Sie möglicherweise zulassen, dass ein Benutzer eine Telefonnummer eingeben kann, um die Remoteverbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b0016-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="b0016-162">Bevor Sie die Dialogfeldprozedur durchschleifen, sollten Sie einen kritischen Abschnitt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="b0016-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="b0016-163">Wenn der Benutzer das Dialogfeld schließt und die Dialogfeldprozedur beendet, sollten Sie den kritischen Abschnitt los.</span><span class="sxs-lookup"><span data-stu-id="b0016-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="b0016-164">Wenn Sie  _ulFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, ruft der MAPI-Spooler keine weiteren Aufrufe an den Anbieter ab, es sei denn, er wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="b0016-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="b0016-165">Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR von der [IXPLogon::StartMessage-](ixplogon-startmessage.md) oder [IXPLogon::SubmitMessage-Methode](ixplogon-submitmessage.md) aufrufen, geben Sie mit einem entsprechenden Fehlerwert aus dem **StartMessage-** oder \*\* SubmitMessage \*\*-Aufruf unmittelbar nach dem **SpoolerNotify-Aufruf** zurück.</span><span class="sxs-lookup"><span data-stu-id="b0016-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="b0016-166">Wenn Ihr Transportanbieter von einer Bedingung wiederhergestellt wurde, die zuvor zu einem Fehler führte, rufen Sie **SpoolerNotify** auf, wenn  _ulFlags_ auf NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="b0016-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="b0016-167">Dieses Flag gibt an, dass der Anbieter wieder für die Verarbeitung von Nachrichten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="b0016-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="b0016-168">Hinweise zu Nachrichtenanbietern Store</span><span class="sxs-lookup"><span data-stu-id="b0016-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="b0016-169">Rufen **Sie SpoolerNotify** auf, übergeben Sie das NOTIFY_READYTOSEND-Flag in _ulFlags,_ bevor Sie den ersten Aufruf von [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage machen.**</span><span class="sxs-lookup"><span data-stu-id="b0016-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="b0016-170">Dieser Aufruf **von SpoolerNotify** muss nur einmal pro Sitzung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="b0016-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="b0016-171">Wenn Ihr Nachrichtenspeicheranbieter eng mit einem Transportanbieter gekoppelt ist und **Sie SpoolerNotify** mit  _ulFlags_ aufrufen, die auf NOTIFY_NEWMAIL_RECEIVED festgelegt sind, öffnet der MAPI-Spooler die neue Nachricht und beginnt mit der Verarbeitung der neuen Message Hook-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b0016-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="b0016-172">Nach Abschluss der Verarbeitung ruft der MAPI-Spooler die [IMsgStore::NotifyNewMail-Methode](imsgstore-notifynewmail.md) auf, um Sie über Ihre eigene neue Nachricht zu informieren.</span><span class="sxs-lookup"><span data-stu-id="b0016-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="b0016-173">Weitere Informationen zum Aufrufen von **SpoolerNotify** finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b0016-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="b0016-174">Implementieren der FlushQueues-Methode</span><span class="sxs-lookup"><span data-stu-id="b0016-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="b0016-175">Interagieren mit dem MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="b0016-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="b0016-176">Nachrichtenempfangsmodell</span><span class="sxs-lookup"><span data-stu-id="b0016-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="b0016-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0016-177">See also</span></span>



[<span data-ttu-id="b0016-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="b0016-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="b0016-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="b0016-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="b0016-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="b0016-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="b0016-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0016-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

