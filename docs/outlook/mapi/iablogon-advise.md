---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428228"
---
# <a name="iablogonadvise"></a><span data-ttu-id="46ff1-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="46ff1-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="46ff1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46ff1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46ff1-105">Registriert den Anrufer, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.</span><span class="sxs-lookup"><span data-stu-id="46ff1-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="46ff1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ff1-106">Parameters</span></span>

 <span data-ttu-id="46ff1-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="46ff1-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="46ff1-108">[in] Die Anzahl der Bytes in der Eintrags-ID, auf die der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="46ff1-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="46ff1-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="46ff1-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="46ff1-110">[in] Ein Zeiger auf den Eintragsbezeichner des Objekts, über das Benachrichtigungen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="46ff1-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="46ff1-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="46ff1-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="46ff1-112">[in] Eine Bitmaske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, die der Anrufer interessiert und in die Registrierung einbezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="46ff1-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="46ff1-113">Jedem Ereignistyp ist eine entsprechende [NOTIFICATION-Struktur](notification.md) zugeordnet, die Informationen zum Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="46ff1-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="46ff1-114">In der folgenden Tabelle sind die gültigen Werte für den  _ulEventMask-Parameter_ und die strukturen aufgeführt, die jedem Wert zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="46ff1-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="46ff1-115">**Benachrichtigungsereignistyp**</span><span class="sxs-lookup"><span data-stu-id="46ff1-115">**Notification event type**</span></span>|<span data-ttu-id="46ff1-116">\*\*Entsprechende \*\*BENACHRICHTIGUNGsstruktur\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="46ff1-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46ff1-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="46ff1-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="46ff1-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="46ff1-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="46ff1-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="46ff1-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="46ff1-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="46ff1-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="46ff1-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="46ff1-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="46ff1-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="46ff1-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="46ff1-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="46ff1-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="46ff1-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="46ff1-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="46ff1-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="46ff1-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="46ff1-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="46ff1-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="46ff1-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="46ff1-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="46ff1-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="46ff1-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="46ff1-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="46ff1-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="46ff1-130">[in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46ff1-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="46ff1-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="46ff1-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="46ff1-132">[out] Ein Zeiger auf einen Wert ungleich Null, der die Benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="46ff1-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46ff1-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46ff1-133">Return value</span></span>

<span data-ttu-id="46ff1-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="46ff1-134">S_OK</span></span> 
  
> <span data-ttu-id="46ff1-135">Die Benachrichtigungsregistrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="46ff1-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="46ff1-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="46ff1-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="46ff1-137">Der im  _lpEntryID-Parameter_ übergebene Eintragsbezeichner hat nicht das entsprechende Format.</span><span class="sxs-lookup"><span data-stu-id="46ff1-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="46ff1-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="46ff1-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="46ff1-139">Der Adressbuchanbieter unterstützt keine Benachrichtigung, möglicherweise, weil er keine Änderungen an seinen Objekten zu lässt.</span><span class="sxs-lookup"><span data-stu-id="46ff1-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="46ff1-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="46ff1-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="46ff1-141">Der Adressbuchanbieter kann die in  _lpEntryID_ übergebene Eintrags-ID nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="46ff1-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46ff1-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46ff1-142">Remarks</span></span>

