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
# <a name="imsgstoreadvise"></a><span data-ttu-id="f8d97-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="f8d97-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="f8d97-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8d97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8d97-105">Registriert, um Benachrichtigungen über angegebene Ereignisse zu empfangen, die sich auf den Nachrichtenspeicher auswirken.</span><span class="sxs-lookup"><span data-stu-id="f8d97-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f8d97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8d97-106">Parameters</span></span>

 <span data-ttu-id="f8d97-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8d97-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f8d97-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f8d97-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f8d97-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8d97-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f8d97-110">in Ein Zeiger auf die Eintrags-ID des Ordners oder der Nachricht, über die Benachrichtigungen generiert werden sollen, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="f8d97-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="f8d97-111">Wenn _lpEntryID_ auf NULL festgelegt ist, **Benachrichtigen** Sie Register für Benachrichtigungen im gesamten Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="f8d97-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="f8d97-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f8d97-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="f8d97-113">in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist und in die Registrierung einbezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f8d97-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="f8d97-114">Jeder Art von Ereignis [](notification.md) , das Informationen über das Ereignis enthält, ist eine entsprechende Benachrichtigungsstruktur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f8d97-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="f8d97-115">Im folgenden sind gültige Werte für den _ulEventMask_ -Parameter angegeben:</span><span class="sxs-lookup"><span data-stu-id="f8d97-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="f8d97-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="f8d97-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="f8d97-117">Registriert für Benachrichtigungen zu schweren Fehlern, beispielsweise unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f8d97-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="f8d97-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="f8d97-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="f8d97-119">Registriert Benachrichtigungen zu Ereignissen, die für den jeweiligen Nachrichtenspeicher Anbieter spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f8d97-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="f8d97-120">_uleventmaskfnevnewmail_</span><span class="sxs-lookup"><span data-stu-id="f8d97-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="f8d97-121">Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f8d97-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="f8d97-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="f8d97-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="f8d97-123">Registriert für Benachrichtigungen über die Erstellung eines neuen Ordners oder einer neuen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f8d97-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="f8d97-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="f8d97-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="f8d97-125">Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="f8d97-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="f8d97-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="f8d97-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="f8d97-127">Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f8d97-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="f8d97-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="f8d97-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="f8d97-129">Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f8d97-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="f8d97-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="f8d97-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="f8d97-131">Registriert für Benachrichtigungen zu einem Ordner oder einer Nachricht, die verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="f8d97-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="f8d97-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="f8d97-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="f8d97-133">Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="f8d97-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="f8d97-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f8d97-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f8d97-135">in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f8d97-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f8d97-136">Dieses Advise-Senke-Objekt muss bereits reserviert worden sein.</span><span class="sxs-lookup"><span data-stu-id="f8d97-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="f8d97-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f8d97-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="f8d97-138">Timeout Ein Zeiger auf eine Zahl ungleich NULL, die die Verbindung zwischen dem Advise-Senk Objekt des Anrufers und der Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8d97-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="f8d97-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f8d97-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f8d97-140">in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f8d97-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f8d97-141">Dieses Advise-Senke-Objekt muss bereits reserviert worden sein.</span><span class="sxs-lookup"><span data-stu-id="f8d97-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="f8d97-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f8d97-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="f8d97-143">Timeout Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Verbindung zwischen dem Advise-Senk Objekt des Anrufers und dem Nachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8d97-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8d97-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8d97-144">Return value</span></span>

<span data-ttu-id="f8d97-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8d97-145">S_OK</span></span> 
  
> <span data-ttu-id="f8d97-146">Die Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f8d97-146">The registration was successful.</span></span>
    
<span data-ttu-id="f8d97-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f8d97-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f8d97-148">Der Nachrichtenspeicher Anbieter unterstützt keine Registrierung für die Benachrichtigung über den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="f8d97-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8d97-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8d97-149">Remarks</span></span>

