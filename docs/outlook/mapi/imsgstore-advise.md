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
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792612"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="52249-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="52249-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="52249-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52249-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52249-105">Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Nachrichtenspeicher registriert.</span><span class="sxs-lookup"><span data-stu-id="52249-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="52249-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52249-106">Parameters</span></span>

 <span data-ttu-id="52249-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="52249-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="52249-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="52249-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="52249-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="52249-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="52249-110">[in] Ein Zeiger auf die Eintrags-ID des Ordners oder Meldung über welche Benachrichtigungen generiert werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="52249-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="52249-111">Wenn _LpEntryID_ auf NULL festgelegt ist, wird für Benachrichtigungen auf dem gesamten Nachrichtenspeicher **Advise** registriert.</span><span class="sxs-lookup"><span data-stu-id="52249-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="52249-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="52249-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="52249-113">[in] Eine Maske von Werten, mit die die Typen von Benachrichtigungsereignisse anzugeben, die dem Anrufer ist daran interessiert, und die Registrierung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="52249-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="52249-114">Es wird eine entsprechende [Benachrichtigung](notification.md) Struktur jede Art von Ereignis, das Informationen über das Ereignis enthält zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="52249-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="52249-115">Folgende sind gültige Werte für den Parameter _UlEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="52249-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="52249-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="52249-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="52249-117">Register für Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="52249-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="52249-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="52249-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="52249-119">Register für Benachrichtigungen über Ereignisse, die speziell für bestimmte Nachricht Speicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="52249-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="52249-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="52249-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="52249-121">Register für die Benachrichtigung über den Empfang von neuen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="52249-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="52249-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="52249-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="52249-123">Register für die Benachrichtigung über die Erstellung einer neuen Ordner oder einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="52249-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="52249-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="52249-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="52249-125">Register für Benachrichtigungen bezüglich eines Ordners oder die Nachricht kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="52249-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="52249-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="52249-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="52249-127">Register für Benachrichtigungen bezüglich eines Ordners oder die Nachricht wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="52249-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="52249-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="52249-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="52249-129">Register für Benachrichtigungen bezüglich eines Ordners oder einer Nachricht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="52249-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="52249-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="52249-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="52249-131">Register für Benachrichtigungen bezüglich eines Ordners oder die Nachricht verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="52249-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="52249-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="52249-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="52249-133">Register für die Benachrichtigung über den Abschluss der Suchvorgang.</span><span class="sxs-lookup"><span data-stu-id="52249-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="52249-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="52249-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="52249-135">[in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="52249-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="52249-136">Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="52249-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="52249-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="52249-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="52249-138">[out] Ein Zeiger auf eine Zahl ungleich NULL für die Verbindung zwischen des Anrufers advise-Empfängerobjekt und der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="52249-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="52249-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="52249-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="52249-140">[in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="52249-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="52249-141">Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="52249-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="52249-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="52249-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="52249-143">[out] Ein Zeiger auf eine ungleich NULL Verbindung Zahl, die die Verbindung zwischen des Anrufers stellt advise-Empfängerobjekt und des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="52249-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52249-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52249-144">Return value</span></span>

<span data-ttu-id="52249-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="52249-145">S_OK</span></span> 
  
> <span data-ttu-id="52249-146">Die Registrierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="52249-146">The registration was successful.</span></span>
    
<span data-ttu-id="52249-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="52249-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="52249-148">Die Nachrichtenanbieter unterstützt keine Registrierung für die Benachrichtigung über den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="52249-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52249-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52249-149">Remarks</span></span>

<span data-ttu-id="52249-150">Die **IMsgStore::Advise** -Methode richtet eine Verbindung zwischen dem Anrufer der advise-Empfängerobjekt und der Nachrichtenspeicher oder ein Objekt im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="52249-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="52249-151">Diese Verbindung wird verwendet, um das Senden von Benachrichtigungen an der Advise-Empfänger, wenn sich ein oder mehr Ereignisse, wie in den _UlEventMask_ -Parameter angegeben an das Quellobjekt Advise auftreten.</span><span class="sxs-lookup"><span data-stu-id="52249-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="52249-152">Wenn der _LpEntryID_ -Parameter verweist auf eine gültige Eingabe Bezeichner, hat die Advise-Quelle das Objekt durch dieses Eintrags-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="52249-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="52249-153">Wenn _LpEntryID_ NULL ist, ist die Advise-Quelle des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="52249-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="52249-154">Um eine Benachrichtigung zu senden, die Nachricht Speicheranbieter oder MAPI der registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="52249-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="52249-155">Einer der Parameter zu **OnNotify**, eine Benachrichtigungsstruktur enthält Informationen des jeweiligen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="52249-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="52249-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="52249-156">Notes to implementers</span></span>

<span data-ttu-id="52249-157">Sie können die Benachrichtigung mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="52249-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="52249-158">MAPI hat drei Methoden von Support-Objekt zur Verfügung stehen-Dienstanbieter Benachrichtigung implementieren: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)und [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="52249-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="52249-159">Wenn Sie sich entscheiden, die MAPI-Support-Methoden verwenden, rufen Sie **Abonnieren** die **Advise** -Methode aufgerufen wird, und heben Sie den Zeiger _LpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="52249-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="52249-160">Wenn Sie sich entscheiden, die Benachrichtigung zu unterstützen, rufen Sie die [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) -Methode der Advise-Empfänger, die durch den Parameter _LpAdviseSink_ dargestellt, um eine Kopie dieses Zeigers beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="52249-160">If you elect to support notification yourself, call the [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="52249-161">Verwalten Sie diese Kopie, bis die [IMsgStore::Unadvise](imsgstore-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="52249-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="52249-162">Unabhängig davon, wie Sie Benachrichtigung zu unterstützen weisen Sie eine Zahl ungleich NULL Verbindung die benachrichtigungsregistrierung, und im Parameter _LpulConnection_ zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="52249-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="52249-163">Freigegeben Sie diese Verbindungsnummer nicht, bis **Unadvise** aufgerufen wurde und dass die Benutzerreplikation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="52249-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="52249-164">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="52249-164">Notes to callers</span></span>

<span data-ttu-id="52249-165">Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auch jederzeit auf einem beliebigen Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="52249-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="52249-166">Wenn Sie müssen, die Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten sicher sein, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion, um das Empfängerobjekt Advise generieren, das an **Advise**übergeben.</span><span class="sxs-lookup"><span data-stu-id="52249-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="52249-167">Nach einem Aufruf von **Advise** erfolgreich war, und bereiten Sie vor dem **Unadvise** aufgerufen wurde, um die Registrierung abzubrechen, für das Empfängerobjekt Advise freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="52249-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="52249-168">Sie sollten Ihre Advise-Empfängerobjekt freigeben, nachdem **Advise** zurückgegeben, es sei denn, Sie eine bestimmte langfristige Verwendung dafür haben.</span><span class="sxs-lookup"><span data-stu-id="52249-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="52249-169">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="52249-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="52249-170">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Behandeln von Benachrichtigungen](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="52249-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="52249-171">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="52249-171">MFCMAPI reference</span></span>

<span data-ttu-id="52249-172">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="52249-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="52249-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="52249-173">**File**</span></span>|<span data-ttu-id="52249-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="52249-174">**Function**</span></span>|<span data-ttu-id="52249-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="52249-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="52249-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="52249-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="52249-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="52249-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="52249-178">MFCMAPI (engl.) verwendet die **IMsgStore::Advise** -Methode, um für Benachrichtigungen auf dem gesamten Nachrichtenspeicher registrieren.</span><span class="sxs-lookup"><span data-stu-id="52249-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52249-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52249-179">See also</span></span>



[<span data-ttu-id="52249-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="52249-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="52249-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="52249-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="52249-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="52249-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="52249-183">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="52249-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="52249-184">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="52249-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="52249-185">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="52249-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

