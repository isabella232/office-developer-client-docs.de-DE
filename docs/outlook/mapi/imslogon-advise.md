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
ms.openlocfilehash: 87be00bce55fabda6271b472a9e5c446aaf8054a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792656"
---
# <a name="imslogonadvise"></a><span data-ttu-id="4a552-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="4a552-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="4a552-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a552-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a552-105">Registriert ein Objekt mit einem Anbieter für Benachrichtigungen zu Änderungen im Nachrichtenspeicher Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4a552-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="4a552-106">Nachrichtenspeicher sendet dann Benachrichtigungen zu Änderungen an das registrierte Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a552-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4a552-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a552-107">Parameters</span></span>

 <span data-ttu-id="4a552-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4a552-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="4a552-109">[in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4a552-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4a552-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4a552-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="4a552-111">[in] Ein Zeiger auf die Eintrags-ID des Objekts darüber, welche Benachrichtigungen generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a552-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="4a552-112">Dieses Objekt kann es sich um einen Ordner, eine Nachricht oder ein anderes Objekt in der Nachrichtenspeicher sein.</span><span class="sxs-lookup"><span data-stu-id="4a552-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="4a552-113">Alternativ MAPI der _CbEntryID_ -Parameter auf 0 festgelegt, und übergibt **null** für _LpEntryID_, werden der Advise-Empfänger Benachrichtigungen zu Änderungen an den Speicher für die gesamte Nachricht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4a552-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="4a552-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4a552-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="4a552-115">[in] Ein Ereignismaske der Typen der Benachrichtigungsereignisse für das Objekt zu dem MAPI-Benachrichtigungen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a552-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="4a552-116">Die Maske Filter Sonderfälle.</span><span class="sxs-lookup"><span data-stu-id="4a552-116">The mask filters specific cases.</span></span> <span data-ttu-id="4a552-117">Jeder Ereignistyp hat eine Struktur zugeordnet, die zusätzliche Informationen über das Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="4a552-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="4a552-118">Die folgende Tabelle enthält die möglichen Ereignistypen zusammen mit ihren entsprechenden Strukturen.</span><span class="sxs-lookup"><span data-stu-id="4a552-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="4a552-119">**Benachrichtigungstyp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="4a552-119">**Notification event type**</span></span>|<span data-ttu-id="4a552-120">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="4a552-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a552-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="4a552-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="4a552-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="4a552-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="4a552-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="4a552-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="4a552-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="4a552-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="4a552-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4a552-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="4a552-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="4a552-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4a552-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="4a552-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="4a552-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4a552-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="4a552-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="4a552-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4a552-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="4a552-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="4a552-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4a552-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="4a552-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="4a552-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4a552-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="4a552-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="4a552-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a552-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="4a552-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4a552-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4a552-140">[in] Ein Zeiger auf eine Advise-Empfängerobjekt aufgerufen werden, wenn ein Ereignis für das Sitzungsobjekt auftritt darüber, welche Benachrichtigung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a552-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="4a552-141">Diese Advise-Empfängerobjekt muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4a552-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="4a552-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4a552-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="4a552-143">[out] Ein Zeiger auf eine Variable, die bei einer erfolgreichen Rückgabe die Anzahl der Verbindung für die benachrichtigungsregistrierung enthält.</span><span class="sxs-lookup"><span data-stu-id="4a552-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="4a552-144">Die Nummer muss ungleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4a552-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a552-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a552-145">Return value</span></span>

<span data-ttu-id="4a552-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a552-146">S_OK</span></span> 
  
> <span data-ttu-id="4a552-147">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="4a552-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4a552-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4a552-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4a552-149">Der Vorgang wird durch MAPI oder durch eine oder mehrere Dienstanbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4a552-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a552-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a552-150">Remarks</span></span>

<span data-ttu-id="4a552-151">Nachricht-Anbieter implementiert die **IMSLogon::Advise** -Methode, um ein Objekt für Benachrichtigung Rückrufe registrieren.</span><span class="sxs-lookup"><span data-stu-id="4a552-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="4a552-152">Wenn eine Änderung für das angegebene Objekt auftritt, überprüft der Anbieter finden Sie unter welche Ereignis Maskenbit im Parameter _UlEventMask_ gesetzt wurde und somit die Art der Änderung.</span><span class="sxs-lookup"><span data-stu-id="4a552-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="4a552-153">Wenn ein bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Empfängerobjekt durch den Parameter _LpAdviseSink_ Sie das Ereignis melden angegeben.</span><span class="sxs-lookup"><span data-stu-id="4a552-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="4a552-154">Daten, die in der Benachrichtigungsstruktur der **OnNotify** Routine übergeben wird das Ereignis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a552-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="4a552-155">Der Aufruf von **OnNotify** kann auftreten, während des Anrufs, der das Objekt geändert wird, oder zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="4a552-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="4a552-156">Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auf einem beliebigen Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="4a552-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="4a552-157">Um einen Anruf an **OnNotify** sicher zu behandeln, die zu einem ungünstigen Zeitpunkt auftreten, sollte eine Clientanwendung die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a552-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="4a552-158">Um Benachrichtigungen zu ermöglichen, der Nachricht Speicher-Anbieter, der **Advise** muss eine Kopie des Zeigers auf das _LpAdviseSink_ implementiert advise-Empfängerobjekt; Hierzu ruft der Anbieter die [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) -Methode für die Advise-Empfänger, dessen Objektzeiger verwalten, bis benachrichtigungsregistrierung mit einem Aufruf der Methode [IMSLogon::Unadvise](imslogon-unadvise.md) abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="4a552-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="4a552-159">Die **Advise** -Implementierung sollte weisen eine Verbindungsnummer zu der benachrichtigungsregistrierung und rufen **AddRef** für diese Verbindungsnummer vor der Rückgabe im _LpulConnection_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="4a552-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="4a552-160">Dienstanbieter können das Empfängerobjekt Advise freigeben, müssen sie die Nummer nicht freigeben, bis **Unadvise** aufgerufen wurde, bevor die Registrierung wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4a552-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="4a552-161">Nachdem ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor **Unadvise** aufgerufen wurde, müssen für das Empfängerobjekt Advise freigegeben werden muss Anbieter vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="4a552-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="4a552-162">Daher sollte ein Anbieter seine Advise-Empfängerobjekt freigeben, nachdem **Advise** zurückgegeben wird, sofern eine bestimmte langfristige Verwendung dafür ist.</span><span class="sxs-lookup"><span data-stu-id="4a552-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="4a552-163">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4a552-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a552-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a552-164">See also</span></span>



[<span data-ttu-id="4a552-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4a552-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4a552-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4a552-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4a552-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4a552-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="4a552-168">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="4a552-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4a552-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a552-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