<span data-ttu-id="f8d97-150">Die **IMsgStore:: Advise** -Methode richtet eine Verbindung zwischen dem Advise-Senk Objekt des Anrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher ein.</span><span class="sxs-lookup"><span data-stu-id="f8d97-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="f8d97-151">Diese Verbindung wird zum Senden von Benachrichtigungen an die Advise-Senke verwendet, wenn ein oder mehrere Ereignisse, wie im Parameter _ulEventMask_ angegeben, im Advise-Quellobjekt auftreten.</span><span class="sxs-lookup"><span data-stu-id="f8d97-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="f8d97-152">Wenn der Parameter _lpEntryID_ auf eine gültige Eintrags-ID verweist, ist die Advise-Quelle das Objekt, das durch diesen Eintragsbezeichner identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f8d97-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="f8d97-153">Wenn _lpEntryID_ NULL ist, ist die Advise-Quelle der Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="f8d97-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="f8d97-154">Zum Senden einer Benachrichtigung ruft entweder der Nachrichtenspeicher Anbieter oder die MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der registrierten Advise-Senke auf.</span><span class="sxs-lookup"><span data-stu-id="f8d97-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="f8d97-155">Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das jeweilige Ereignis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f8d97-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f8d97-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f8d97-156">Notes to implementers</span></span>

<span data-ttu-id="f8d97-157">Sie können die Benachrichtigung mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f8d97-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="f8d97-158">MAPI verfügt über drei Unterstützungsobjekt Methoden, um Dienstanbietern bei der Implementierung der Benachrichtigung zu helfen: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport:: notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="f8d97-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="f8d97-159">Wenn Sie sich für die Verwendung der MAPI-Unterstützungsmethoden entscheiden, rufen Sie **subscribe** an, wenn Ihre **Advise** -Methode aufgerufen wird, und geben Sie den _lpAdviseSink_ -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="f8d97-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="f8d97-160">Wenn Sie die Benachrichtigung selbst unterstützen möchten, rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode der Advise-Senke, die durch den _lpAdviseSink_ -Parameter dargestellt wird, auf, um eine Kopie dieses Zeigers beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="f8d97-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="f8d97-161">Bewahren Sie diese Kopie auf, bis Ihre [IMsgStore:: Unadvise](imsgstore-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="f8d97-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="f8d97-162">Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungs Registrierung eine ungleich NULL-Verbindungsnummer zu und geben Sie im Parameter _lpulConnection_ zurück.</span><span class="sxs-lookup"><span data-stu-id="f8d97-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f8d97-163">Geben Sie diese Verbindungsnummer nicht frei \*\*\*\* , bis Unadvise aufgerufen wurde und abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f8d97-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f8d97-164">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f8d97-164">Notes to callers</span></span>

<span data-ttu-id="f8d97-165">Auf Systemen, die mehrere Ausführungs Threads unterstützen, kann der \*\*\*\* Aufruf von OnNotify auch jederzeit auf jedem Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f8d97-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="f8d97-166">Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt für einen bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion auf, um das Advise-Senke-Objekt zu generieren, das Sie an **Advise**übergeben.</span><span class="sxs-lookup"><span data-stu-id="f8d97-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="f8d97-167">Nachdem ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor **Unadvise** aufgerufen wurde, um die Registrierung abzubrechen, müssen Sie darauf vorbereitet sein, das Advise-Senke-Objekt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f8d97-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="f8d97-168">Sie sollten Ihr Advise-Senke-Objekt nach der Rückgabe von **Advise** freigeben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="f8d97-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f8d97-169">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f8d97-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="f8d97-170">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f8d97-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8d97-171">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="f8d97-171">MFCMAPI reference</span></span>

<span data-ttu-id="f8d97-172">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f8d97-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8d97-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f8d97-173">**File**</span></span>|<span data-ttu-id="f8d97-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f8d97-174">**Function**</span></span>|<span data-ttu-id="f8d97-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f8d97-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8d97-176">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="f8d97-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="f8d97-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="f8d97-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="f8d97-178">MfcMapi verwendet die **IMsgStore:: Advise** -Methode, um für Benachrichtigungen im gesamten Nachrichtenspeicher zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f8d97-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8d97-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8d97-179">See also</span></span>



[<span data-ttu-id="f8d97-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f8d97-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f8d97-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f8d97-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f8d97-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f8d97-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="f8d97-183">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="f8d97-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f8d97-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f8d97-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="f8d97-185">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f8d97-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

