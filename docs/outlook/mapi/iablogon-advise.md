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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791978"
---
# <a name="iablogonadvise"></a><span data-ttu-id="0bd3f-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="0bd3f-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="0bd3f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bd3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bd3f-105">Den Anrufer, um die Benachrichtigung der angegebenen Ereignisse, die einen Container, messaging-Benutzer oder Verteilerliste betreffen registriert.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0bd3f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bd3f-106">Parameters</span></span>

 <span data-ttu-id="0bd3f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0bd3f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0bd3f-108">[in] Die Anzahl von Bytes in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0bd3f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0bd3f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0bd3f-110">[in] Ein Zeiger auf die Eintrags-ID des Objekts darüber, welche Benachrichtigungen generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="0bd3f-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="0bd3f-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="0bd3f-112">[in] Eine Bitmaske der Werte, die die Typen von Benachrichtigungsereignisse anzugeben, die dem Anrufer ist daran interessiert, und die Registrierung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="0bd3f-113">Es wird eine entsprechende [Benachrichtigung](notification.md) Struktur jede Art von Ereignis, das Informationen über das Ereignis enthält zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="0bd3f-114">Die folgende Tabelle enthält die gültigen Werte für den Parameter _UlEventMask_ und die Strukturen jeden Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="0bd3f-115">**Benachrichtigungstyp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-115">**Notification event type**</span></span>|<span data-ttu-id="0bd3f-116">**Entsprechende **Benachrichtigung** -Struktur**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0bd3f-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="0bd3f-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0bd3f-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="0bd3f-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="0bd3f-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0bd3f-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0bd3f-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="0bd3f-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="0bd3f-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="0bd3f-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="0bd3f-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="0bd3f-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="0bd3f-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="0bd3f-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0bd3f-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="0bd3f-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="0bd3f-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="0bd3f-130">[in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="0bd3f-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="0bd3f-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="0bd3f-132">[out] Ein Zeiger auf einen Wert ungleich NULL, der die benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0bd3f-133">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0bd3f-133">Return value</span></span>

<span data-ttu-id="0bd3f-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="0bd3f-134">S_OK</span></span> 
  
> <span data-ttu-id="0bd3f-135">Die benachrichtigungsregistrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="0bd3f-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0bd3f-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="0bd3f-137">Die Eintrags-ID in der _LpEntryID_ -Parameter übergeben, ist nicht im entsprechenden Format.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="0bd3f-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0bd3f-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0bd3f-139">Der Adressbuchanbieter unterstützt Benachrichtigung, möglicherweise nicht, da keine Änderungen auf Objekte getroffen werden können.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="0bd3f-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0bd3f-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0bd3f-141">Der Adressbuchanbieter kann nicht die Eintrags-ID _LpEntryID_übergebenen behandeln.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bd3f-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bd3f-142">Remarks</span></span>

<span data-ttu-id="0bd3f-143">Von adressbuchanbietern implementierte implementieren Sie die **IABLogon::Advise** -Methode zum Registrieren des Aufrufers benachrichtigt werden, wenn ein Objekt in einem der deren Container, geändert.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="0bd3f-144">Anrufer können für Benachrichtigungen bezüglich messaging-Benutzern, Verteilerlisten oder gesamte Container registrieren.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="0bd3f-145">Clients aufrufen in der Regel die [IAddrBook::Advise](iaddrbook-advise.md) -Methode für Address Book Benachrichtigungen registriert.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="0bd3f-146">MAPI ruft dann die **Advise** -Methode des Adressbuchanbieter an, der für das Objekt, dargestellt durch die Eintrags-ID in _LpEntryID_zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="0bd3f-147">Tritt eine Änderung auf das angegebene Objekt vom Typ in _UlEventMask_dargestellt, ist die **OnNotify** -Methode der Advise-Empfänger, die auf den _LpAdviseSink_aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="0bd3f-148">Daten, die in der **Benachrichtigung** Struktur der **OnNotify** Routine übergeben wird das Ereignis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0bd3f-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="0bd3f-149">Notes to implementers</span></span>

<span data-ttu-id="0bd3f-150">Sie können die Benachrichtigung mit oder ohne Hilfe von MAPI unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="0bd3f-151">MAPI hat drei Support-Objektmethoden zu Dienstanbietern Benachrichtigung zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="0bd3f-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="0bd3f-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="0bd3f-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="0bd3f-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="0bd3f-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="0bd3f-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="0bd3f-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="0bd3f-155">Wenn Sie sich entscheiden, die MAPI-Support-Methoden verwenden, rufen Sie **Abonnieren** die **Advise** -Methode aufgerufen wird, und heben Sie den Zeiger _LpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="0bd3f-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="0bd3f-156">Wenn Sie sich entscheiden, die Benachrichtigung zu unterstützen, rufen Sie die **AddRef** -Methode der Advise-Empfänger, die durch den Parameter _LpAdviseSink_ dargestellt, um eine Kopie dieses Zeigers beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="0bd3f-157">Verwalten Sie diese Kopie, bis die [IABLogon::Unadvise](iablogon-unadvise.md) -Methode aufgerufen wird, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="0bd3f-158">Unabhängig davon, wie Sie Benachrichtigung zu unterstützen weisen Sie eine Zahl ungleich NULL Verbindung die benachrichtigungsregistrierung, und im Parameter _LpulConnection_ zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="0bd3f-159">Freigegeben Sie diese Verbindungsnummer nicht, bis die **Unadvise** -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0bd3f-160">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0bd3f-160">Notes to callers</span></span>

<span data-ttu-id="0bd3f-161">Der Advise Empfängerzeiger, den im Parameter _LpAdviseSink_ **Advise** übergebene kann auf ein Objekt verweisen, die Sie erstellt haben oder die MAPI über die Funktion [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="0bd3f-162">Sie möchten möglicherweise **HrThisThreadAdviseSink** zu verwenden, wenn Sie die Unterstützung von mehreren Threads der Ausführung und möchten, um sicherzustellen, dass, die nachfolgende Aufrufe an die **OnNotify** -Methode zu einem geeigneten Zeitpunkt in einem entsprechenden Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="0bd3f-163">Bereiten Sie für Ihre Advise-Empfängerobjekt jederzeit nach Ihren Anruf von der **Advise** und vor den Anruf auf **Unadvise**freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="0bd3f-164">Aus diesem Grund sollten Sie Ihre Advise-Empfängerobjekt freigeben nach **Advise** zurückgegeben wird, es sei denn, Sie eine bestimmte langfristige Verwendung dafür haben.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="0bd3f-165">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0bd3f-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="0bd3f-166">Informationen dazu, wie Sie die **IMAPISupport** -Methoden verwenden, um die Benachrichtigung zu unterstützen finden Sie unter [Event Notification unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="0bd3f-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="0bd3f-167">Weitere Informationen zu multithreading und MAPI, [Threading in MAPI](threading-in-mapi.md)finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="0bd3f-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0bd3f-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bd3f-168">See also</span></span>



[<span data-ttu-id="0bd3f-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0bd3f-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="0bd3f-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0bd3f-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="0bd3f-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0bd3f-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0bd3f-172">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0bd3f-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="0bd3f-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bd3f-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

