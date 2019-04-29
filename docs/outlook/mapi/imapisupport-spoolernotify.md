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
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="624bb-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="624bb-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="624bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="624bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="624bb-105">Benachrichtigt den MAPI-Spooler über eine Änderung des Status oder eine Anforderung für Dienst.</span><span class="sxs-lookup"><span data-stu-id="624bb-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="624bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="624bb-106">Parameters</span></span>

 <span data-ttu-id="624bb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="624bb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="624bb-108">in Eine Bitmaske von Flags, die den Benachrichtigungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="624bb-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="624bb-109">Transport Anbieter können alle Flags festlegen, mit Ausnahme von NOTIFY_NEWMAIL_RECEIVED; nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind für Nachrichtenspeicher Anbieter gültig.</span><span class="sxs-lookup"><span data-stu-id="624bb-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="624bb-110">Die folgenden Flags sind für den _ulFlags_ -Parameter gültig:</span><span class="sxs-lookup"><span data-stu-id="624bb-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="624bb-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="624bb-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="624bb-112">Registriert eine Anforderung zum Ändern der Konfiguration des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="624bb-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="624bb-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="624bb-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="624bb-114">Ein nicht behebbarer Fehler ist beim Transportanbieter aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="624bb-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="624bb-115">Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR den _lpvData_ -Parameter für Transportanbieter Aufrufe verwenden, schließen sich diese Flags gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="624bb-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="624bb-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="624bb-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="624bb-117">Fordert einen kritischen Abschnitt für den Transportanbieter an.</span><span class="sxs-lookup"><span data-stu-id="624bb-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="624bb-118">Der _lpvData_ -Parameter ist nicht definiert und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="624bb-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="624bb-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="624bb-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="624bb-120">Der MAPI-Spooler sollte alle neu empfangenen Nachrichten zum nächsten verfügbaren Zeitpunkt herunterladen.</span><span class="sxs-lookup"><span data-stu-id="624bb-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="624bb-121">Der Parameter _lpvData_ ist nicht definiert und sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="624bb-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="624bb-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="624bb-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="624bb-123">Im Nachrichtenspeicher wurde eine neue Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="624bb-123">A new message has been received in the message store.</span></span> <span data-ttu-id="624bb-124">Der _lpvData_ -Parameter verweist auf eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die die Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="624bb-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="624bb-125">Dieses Flag wird für Nachrichtenspeicher Anbieter verwendet, die eng mit Transportanbietern gekoppelt sind, und wird ignoriert, wenn der Informationsspeicher Anbieter mit dem MAPI_NO_MAIL-Kennzeichen Satz angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="624bb-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="624bb-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="624bb-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="624bb-127">Gibt einen kritischen Abschnitt zurück, der mit einem vorherigen Aufruf von **SpoolerNotify** abgerufen wurde, wobei _ulFlags_ auf NOTIFY_CRITSEC festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="624bb-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="624bb-128">Der Parameter _lpvData_ ist nicht definiert und sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="624bb-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="624bb-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="624bb-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="624bb-130">Der Transport-oder Nachrichtenspeicher Anbieter ist bereit, Nachrichten zu senden.</span><span class="sxs-lookup"><span data-stu-id="624bb-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="624bb-131">Der Parameter _lpvData_ ist nicht definiert und sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="624bb-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="624bb-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="624bb-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="624bb-133">Eine zuvor verzögerte Nachricht sollte jetzt gesendet werden, und der Transportanbieter sollte benachrichtigt werden, wenn die Nachricht mithilfe eines Aufrufs der [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="624bb-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="624bb-134">Der Eintragsbezeichner der verzögerten Nachricht ist in einer [SBinary](sbinary.md) -Struktur enthalten, auf die durch _lpvData_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="624bb-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="624bb-135">Da sowohl NOTIFY_SENTDEFERRED als auch NOTIFY_CRITICAL_ERROR den _lpvData_ -Parameter verwenden, schließen sich diese Flags gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="624bb-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="624bb-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="624bb-136">_lpvData_</span></span>
  
> <span data-ttu-id="624bb-137">in Ein Zeiger auf zugeordnete Daten, die für eine Benachrichtigung gelten.</span><span class="sxs-lookup"><span data-stu-id="624bb-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="624bb-138">Der Parameter _lpvData_ zeigt nur dann auf gültige Daten, wenn die folgenden Flags festgelegt sind (_lpvData_ ist NULL, wenn _ulFlags_ auf andere Benachrichtigungstypen festgelegt ist):</span><span class="sxs-lookup"><span data-stu-id="624bb-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="624bb-139">**_ulFlags_ -Einstellung**</span><span class="sxs-lookup"><span data-stu-id="624bb-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="624bb-140">**_lpvData_ -Wert**</span><span class="sxs-lookup"><span data-stu-id="624bb-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="624bb-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="624bb-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="624bb-142">Informationen zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="624bb-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="624bb-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="624bb-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="624bb-144">Eine **NEWMAIL_NOTIFICATION** -Struktur, die Informationen über die neu zugestellte Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="624bb-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="624bb-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="624bb-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="624bb-146">Eine **SBinary** -Struktur, die den Eintragsbezeichner der verzögerten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="624bb-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="624bb-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="624bb-147">Return value</span></span>

<span data-ttu-id="624bb-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="624bb-148">S_OK</span></span> 
  
> <span data-ttu-id="624bb-149">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="624bb-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="624bb-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="624bb-150">Remarks</span></span>

<span data-ttu-id="624bb-151">Die **IMAPISupport:: SpoolerNotify** -Methode wird für Nachrichtenspeicher-und Transportanbieter-Support Objekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="624bb-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="624bb-152">Diese Anbieter rufen **SpoolerNotify** auf, um den MAPI-Spooler über eine Änderung des Status oder eine Anforderung für Dienst zu informieren.</span><span class="sxs-lookup"><span data-stu-id="624bb-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="624bb-153">**SpoolerNotify** wird in erster Linie von Transportanbietern aufgerufen und kann jederzeit während der Sitzung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="624bb-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="624bb-154">Hinweise für Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="624bb-154">Notes to Transport Providers</span></span>

<span data-ttu-id="624bb-155">Wenn Sie Ihre Transportanbieter Konfiguration geändert haben, rufen Sie **SpoolerNotify** auf, und legen Sie _ulFlags_ auf NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="624bb-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="624bb-156">**SpoolerNotify** antwortet durch Aufrufen der [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode, um eine Änderung der unterstützten Adresstypen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="624bb-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="624bb-157">Wenn Sie einen kritischen Abschnitt benötigen, um eine ununterbrochene Verarbeitung sicherzustellen, rufen Sie **SpoolerNotify** mit _ulFlags_ auf NOTIFY_CRITSEC festgelegt.</span><span class="sxs-lookup"><span data-stu-id="624bb-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="624bb-158">Wenn Sie dieses Flag festlegen, wird der MAPI-Spooler darüber informiert, dass die [IXPLogon:: idle](ixplogon-idle.md) -und [IXPLogon::P-oll](ixplogon-poll.md) -Methoden nicht aufgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="624bb-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="624bb-159">Wenn ein kritischer Abschnitt geöffnet ist, geben Sie MAPI_E_BUSY immer dann zurück, wenn die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="624bb-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="624bb-160">Wenn Sie den kritischen Abschnitt beendet haben, führen Sie einen weiteren Aufruf von **SpoolerNotify** aus, wobei _ulFlags_ auf NOTIFY_NONCRIT festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="624bb-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="624bb-161">Wenn beispielsweise der Remote Transport-Anbieter Nachrichten hochgeladen hat, müssen Sie möglicherweise einem Benutzer die Eingabe einer Telefonnummer gestatten, um die Remoteverbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="624bb-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="624bb-162">Bevor Sie die Dialogfeldprozedur durchlaufen, sollten Sie einen kritischen Abschnitt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="624bb-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="624bb-163">Wenn der Benutzer das Dialogfeld schließt und die Dialogfeldprozedur beendet, sollten Sie den kritischen Abschnitt freigeben.</span><span class="sxs-lookup"><span data-stu-id="624bb-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="624bb-164">Wenn Sie _ulFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, führt der MAPI-Spooler keine weiteren Aufrufe an den Anbieter aus, außer dass dieser freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="624bb-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="624bb-165">Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR-Set aus der [IXPLogon:: StartMessage](ixplogon-startmessage.md) -oder [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methode aufrufen, geben Sie mit einem entsprechenden Fehlerwert aus dem **StartMessage** oder \* \* SubmitMessage \* \* Call zurück. unmittelbar nach dem **SpoolerNotify** -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="624bb-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="624bb-166">Wenn der Transportanbieter von einer Bedingung wiederhergestellt wurde, die zuvor einen Fehler verursacht hat, rufen Sie **SpoolerNotify** mit _ulFlags_ auf NOTIFY_READYTOSEND festgelegt.</span><span class="sxs-lookup"><span data-stu-id="624bb-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="624bb-167">Dieses Flag gibt an, dass der Anbieter wieder für die Verarbeitung von Nachrichten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="624bb-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="624bb-168">Hinweise für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="624bb-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="624bb-169">Rufen Sie **SpoolerNotify**auf, und übergeben Sie das NOTIFY_READYTOSEND-Flag in _ulFlags_, bevor Sie den ersten aufruf an [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) in **IMessage:: SubmitMessage**durchführen.</span><span class="sxs-lookup"><span data-stu-id="624bb-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="624bb-170">Dieser Aufruf von **SpoolerNotify** muss nur einmal pro Sitzung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="624bb-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="624bb-171">Wenn der Nachrichtenspeicher Anbieter eng mit einem Transportanbieter gekoppelt ist und Sie **SpoolerNotify** aufrufen, wobei _ulFlags_ auf NOTIFY_NEWMAIL_RECEIVED festgelegt ist, wird die neue Nachricht vom MAPI-Spooler geöffnet und mit der Verarbeitung der neuen Nachrichten Hookfunktion begonnen.</span><span class="sxs-lookup"><span data-stu-id="624bb-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="624bb-172">Nach Abschluss der Verarbeitung ruft der MAPI-Spooler die [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) -Methode auf, um Sie über Ihre eigene neue Nachricht zu informieren.</span><span class="sxs-lookup"><span data-stu-id="624bb-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="624bb-173">Weitere Informationen zum Aufrufen von **SpoolerNotify**finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="624bb-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="624bb-174">Implementieren der FlushQueues-Methode</span><span class="sxs-lookup"><span data-stu-id="624bb-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="624bb-175">Interaktion mit dem MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="624bb-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="624bb-176">Nachrichtenempfangs Modell</span><span class="sxs-lookup"><span data-stu-id="624bb-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="624bb-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="624bb-177">See also</span></span>



[<span data-ttu-id="624bb-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="624bb-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="624bb-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="624bb-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="624bb-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="624bb-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="624bb-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="624bb-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

