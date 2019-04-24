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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317325"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="65d9f-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="65d9f-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="65d9f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65d9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65d9f-105">Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf den Nachrichtenspeicher auswirken.</span><span class="sxs-lookup"><span data-stu-id="65d9f-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="65d9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65d9f-106">Parameters</span></span>

 <span data-ttu-id="65d9f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="65d9f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="65d9f-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="65d9f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="65d9f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="65d9f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="65d9f-110">in Ein Zeiger auf die Eintrags-ID des Ordners oder der Nachricht, über die Benachrichtigungen generiert werden sollen, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="65d9f-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="65d9f-111">Wenn _lpEntryID_ auf NULL festgelegt ist, **Raten** Sie Register für Benachrichtigungen im gesamten Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="65d9f-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="65d9f-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="65d9f-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="65d9f-113">in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist, und die in die Registrierung aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65d9f-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="65d9f-114">Jeder Art von Ereignis [](notification.md) , das Informationen über das Ereignis enthält, ist eine entsprechende Benachrichtigungsstruktur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="65d9f-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="65d9f-115">Im folgenden finden Sie gültige Werte für den Parameter _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="65d9f-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="65d9f-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="65d9f-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="65d9f-117">Registriert Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="65d9f-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="65d9f-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="65d9f-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="65d9f-119">Registriert Benachrichtigungen zu Ereignissen, die spezifisch für den jeweiligen Nachrichtenspeicher Anbieter sind.</span><span class="sxs-lookup"><span data-stu-id="65d9f-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="65d9f-120">_Uleventmaskfnevnewmail_</span><span class="sxs-lookup"><span data-stu-id="65d9f-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="65d9f-121">Registriert Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="65d9f-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="65d9f-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="65d9f-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="65d9f-123">Registriert Benachrichtigungen über das Erstellen eines neuen Ordners oder einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="65d9f-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="65d9f-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="65d9f-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="65d9f-125">Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="65d9f-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="65d9f-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="65d9f-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="65d9f-127">Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="65d9f-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="65d9f-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="65d9f-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="65d9f-129">Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="65d9f-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="65d9f-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="65d9f-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="65d9f-131">Registriert Benachrichtigungen zu einem Ordner oder einer Nachricht, die verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="65d9f-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="65d9f-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="65d9f-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="65d9f-133">Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="65d9f-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="65d9f-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="65d9f-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="65d9f-135">in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="65d9f-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="65d9f-136">Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.</span><span class="sxs-lookup"><span data-stu-id="65d9f-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="65d9f-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="65d9f-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="65d9f-138">Out Ein Zeiger auf eine Zahl ungleich NULL, die die Verbindung zwischen dem Advise-Objekt des Empfängers und der Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="65d9f-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="65d9f-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="65d9f-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="65d9f-140">in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="65d9f-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="65d9f-141">Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.</span><span class="sxs-lookup"><span data-stu-id="65d9f-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="65d9f-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="65d9f-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="65d9f-143">Out Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Verbindung zwischen dem Advise-Objekt des Empfängers und dem Nachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="65d9f-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65d9f-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65d9f-144">Return value</span></span>

<span data-ttu-id="65d9f-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="65d9f-145">S_OK</span></span> 
  
> <span data-ttu-id="65d9f-146">Die Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="65d9f-146">The registration was successful.</span></span>
    
<span data-ttu-id="65d9f-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="65d9f-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="65d9f-148">Der Nachrichtenspeicher Anbieter unterstützt keine Registrierung für Benachrichtigungen über den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="65d9f-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65d9f-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65d9f-149">Remarks</span></span>

