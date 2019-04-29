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
# <a name="iablogonadvise"></a><span data-ttu-id="eb862-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="eb862-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="eb862-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb862-105">Registriert den Anrufer so, dass er Benachrichtigungen über angegebene Ereignisse erhält, die sich auf einen Container, einen Messagingbenutzer oder eine Verteilerliste auswirken.</span><span class="sxs-lookup"><span data-stu-id="eb862-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="eb862-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb862-106">Parameters</span></span>

 <span data-ttu-id="eb862-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="eb862-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="eb862-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="eb862-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="eb862-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="eb862-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="eb862-110">in Ein Zeiger auf die Eintrags-ID des Objekts, über das Benachrichtigungen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb862-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="eb862-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="eb862-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="eb862-112">in Eine Bitmaske von Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist, und die in die Registrierung aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb862-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="eb862-113">Jeder Art von Ereignis [](notification.md) , das Informationen über das Ereignis enthält, ist eine entsprechende Benachrichtigungsstruktur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="eb862-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="eb862-114">In der folgenden Tabelle sind die gültigen Werte für den _ulEventMask_ -Parameter und die jedem Wert zugeordneten Strukturen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb862-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="eb862-115">**Benachrichtigungs Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="eb862-115">**Notification event type**</span></span>|<span data-ttu-id="eb862-116">**Entsprechende **Benachrichtigungs** Struktur**</span><span class="sxs-lookup"><span data-stu-id="eb862-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb862-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="eb862-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="eb862-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="eb862-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="eb862-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="eb862-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="eb862-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="eb862-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="eb862-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="eb862-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="eb862-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="eb862-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="eb862-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="eb862-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="eb862-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="eb862-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="eb862-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="eb862-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="eb862-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="eb862-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="eb862-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="eb862-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="eb862-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="eb862-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="eb862-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="eb862-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="eb862-130">in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="eb862-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="eb862-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="eb862-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="eb862-132">Out Ein Zeiger auf einen Wert ungleich NULL, der die Benachrichtigungs Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb862-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb862-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb862-133">Return value</span></span>

<span data-ttu-id="eb862-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb862-134">S_OK</span></span> 
  
> <span data-ttu-id="eb862-135">Die Benachrichtigungs Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="eb862-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="eb862-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="eb862-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="eb862-137">Die im _lpEntryID_ -Parameter übergebene Eintrags-ID weist nicht das entsprechende Format auf.</span><span class="sxs-lookup"><span data-stu-id="eb862-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="eb862-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="eb862-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="eb862-139">Der Adressbuchanbieter unterstützt keine Benachrichtigung, da möglicherweise keine Änderungen an den Objekten vorgenommen werden können.</span><span class="sxs-lookup"><span data-stu-id="eb862-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="eb862-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="eb862-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="eb862-141">Der Adressbuchanbieter kann den in _lpEntryID_übergebenen Eintragsbezeichner nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="eb862-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb862-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb862-142">Remarks</span></span>

<span data-ttu-id="eb862-143">Adressbuchanbieter implementieren die **IABLogon:: Advise** -Methode, um den Anrufer zu registrieren, der benachrichtigt werden soll, wenn eine Änderung an einem Objekt in einem ihrer Container erfolgt.</span><span class="sxs-lookup"><span data-stu-id="eb862-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="eb862-144">Anrufer können sich für Benachrichtigungen zu Messaging Benutzern, Verteilerlisten oder ganzen Containern registrieren.</span><span class="sxs-lookup"><span data-stu-id="eb862-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="eb862-145">Clients rufen in der Regel die [IAddrBook:: Advise](iaddrbook-advise.md) -Methode auf, um Adressbuch Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="eb862-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="eb862-146">Anschließend ruft MAPI die **Advise** -Methode des Adressbuch Anbieters auf, der für das durch den Eintragsbezeichner in _lpEntryID_dargestellte Objekt zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="eb862-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="eb862-147">Wenn eine Änderung an dem angegebenen Objekt des in _ulEventMask_dargestellten Typs erfolgt, wird ein Aufruf an die OnNotify-Methode der Advise-Senke durch _lpAdviseSink_verwiesen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="eb862-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="eb862-148">Die Daten, die \*\*\*\* in der Benachrichtigungsstruktur an die OnNotify-Routine übergeben werden, beschreiben das Ereignis. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="eb862-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eb862-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="eb862-149">Notes to implementers</span></span>

<span data-ttu-id="eb862-150">Sie können Benachrichtigungen mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eb862-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="eb862-151">MAPI verfügt über drei Support Objektmethoden, mit denen Dienstanbieter Benachrichtigungen implementieren können:</span><span class="sxs-lookup"><span data-stu-id="eb862-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="eb862-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="eb862-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="eb862-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="eb862-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="eb862-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="eb862-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="eb862-155">Wenn Sie die MAPI-Supportmethoden verwenden möchten, rufen Sie **subscribe** auf, wenn Ihre **Advise** -Methode aufgerufen wird, und geben Sie den _lpAdviseSink_ -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="eb862-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="eb862-156">Wenn Sie sich für die Unterstützung der Benachrichtigung entscheiden, rufen Sie die **AddRef** -Methode der durch den _lpAdviseSink_ -Parameter dargestellten Advise-Senke auf, um eine Kopie dieses Zeigers aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="eb862-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="eb862-157">Bewahren Sie diese Kopie auf, bis die [IABLogon:: Unadvise](iablogon-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="eb862-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="eb862-158">Unabhängig davon, wie Sie die Benachrichtigung unterstützen, weisen Sie der Benachrichtigungs Registrierung eine unGleich NULL-Verbindung zu und geben Sie im _lpulConnection_ -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="eb862-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="eb862-159">Geben Sie diese Verbindungsnummer erst frei, \*\*\*\* wenn die Unadvise-Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="eb862-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb862-160">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eb862-160">Notes to callers</span></span>

<span data-ttu-id="eb862-161">Der Advise-Senke-Zeiger, den Sie im _lpAdviseSink_ -Parameter an **Advise** übergeben, kann auf ein Objekt verweisen, das Sie erstellt haben oder die MAPI über die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="eb862-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="eb862-162">Möglicherweise möchten Sie **HrThisThreadAdviseSink** verwenden, wenn Sie mehrere Threads der Ausführung unterstützen und sicher sein möchten, dass nachfolgende \*\*\*\* Aufrufe an Ihre OnNotify-Methode zu einem geeigneten Zeitpunkt in einem entsprechenden Thread stattfinden.</span><span class="sxs-lookup"><span data-stu-id="eb862-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="eb862-163">Bereiten Sie sich darauf vor, dass Ihr Advise-Senke-Objekt jederzeit nach dem Anruf zur **Beratung** und vor dem Aufruf von Unadvise freigegeben werden kann. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="eb862-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="eb862-164">Daher sollten Sie Ihr Advise-Senke-Objekt nach der Rückgabe von **Advise** freigeben, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="eb862-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="eb862-165">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="eb862-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="eb862-166">Informationen zur Verwendung der **IMAPISupport** -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="eb862-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="eb862-167">Weitere Informationen zu Multithreading und MAPI finden Sie unter [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="eb862-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb862-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb862-168">See also</span></span>



[<span data-ttu-id="eb862-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="eb862-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="eb862-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="eb862-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="eb862-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="eb862-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="eb862-172">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="eb862-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="eb862-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb862-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

