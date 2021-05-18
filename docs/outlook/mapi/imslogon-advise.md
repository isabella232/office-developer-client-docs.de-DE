---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317311"
---
# <a name="imslogonadvise"></a><span data-ttu-id="40131-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="40131-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="40131-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40131-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40131-105">Registriert ein Objekt bei einem Nachrichtenspeicheranbieter für Benachrichtigungen über Änderungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="40131-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="40131-106">Der Nachrichtenspeicher sendet dann Benachrichtigungen über Änderungen am registrierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="40131-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="40131-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="40131-107">Parameters</span></span>

 <span data-ttu-id="40131-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="40131-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="40131-109">[in] Die Größe des Eintragsbezeichners in Bytes, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="40131-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="40131-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="40131-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="40131-111">[in] Ein Zeiger auf den Eintragsbezeichner des Objekts, über das Benachrichtigungen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40131-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="40131-112">Dieses Objekt kann ein Ordner, eine Nachricht oder ein beliebiges anderes Objekt im Nachrichtenspeicher sein.</span><span class="sxs-lookup"><span data-stu-id="40131-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="40131-113">Wenn MAPI den  _cbEntryID-Parameter_ auf 0 legt und **null** für  _lpEntryID_ übergibt, stellt die Hinweisesenke Benachrichtigungen zu Änderungen am gesamten Nachrichtenspeicher zur Hand.</span><span class="sxs-lookup"><span data-stu-id="40131-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="40131-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="40131-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="40131-115">[in] Eine Ereignismaske der Arten von Benachrichtigungsereignissen, die für das Objekt auftreten, über das MAPI Benachrichtigungen generiert.</span><span class="sxs-lookup"><span data-stu-id="40131-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="40131-116">Die Maske filtert bestimmte Fälle.</span><span class="sxs-lookup"><span data-stu-id="40131-116">The mask filters specific cases.</span></span> <span data-ttu-id="40131-117">Jedem Ereignistyp ist eine Struktur zugeordnet, die zusätzliche Informationen zum Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="40131-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="40131-118">In der folgenden Tabelle sind die möglichen Ereignistypen zusammen mit den entsprechenden Strukturen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="40131-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="40131-119">**Benachrichtigungsereignistyp**</span><span class="sxs-lookup"><span data-stu-id="40131-119">**Notification event type**</span></span>|<span data-ttu-id="40131-120">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="40131-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40131-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="40131-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="40131-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="40131-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="40131-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="40131-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="40131-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="40131-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="40131-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40131-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="40131-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="40131-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40131-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="40131-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="40131-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40131-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="40131-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="40131-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40131-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="40131-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="40131-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40131-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="40131-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="40131-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40131-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="40131-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="40131-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40131-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="40131-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="40131-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="40131-140">[in] Ein Zeiger auf ein Advise Sink-Objekt, das aufgerufen werden soll, wenn ein Ereignis für das Sitzungsobjekt auftritt, über das eine Benachrichtigung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="40131-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="40131-141">Dieses ratende Sink-Objekt muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="40131-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="40131-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="40131-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="40131-143">[out] Ein Zeiger auf eine Variable, die bei erfolgreicher Rückgabe die Verbindungsnummer für die Benachrichtigungsregistrierung enthält.</span><span class="sxs-lookup"><span data-stu-id="40131-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="40131-144">Die Verbindungsnummer muss ungleich Null sein.</span><span class="sxs-lookup"><span data-stu-id="40131-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40131-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40131-145">Return value</span></span>

<span data-ttu-id="40131-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="40131-146">S_OK</span></span> 
  
> <span data-ttu-id="40131-147">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="40131-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="40131-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="40131-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="40131-149">Der Vorgang wird weder von MAPI noch von einem oder mehreren Dienstanbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40131-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40131-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40131-150">Remarks</span></span>

<span data-ttu-id="40131-151">Nachrichtenspeicheranbieter implementieren die **IMSLogon::Advise-Methode,** um ein Objekt für Benachrichtigungsrückrufe zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="40131-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="40131-152">Wenn eine Änderung am angegebenen Objekt auftritt, überprüft der Anbieter, welches Ereignismaskenbit im  _ulEventMask-Parameter_ festgelegt wurde und welche Art von Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="40131-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="40131-153">Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) auf, damit das vom  _lpAdviseSink-Parameter_ angegebene Advise Sink-Objekt das Ereignis melden kann.</span><span class="sxs-lookup"><span data-stu-id="40131-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="40131-154">Daten, die in der Benachrichtigungsstruktur an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="40131-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="40131-155">Der Aufruf von **OnNotify** kann während des Aufrufs erfolgen, der das Objekt ändert, oder zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="40131-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="40131-156">Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="40131-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="40131-157">Zum sicheren Behandeln eines Aufrufs von **OnNotify,** der zu einem unvorstellbarem Zeitpunkt ausgeführt werden kann, sollte eine Clientanwendung die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="40131-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="40131-158">Um Benachrichtigungen bereitstellen zu können, muss der Nachrichtenspeicheranbieter, der **Advise** implementiert, eine Kopie des Zeigers auf das  _lpAdviseSink-Ratgeber-Sink-Objekt_ behalten. Dazu ruft der Anbieter die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) auf, um den Objektzeiger zu verwalten, bis die Benachrichtigungsregistrierung mit einem Aufruf der [IMSLogon::Unadvise-Methode](imslogon-unadvise.md) abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="40131-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="40131-159">Die **Advise-Implementierung** sollte der Benachrichtigungsregistrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor sie im  _lpulConnection-Parameter zurückgesenkt_ wird.</span><span class="sxs-lookup"><span data-stu-id="40131-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="40131-160">Dienstanbieter können das Advise -Sink-Objekt vor dem Abbrechen der Registrierung los, aber sie dürfen die Verbindungsnummer erst los, wenn **Unadvise** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="40131-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="40131-161">Nachdem ein Aufruf von **Advise** erfolgreich war und **unadvise** aufgerufen wurde, müssen Anbieter darauf vorbereitet sein, dass das Advise Sink-Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40131-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="40131-162">Daher sollte ein Anbieter sein Advise -Sink-Objekt nach **der Rückgabe** von Advise veröffentlichen, es sei denn, er hat eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="40131-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="40131-163">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="40131-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40131-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40131-164">See also</span></span>



[<span data-ttu-id="40131-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="40131-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="40131-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="40131-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="40131-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="40131-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="40131-168">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="40131-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="40131-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40131-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