<span data-ttu-id="65d9f-150">Die **IMsgStore:: Advise** -Methode stellt eine Verbindung zwischen dem Advise-Objekt des Anrufers und dem Nachrichtenspeicher oder einem Objekt im Nachrichtenspeicher her.</span><span class="sxs-lookup"><span data-stu-id="65d9f-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="65d9f-151">Diese Verbindung wird verwendet, um Benachrichtigungen an die Advise-Senke zu senden, wenn mindestens ein Ereignis, wie im _ulEventMask_ -Parameter angegeben, für das Advise-Quellobjekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="65d9f-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="65d9f-152">Wenn der _lpEntryID_ -Parameter auf eine gültige Eintrags-ID zeigt, ist die Advise-Quelle das Objekt, das durch diese Eintrags-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="65d9f-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="65d9f-153">Wenn _lpEntryID_ ist, ist die Advise-Quelle der Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="65d9f-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="65d9f-154">Zum Senden einer Benachrichtigung ruft der Nachrichtenspeicher Anbieter oder die MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der registrierten Advise-Senke auf.</span><span class="sxs-lookup"><span data-stu-id="65d9f-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="65d9f-155">Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="65d9f-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="65d9f-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="65d9f-156">Notes to implementers</span></span>

<span data-ttu-id="65d9f-157">Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="65d9f-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="65d9f-158">MAPI verfügt über drei Support Objektmethoden, mit denen Dienstanbieter die Benachrichtigung implementieren können: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport:: notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="65d9f-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="65d9f-159">Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **subscribe** auf, wenn Ihre **Advise** -Methode aufgerufen wird, und geben Sie den _lpAdviseSink_ -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="65d9f-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="65d9f-160">Wenn Sie sich für die Unterstützung der Benachrichtigung entscheiden, rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode der Advise-Senke auf, die durch den _lpAdviseSink_ -Parameter dargestellt wird, um eine Kopie dieses Zeigers aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="65d9f-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="65d9f-161">Bewahren Sie diese Kopie auf, bis die [IMsgStore:: Unadvise](imsgstore-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="65d9f-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="65d9f-162">Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungs Registrierung eine unGleich NULL-Verbindung zu und geben Sie im _lpulConnection_ -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="65d9f-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="65d9f-163">Geben Sie diese Verbindungsnummer nicht frei \*\*\*\* , bis Unadvise aufgerufen und abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="65d9f-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="65d9f-164">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="65d9f-164">Notes to callers</span></span>

<span data-ttu-id="65d9f-165">Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann \*\*\*\* der Aufruf von OnNotify auch jederzeit in jedem Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="65d9f-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="65d9f-166">Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt für einen bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion auf, um das Advise-Objekt, das Sie an **Advise**weitergeben, zu generieren.</span><span class="sxs-lookup"><span data-stu-id="65d9f-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="65d9f-167">Nachdem ein Anruf bei **Advise** erfolgreich war und bevor **Unadvise** aufgerufen wurde, um die Registrierung abzubrechen, müssen Sie darauf vorbereitet sein, dass das Advise-Senke-Objekt freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d9f-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="65d9f-168">Sie sollten Ihr Advise-Senke-Objekt freigeben, nachdem **Advise** zurückgegeben wird, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="65d9f-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="65d9f-169">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="65d9f-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="65d9f-170">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="65d9f-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="65d9f-171">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="65d9f-171">MFCMAPI reference</span></span>

<span data-ttu-id="65d9f-172">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="65d9f-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="65d9f-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="65d9f-173">**File**</span></span>|<span data-ttu-id="65d9f-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="65d9f-174">**Function**</span></span>|<span data-ttu-id="65d9f-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="65d9f-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65d9f-176">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="65d9f-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="65d9f-177">CBaseDialog:: OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="65d9f-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="65d9f-178">MFCMAPI verwendet die **IMsgStore:: Advise** -Methode, um Benachrichtigungen für den gesamten Nachrichtenspeicher zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="65d9f-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65d9f-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65d9f-179">See also</span></span>



[<span data-ttu-id="65d9f-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="65d9f-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="65d9f-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="65d9f-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="65d9f-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="65d9f-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="65d9f-183">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="65d9f-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="65d9f-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="65d9f-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="65d9f-185">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="65d9f-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