<span data-ttu-id="46ff1-143">Adressbuchanbieter implementieren die **IABLogon::Advise-Methode,** um den Anrufer zu registrieren, der benachrichtigt wird, wenn eine Änderung an einem Objekt in einem ihrer Container auftritt.</span><span class="sxs-lookup"><span data-stu-id="46ff1-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="46ff1-144">Anrufer können sich für Benachrichtigungen zu Messagingbenutzern, Verteilerlisten oder ganzen Containern registrieren.</span><span class="sxs-lookup"><span data-stu-id="46ff1-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="46ff1-145">Clients rufen in der Regel die [IAddrBook::Advise-Methode auf, um](iaddrbook-advise.md) sich für Adressbuchbenachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="46ff1-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="46ff1-146">MAPI ruft dann die **Advise-Methode** des Adressbuchanbieters auf, der für das Objekt verantwortlich ist, das durch den Eintragsbezeichner in _lpEntryID dargestellt wird._</span><span class="sxs-lookup"><span data-stu-id="46ff1-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="46ff1-147">Wenn eine Änderung am angegebenen Objekt des typs auftritt, der in  _ulEventMask_ dargestellt wird, wird ein Aufruf der **OnNotify-Methode** der Ratensenke vorgenommen, auf die  _von lpAdviseSink_ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="46ff1-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="46ff1-148">Daten, die in der **NOTIFICATION-Struktur** an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="46ff1-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="46ff1-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="46ff1-149">Notes to implementers</span></span>

<span data-ttu-id="46ff1-150">Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="46ff1-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="46ff1-151">MAPI verfügt über drei Unterstützungsobjektmethoden, mit deren Hilfe Dienstanbieter Benachrichtigungen implementieren können:</span><span class="sxs-lookup"><span data-stu-id="46ff1-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="46ff1-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="46ff1-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="46ff1-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="46ff1-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="46ff1-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="46ff1-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="46ff1-155">Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **Subscribe** auf, wenn Ihre **Advise-Methode** aufgerufen wird, und geben Sie den  _lpAdviseSink-Zeiger_ frei.</span><span class="sxs-lookup"><span data-stu-id="46ff1-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="46ff1-156">Wenn Sie die Benachrichtigung selbst unterstützen möchten, rufen Sie die **AddRef-Methode** der Durchwahlsenke auf, die durch den  _lpAdviseSink-Parameter_ dargestellt wird, um eine Kopie dieses Zeigers zu behalten.</span><span class="sxs-lookup"><span data-stu-id="46ff1-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="46ff1-157">Bewahren Sie diese Kopie auf, bis Ihre [IABLogon::Unadvise-Methode](iablogon-unadvise.md) aufgerufen wird, um die Registrierung abbricht.</span><span class="sxs-lookup"><span data-stu-id="46ff1-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="46ff1-158">Weisen Sie unabhängig davon, wie Sie die Benachrichtigung unterstützen, der Benachrichtigungsregistrierung eine Verbindungsnummer ungleich Null zu, und geben Sie sie im  _lpulConnection-Parameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="46ff1-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="46ff1-159">Geben Sie diese Verbindungsnummer erst frei, wenn die **Unadvise-Methode** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="46ff1-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="46ff1-160">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="46ff1-160">Notes to callers</span></span>

<span data-ttu-id="46ff1-161">Der Hinweissenkenzeiger, den Sie im  _lpAdviseSink-Parameter_ **an Advise** übergeben, kann auf ein Objekt verweisen, das Sie erstellt haben oder das MAPI über die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="46ff1-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="46ff1-162">Möglicherweise sollten Sie **HrThisThreadAdviseSink** verwenden, wenn Sie mehrere Ausführungsthreads unterstützen und sicherstellen möchten, dass nachfolgende Aufrufe ihrer **OnNotify-Methode** zu einem geeigneten Zeitpunkt in einem geeigneten Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="46ff1-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="46ff1-163">Bereiten Sie sich darauf vor, dass Ihr Advise Sink-Objekt jederzeit nach Ihrem Aufruf von **Advise** und vor Ihrem Anruf bei **Unadvise** freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="46ff1-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="46ff1-164">Daher sollten Sie Ihr Advise Sink-Objekt nach der Rückgabe von **Advise** frei geben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="46ff1-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="46ff1-165">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="46ff1-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="46ff1-166">Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="46ff1-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="46ff1-167">Weitere Informationen zu Multithreading und MAPI finden Sie unter [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="46ff1-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46ff1-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46ff1-168">See also</span></span>



[<span data-ttu-id="46ff1-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="46ff1-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="46ff1-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="46ff1-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="46ff1-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="46ff1-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="46ff1-172">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="46ff1-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="46ff1-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46ff1-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

