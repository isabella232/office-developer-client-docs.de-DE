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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792418"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="fc3e8-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="fc3e8-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="fc3e8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc3e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc3e8-105">Benachrichtigt die MAPI-Warteschlange von einer Änderung im Status oder eine Anforderung für den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="fc3e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc3e8-106">Parameters</span></span>

 <span data-ttu-id="fc3e8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc3e8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fc3e8-108">[in] Eine Bitmaske aus Flags, die den Typ der Benachrichtigung angibt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="fc3e8-109">Transportanbieter können alle außer NOTIFY_NEWMAIL_RECEIVED Kennzeichen festgelegt. nur NOTIFY_NEWMAIL_RECEIVED und NOTIFY_READTOSEND sind gültig für eine Nachricht-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="fc3e8-110">Die folgenden Kennzeichen sind für den Parameter _UlFlags_ gültig:</span><span class="sxs-lookup"><span data-stu-id="fc3e8-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="fc3e8-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="fc3e8-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="fc3e8-112">Eine Anforderung zum Ändern der Konfiguration der Adressbuchhierarchie registriert.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="fc3e8-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="fc3e8-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="fc3e8-114">Der Transportdienst aufgetretenen Fehler nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="fc3e8-115">Da NOTIFY_SENTDEFERRED und NOTIFY_CRITICAL_ERROR den Parameter _LpvData_ für Transport Anbieter Anrufe verwenden, sind diese Flags schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="fc3e8-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="fc3e8-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="fc3e8-117">Fordert einen kritischen Abschnitt für den Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="fc3e8-118">Der Parameter _LpvData_ ist nicht definiert und NULL sein.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="fc3e8-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="fc3e8-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="fc3e8-120">Die MAPI-Warteschlange sollten unter der nächsten verfügbaren Zeit neu empfangenen Nachrichten herunterladen.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="fc3e8-121">Der Parameter _LpvData_ ist nicht definiert und auf NULL festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="fc3e8-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="fc3e8-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="fc3e8-123">Eine neue Nachricht wurde im Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-123">A new message has been received in the message store.</span></span> <span data-ttu-id="fc3e8-124">Der Parameter _LpvData_ verweist auf eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die die Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="fc3e8-125">Dieses Kennzeichen werden für die Nachricht-Anbieter, die eng mit Anbietern Transport verknüpft sind, und werden ignoriert, wenn der Anbieter mit dem Flag MAPI_NO_MAIL angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="fc3e8-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="fc3e8-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="fc3e8-127">Gibt einen kritischen Abschnitt, der mit einem vorherigen Aufruf von **SpoolerNotify** , mit _UlFlags_ auf NOTIFY_CRITSEC festgelegt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="fc3e8-128">Der Parameter _LpvData_ ist nicht definiert und auf NULL festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="fc3e8-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="fc3e8-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="fc3e8-130">Der Informationsdienst Transport oder einer Nachricht ist bereit zum Senden von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="fc3e8-131">Der Parameter _LpvData_ ist nicht definiert und auf NULL festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="fc3e8-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="fc3e8-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="fc3e8-133">Jetzt sollte eine zuvor zurückgestellte Nachricht gesendet werden, und der Adressbuchhierarchie benachrichtigt werden soll, wenn die Nachricht bereitgestellt werden, mit einem Aufruf der [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methode ist.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="fc3e8-134">Die Eintrags-ID der zurückgestellte Nachricht ist in eine [SBinary](sbinary.md) -Struktur, die auf den _LpvData_enthalten.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="fc3e8-135">Da NOTIFY_SENTDEFERRED und NOTIFY_CRITICAL_ERROR den _LpvData_ -Parameter verwenden, sind diese Flags schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="fc3e8-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="fc3e8-136">_lpvData_</span></span>
  
> <span data-ttu-id="fc3e8-137">[in] Ein Zeiger auf die zugehörigen Daten für eine Benachrichtigung gelten.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="fc3e8-138">Der _LpvData_ -Parameter verweist auf gültige Daten nur, wenn die folgenden Kennzeichen festgelegt werden (_LpvData_ ist NULL, wenn _UlFlags_ auf anderen Benachrichtigungstypen festgelegt ist):</span><span class="sxs-lookup"><span data-stu-id="fc3e8-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="fc3e8-139">**_UlFlags_ -Einstellung**</span><span class="sxs-lookup"><span data-stu-id="fc3e8-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="fc3e8-140">**_LpvData_ Wert**</span><span class="sxs-lookup"><span data-stu-id="fc3e8-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc3e8-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="fc3e8-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="fc3e8-142">Informationen zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="fc3e8-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="fc3e8-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="fc3e8-144">Eine **NEWMAIL_NOTIFICATION** -Struktur, die Informationen über die neu gesendete Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="fc3e8-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="fc3e8-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="fc3e8-146">Eine **SBinary** -Struktur, die Eintrags-ID der zurückgestellte Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="fc3e8-147">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fc3e8-147">Return value</span></span>

<span data-ttu-id="fc3e8-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc3e8-148">S_OK</span></span> 
  
> <span data-ttu-id="fc3e8-149">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc3e8-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc3e8-150">Remarks</span></span>

<span data-ttu-id="fc3e8-151">Die **IMAPISupport::SpoolerNotify** -Methode wird für die Nachricht implementiert speichern und transport-Provider Unterstützungsobjekte.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="fc3e8-152">Diese Anbieter rufen Sie **SpoolerNotify** , um die MAPI-Warteschlange von einer Änderung im Status oder eine Anforderung für den Dienst zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="fc3e8-153">**SpoolerNotify** wird hauptsächlich von Transportanbieter aufgerufen und können jederzeit während der Sitzung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="fc3e8-154">Hinweise für Transport-Anbieter</span><span class="sxs-lookup"><span data-stu-id="fc3e8-154">Notes to Transport Providers</span></span>

<span data-ttu-id="fc3e8-155">Wenn Sie Ihrer Anbieterkonfiguration Transport geändert haben, rufen Sie **SpoolerNotify** und _UlFlags_ auf NOTIFY_CONFIG_CHANGED festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="fc3e8-156">Durch Aufrufen der [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode, um die Abfrage für eine Änderung in unterstützte-Adresstypen auf **SpoolerNotify** reagiert.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="fc3e8-157">Wenn Sie einen kritischen Abschnitt um sicherzustellen, dass ununterbrochenen Verarbeitung benötigen, rufen Sie **SpoolerNotify** mit _UlFlags_ auf NOTIFY_CRITSEC festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="fc3e8-158">Dieses Flag festlegen informiert der MAPI-Warteschlange an, dass die Methoden [IXPLogon::Idle](ixplogon-idle.md) und [IXPLogon::Poll](ixplogon-poll.md) nicht aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="fc3e8-159">Während Sie einen kritischen Abschnitt öffnen haben, MAPI_E_BUSY zurückgeben, wenn die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="fc3e8-160">Wenn Sie mit den kritischen Abschnitt fertig sind, stellen Sie einen weiteren Anruf zu **SpoolerNotify** mit _UlFlags_ auf NOTIFY_NONCRIT festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="fc3e8-161">Wenn Ihre remote Adressbuchhierarchie wird gerade Nachrichten hochladen, müssen Sie einen Benutzer geben Sie eine Telefonnummer ein, um die remote-Verbindung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="fc3e8-162">Bevor Sie das Dialogfeld Feld Verfahren durchlaufen haben, sollten Sie einen kritischen Abschnitt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="fc3e8-163">Wenn der Benutzer das Dialogfeld geschlossen wird, sollte, auf dem Sie den kritischen Abschnitt freigeben wird das Dialogfeld Feld Verfahren beendet.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="fc3e8-164">Wenn Sie _UlFlags_ auf NOTIFY_CRITICAL_ERROR festlegen, wird die MAPI-Warteschlange keine weiteren Aufrufe an den Anbieter mit Ausnahme von an freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="fc3e8-165">Wenn Sie **SpoolerNotify** mit NOTIFY_CRITICAL_ERROR legen Sie die [IXPLogon::StartMessage](ixplogon-startmessage.md) oder [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methoden aufrufen, mit einem entsprechenden Fehlerwert zurückgeben, aus der **StartMessage** oder ** SubmitMessage ** aufrufen unmittelbar nach dem Aufruf **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="fc3e8-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or ** SubmitMessage ** call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="fc3e8-166">Wenn Ihre Adressbuchhierarchie aus einer Bedingung, die zuvor Fehler verursacht hat wiederhergestellt, rufen Sie **SpoolerNotify** mit _UlFlags_ auf NOTIFY_READYTOSEND festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="fc3e8-167">Dieses Kennzeichen gibt an, dass der Anbieter erneut bereit, um Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="fc3e8-168">Hinweise für Nachrichtenspeicher-Anbieter</span><span class="sxs-lookup"><span data-stu-id="fc3e8-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="fc3e8-169">Rufen Sie **SpoolerNotify**, das NOTIFY_READYTOSEND-Flag in _UlFlags_, übergeben, bevor Sie Ihre erste [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="fc3e8-170">Dieser Aufruf von **SpoolerNotify** muss nur einmal pro Sitzung vorgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="fc3e8-171">Wenn Ihre Nachrichtenanbieter eng verknüpft ist mit einer Transport-Anbieter und Sie rufen **SpoolerNotify** _UlFlags_ auf NOTIFY_NEWMAIL_RECEIVED festgelegt, die MAPI-Warteschlange wird die neue Nachricht geöffnet, und mit der Verarbeitung der neuen Nachricht Hook-Funktion beginnt.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="fc3e8-172">Nach Abschluss der Verarbeitung Ruft die MAPI-Warteschlange die [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) -Methode, um Sie der neuen Nachricht informiert.</span><span class="sxs-lookup"><span data-stu-id="fc3e8-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="fc3e8-173">Weitere Informationen zum Aufrufen von **SpoolerNotify**finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="fc3e8-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="fc3e8-174">Implementieren der FlushQueues-Methode</span><span class="sxs-lookup"><span data-stu-id="fc3e8-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="fc3e8-175">Interaktion mit dem MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="fc3e8-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="fc3e8-176">Nachrichtenempfangsmodell</span><span class="sxs-lookup"><span data-stu-id="fc3e8-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="fc3e8-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc3e8-177">See also</span></span>



[<span data-ttu-id="fc3e8-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="fc3e8-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="fc3e8-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="fc3e8-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="fc3e8-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fc3e8-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="fc3e8-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc3e8-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

