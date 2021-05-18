---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317325"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="8fa1b-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="8fa1b-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="8fa1b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fa1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fa1b-105">Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf den Nachrichtenspeicher auswirken.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8fa1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa1b-106">Parameters</span></span>

 <span data-ttu-id="8fa1b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8fa1b-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8fa1b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8fa1b-110">[in] Ein Zeiger auf den Eintragsbezeichner des Ordners oder der Nachricht, über den Benachrichtigungen generiert werden sollen, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="8fa1b-111">Wenn  _lpEntryID_ auf NULL festgelegt ist, registriert **Advise** Benachrichtigungen im gesamten Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="8fa1b-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="8fa1b-113">[in] Eine Maske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, die der Anrufer interessiert und in die Registrierung einbezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="8fa1b-114">Jedem Ereignistyp ist eine entsprechende [NOTIFICATION-Struktur](notification.md) zugeordnet, die Informationen zum Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="8fa1b-115">Es folgen gültige Werte für den _ulEventMask-Parameter:_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="8fa1b-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="8fa1b-117">Registriert für Benachrichtigungen über schwerwiegende Fehler, z. B. unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="8fa1b-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="8fa1b-119">Registriert für Benachrichtigungen über Ereignisse, die für den jeweiligen Nachrichtenspeicheranbieter spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="8fa1b-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="8fa1b-121">Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="8fa1b-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="8fa1b-123">Registriert für Benachrichtigungen über die Erstellung eines neuen Ordners oder einer neuen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="8fa1b-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="8fa1b-125">Registriert für Benachrichtigungen über einen zu kopierenden Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="8fa1b-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="8fa1b-127">Registriert für Benachrichtigungen über einen zu löschenden Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="8fa1b-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="8fa1b-129">Registriert für Benachrichtigungen über einen zu ändernden Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="8fa1b-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="8fa1b-131">Registriert für Benachrichtigungen über einen verschobenen Ordner oder eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="8fa1b-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="8fa1b-133">Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="8fa1b-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="8fa1b-135">[in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="8fa1b-136">Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="8fa1b-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="8fa1b-138">[out] Ein Zeiger auf eine Nullnummer, die die Verbindung zwischen dem Ratensenkenobjekt des Anrufers und der Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="8fa1b-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="8fa1b-140">[in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="8fa1b-141">Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="8fa1b-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="8fa1b-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="8fa1b-143">[out] Ein Zeiger auf eine Verbindungsnummer ungleich Null, die die Verbindung zwischen dem Ratensenkenobjekt des Anrufers und dem Nachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8fa1b-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fa1b-144">Return value</span></span>

<span data-ttu-id="8fa1b-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fa1b-145">S_OK</span></span> 
  
> <span data-ttu-id="8fa1b-146">Die Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-146">The registration was successful.</span></span>
    
<span data-ttu-id="8fa1b-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8fa1b-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8fa1b-148">Der Nachrichtenspeicheranbieter unterstützt keine Registrierung für Benachrichtigungen über den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8fa1b-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fa1b-149">Remarks</span></span>

<span data-ttu-id="8fa1b-150">Mit **der IMsgStore::Advise-Methode** wird eine Verbindung zwischen dem Ratensenkenobjekt des Aufrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="8fa1b-151">Diese Verbindung wird verwendet, um Benachrichtigungen an die Ratensenke zu senden, wenn ein oder mehrere Ereignisse, wie im  _ulEventMask-Parameter_ angegeben, für das advise-Quellobjekt auftreten.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="8fa1b-152">Wenn der  _lpEntryID-Parameter_ auf einen gültigen Eintragsbezeichner verweist, ist die Advise-Quelle das durch diesen Eintragsbezeichner identifizierte Objekt.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="8fa1b-153">Wenn  _lpEntryID_ NULL ist, ist die Informationsquelle der Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="8fa1b-154">Zum Senden einer Benachrichtigung ruft der Nachrichtenspeicheranbieter oder mapI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der registrierten Hinweissenke auf.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="8fa1b-155">Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8fa1b-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8fa1b-156">Notes to implementers</span></span>

<span data-ttu-id="8fa1b-157">Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="8fa1b-158">MAPI verfügt über drei Unterstützungsobjektmethoden, mit deren Hilfe Dienstanbieter Benachrichtigungen implementieren können: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="8fa1b-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="8fa1b-159">Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **Subscribe** auf, wenn Ihre **Advise-Methode** aufgerufen wird, und geben Sie den  _lpAdviseSink-Zeiger_ frei.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="8fa1b-160">Wenn Sie die Benachrichtigung selbst unterstützen möchten, rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) der Durchwahlsenke auf, die durch den  _lpAdviseSink-Parameter_ dargestellt wird, um eine Kopie dieses Zeigers zu behalten.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="8fa1b-161">Bewahren Sie diese Kopie auf, bis Ihre [IMsgStore::Unadvise-Methode](imsgstore-unadvise.md) aufgerufen wird, um die Registrierung abbricht.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="8fa1b-162">Weisen Sie unabhängig davon, wie Sie die Benachrichtigung unterstützen, der Benachrichtigungsregistrierung eine Verbindungsnummer ungleich Null zu, und geben Sie sie im  _lpulConnection-Parameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="8fa1b-163">Geben Sie diese Verbindungsnummer erst frei, **wenn Unadvise** aufgerufen und abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8fa1b-164">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8fa1b-164">Notes to callers</span></span>

<span data-ttu-id="8fa1b-165">Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** jederzeit auch in jedem Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="8fa1b-166">Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) auf, um das an **Advise** übergebene Advise-Sink-Objekt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="8fa1b-167">Nachdem ein Aufruf von **Advise** erfolgreich war und **Unadvise** zum Abbrechen der Registrierung aufgerufen wurde, sollten Sie darauf vorbereitet sein, dass das Objekt "Advise Sink" freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="8fa1b-168">Sie sollten Ihr Advise Sink-Objekt nach **der Rückgabe von Advise** frei geben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="8fa1b-169">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="8fa1b-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="8fa1b-170">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="8fa1b-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8fa1b-171">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8fa1b-171">MFCMAPI reference</span></span>

<span data-ttu-id="8fa1b-172">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8fa1b-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8fa1b-173">**File**</span></span>|<span data-ttu-id="8fa1b-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8fa1b-174">**Function**</span></span>|<span data-ttu-id="8fa1b-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8fa1b-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8fa1b-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="8fa1b-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="8fa1b-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="8fa1b-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="8fa1b-178">MFCMAPI verwendet die **IMsgStore::Advise-Methode,** um sich für Benachrichtigungen im gesamten Nachrichtenspeicher zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fa1b-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fa1b-179">See also</span></span>



[<span data-ttu-id="8fa1b-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8fa1b-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="8fa1b-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8fa1b-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8fa1b-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8fa1b-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="8fa1b-183">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8fa1b-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="8fa1b-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8fa1b-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="8fa1b-185">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8fa1b-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

