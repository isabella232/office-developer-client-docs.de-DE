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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317311"
---
# <a name="imslogonadvise"></a><span data-ttu-id="6a13e-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="6a13e-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="6a13e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a13e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a13e-105">Registriert ein Objekt bei einem Nachrichtenspeicher Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="6a13e-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="6a13e-106">Der Nachrichtenspeicher sendet dann Benachrichtigungen zu Änderungen am registrierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="6a13e-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6a13e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a13e-107">Parameters</span></span>

 <span data-ttu-id="6a13e-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6a13e-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="6a13e-109">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6a13e-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6a13e-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6a13e-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="6a13e-111">in Ein Zeiger auf die Eintrags-ID des Objekts, über das Benachrichtigungen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6a13e-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="6a13e-112">Bei diesem Objekt kann es sich um einen Ordner, eine Nachricht oder ein beliebiges anderes Objekt im Nachrichtenspeicher handeln.</span><span class="sxs-lookup"><span data-stu-id="6a13e-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="6a13e-113">Wenn MAPI den Parameter _cbEntryID_ auf 0 festlegt und für _lpEntryID_den Wert **null** übergibt, stellt die Advise-Senke Benachrichtigungen zu Änderungen am gesamten Nachrichtenspeicher bereit.</span><span class="sxs-lookup"><span data-stu-id="6a13e-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="6a13e-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="6a13e-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="6a13e-115">in Eine Ereignismaske der Typen von Benachrichtigungsereignissen, die für das Objekt auftreten, über das MAPI Benachrichtigungen generiert.</span><span class="sxs-lookup"><span data-stu-id="6a13e-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="6a13e-116">Die Maske filtert bestimmte Fälle.</span><span class="sxs-lookup"><span data-stu-id="6a13e-116">The mask filters specific cases.</span></span> <span data-ttu-id="6a13e-117">Jedem Ereignistyp ist eine Struktur zugeordnet, die zusätzliche Informationen über das Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="6a13e-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="6a13e-118">In der folgenden Tabelle sind die möglichen Ereignistypen zusammen mit den entsprechenden Strukturen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a13e-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="6a13e-119">**Benachrichtigungs Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="6a13e-119">**Notification event type**</span></span>|<span data-ttu-id="6a13e-120">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="6a13e-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a13e-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="6a13e-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="6a13e-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="6a13e-123">Uleventmaskfnevnewmail</span><span class="sxs-lookup"><span data-stu-id="6a13e-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="6a13e-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="6a13e-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="6a13e-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="6a13e-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a13e-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="6a13e-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="6a13e-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a13e-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="6a13e-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="6a13e-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a13e-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="6a13e-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="6a13e-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a13e-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="6a13e-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="6a13e-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a13e-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="6a13e-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="6a13e-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a13e-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="6a13e-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="6a13e-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a13e-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="6a13e-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="6a13e-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="6a13e-140">in Ein Zeiger auf ein Advise-Senke-Objekt, das aufgerufen werden soll, wenn ein Ereignis für das Session-Objekt auftritt, über das die Benachrichtigung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="6a13e-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="6a13e-141">Dieses Advise-Senke-Objekt muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6a13e-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="6a13e-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="6a13e-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="6a13e-143">Out Ein Zeiger auf eine Variable, die bei erfolgreicher Rückgabe die Verbindungsnummer für die Benachrichtigungs Registrierung enthält.</span><span class="sxs-lookup"><span data-stu-id="6a13e-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="6a13e-144">Die Verbindungsnummer muss ungleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6a13e-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a13e-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a13e-145">Return value</span></span>

<span data-ttu-id="6a13e-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a13e-146">S_OK</span></span> 
  
> <span data-ttu-id="6a13e-147">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6a13e-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6a13e-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6a13e-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6a13e-149">Der Vorgang wird nicht von MAPI oder von einem oder mehreren Dienstanbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a13e-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a13e-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a13e-150">Remarks</span></span>

<span data-ttu-id="6a13e-151">Nachrichtenspeicher Anbieter implementieren die **IMSLogon:: Advise** -Methode, um ein Objekt für Benachrichtigungsrückrufe zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="6a13e-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="6a13e-152">Wenn eine Änderung für das angegebene Objekt auftritt, überprüft der Anbieter, um zu sehen, welches Ereignis Masken Bit im _ulEventMask_ -Parameter festgelegt wurde, und daher, welche Art von Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6a13e-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="6a13e-153">Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das vom _lpAdviseSink_ -Parameter angegebene Advise-Senke-Objekt auf, um das Ereignis zu melden.</span><span class="sxs-lookup"><span data-stu-id="6a13e-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="6a13e-154">Die Daten, die in der Benachrichtigungs \*\*\*\* Struktur an die OnNotify-Routine übergeben werden, beschreiben das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a13e-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="6a13e-155">Der Aufruf von **OnNotify** kann während des Anrufs auftreten, der das Objekt oder zu einem späteren Zeitpunkt ändert.</span><span class="sxs-lookup"><span data-stu-id="6a13e-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="6a13e-156">Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann \*\*\*\* der Aufruf von OnNotify in jedem Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="6a13e-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="6a13e-157">Um einen Anruf von onNotify \*\*\*\* sicher zu behandeln, der zu einem ungünstigen Zeitpunkt geschehen kann, sollte eine Clientanwendung die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6a13e-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="6a13e-158">Um Benachrichtigungen bereitzustellen, muss der Nachrichtenspeicher Anbieter, der **Advise** implementiert, eine Kopie des Zeigers auf das _lpAdviseSink_ -Advise-Senke-Objekt aufbewahren; Hierzu ruft der Anbieter die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode für die Advise-Senke auf, um den Objektzeiger zu warten, bis die Benachrichtigungs Registrierung mit einem Aufruf der [IMSLogon:: Unadvise](imslogon-unadvise.md) -Methode abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="6a13e-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="6a13e-159">Die **Advise** -Implementierung sollte der Benachrichtigungs Registrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor Sie im _lpulConnection_ -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a13e-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="6a13e-160">Dienstanbieter können das Advise-Senke-Objekt freigeben, bevor die Registrierung abgebrochen wird, aber Sie dürfen \*\*\*\* die Verbindungsnummer erst freigeben, wenn Unadvise aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6a13e-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="6a13e-161">Nachdem ein Aufruf von **Advise** erfolgreich war und bevor **Unadvise** aufgerufen wurde, müssen Anbieter für das Advise-Senke-Objekt freigegeben werden vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="6a13e-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="6a13e-162">Daher sollte ein Anbieter seine Advise-Senke-Objekt nach der Rückgabe von **Advise** freigeben, es sei denn, es hat eine bestimmte langfristige Verwendung für Sie.</span><span class="sxs-lookup"><span data-stu-id="6a13e-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="6a13e-163">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6a13e-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a13e-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a13e-164">See also</span></span>



[<span data-ttu-id="6a13e-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6a13e-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="6a13e-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6a13e-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6a13e-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6a13e-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="6a13e-168">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6a13e-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6a13e-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a13e-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

