---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407361"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="e8ea8-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e8ea8-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="e8ea8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8ea8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8ea8-105">Antwortet auf eine Benachrichtigung, indem mindestens eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="e8ea8-106">Die ausgeführten Aufgaben hängen vom Typ des Ereignisses und dem Objekt ab, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="e8ea8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8ea8-107">Parameters</span></span>

 <span data-ttu-id="e8ea8-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="e8ea8-108">_cNotif_</span></span>
  
> <span data-ttu-id="e8ea8-109">[in] Die Anzahl der [NOTIFICATION-Strukturen,](notification.md) auf die der  _lpNotifications-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="e8ea8-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="e8ea8-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="e8ea8-111">[in] Ein Zeiger auf eine oder mehrere **NOTIFICATION-Strukturen,** die Informationen zu den aufgetretenen Ereignissen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8ea8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8ea8-112">Return value</span></span>

<span data-ttu-id="e8ea8-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8ea8-113">S_OK</span></span> 
  
> <span data-ttu-id="e8ea8-114">Die Benachrichtigung wurde erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8ea8-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8ea8-115">Remarks</span></span>

<span data-ttu-id="e8ea8-116">Der Benachrichtigungsprozess beginnt, wenn ein Client oder eine MAPI die **Advise-Methode** eines Dienstanbieters aufruft, um sich zu registrieren, um eine Benachrichtigung eines bestimmten Typs für ein bestimmtes Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="e8ea8-117">Einer der Parameter für die **Advise-Methode** ist ein Zeiger auf ein Advise Sink-Objekt, das die [IMAPIAdviseSink-Schnittstelle](imapiadvisesinkiunknown.md) implementiert.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="e8ea8-118">Wenn ein Ereignis für das Zielobjekt auftritt, das der registrierten Benachrichtigung entspricht, ruft der Dienstanbieter entweder direkt oder indirekt über MAPI die **OnNotify-Methode** der Hinweissenke auf.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="e8ea8-119">Der Aufruf von **OnNotify** kann entweder während des MAPI-Aufrufs erfolgen, der das Ereignis verursacht, oder zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="e8ea8-120">Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann **OnNotify** entweder im selben Thread aufgerufen werden, der für die Registrierung verwendet wurde, oder in einem anderen Thread.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="e8ea8-121">Clients können sicherstellen, dass der **OnNotify-Aufruf** im selben Thread ausgeführt wird, der zum Aufrufen von **Advise** verwendet wird, indem sie die Ratensenke erstellen, die sie mit der [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) an **Advise** übergeben.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="e8ea8-122">Der  _lpNotifications-Parameter_ verweist auf eine oder mehrere **NOTIFICATION-Strukturen,** die beschreiben, was sich während des Ereignisses geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="e8ea8-123">Es gibt einen anderen Typ von **NOTIFICATION-Struktur** für jeden Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="e8ea8-124">In der folgenden Tabelle sind die Werte aufgeführt, die zum Darstellen der möglichen Ereignistypen und der strukturen verwendet werden, die den einzelnen Werten zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="e8ea8-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="e8ea8-125">**Benachrichtigungsereignistyp**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-125">**Notification event type**</span></span>|<span data-ttu-id="e8ea8-126">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8ea8-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="e8ea8-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="e8ea8-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="e8ea8-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="e8ea8-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="e8ea8-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e8ea8-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="e8ea8-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e8ea8-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="e8ea8-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e8ea8-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="e8ea8-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e8ea8-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="e8ea8-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e8ea8-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="e8ea8-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="e8ea8-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="e8ea8-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="e8ea8-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="e8ea8-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e8ea8-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="e8ea8-147">Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie in den Referenzeinträgen für die **Methoden Advise** und **Unadvise** für eine der folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e8ea8-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="e8ea8-148">Allgemeine Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e8ea8-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e8ea8-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e8ea8-149">Notes to implementers</span></span>

<span data-ttu-id="e8ea8-150">Ihre **OnNotify-Implementierung** besteht in der Regel aus einem oder mehreren Codeblöcken für jeden Benachrichtigungstyp, den Sie erwarten.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="e8ea8-151">Führen Sie in diesen Codeblöcken alle Aufgaben aus, die Sie als Reaktion auf die Benachrichtigung für erforderlich halten.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="e8ea8-152">Angenommen, Sie registrieren sich für den Empfang **von fnevObjectModified-Benachrichtigungen** in einem Ordner, der in einer Dialogfeldanzeige enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="e8ea8-153">Im Codeblock, den Sie in Ihre **OnNotify-Methode** zum Behandeln von **fnevObjectModified-Benachrichtigungen** verwenden, senden Sie möglicherweise eine Windows-Nachricht an das Dialogfeld, um eine aktualisierte Anzeige an fordern.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="e8ea8-154">Ändern oder geben Sie die an OnNotify übergebene **NOTIFICATION-Struktur nicht frei.** </span><span class="sxs-lookup"><span data-stu-id="e8ea8-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="e8ea8-155">Die Daten in der Struktur sind nur gültig, bis **OnNotify zurückgegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8ea8-156">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e8ea8-156">Notes to callers</span></span>

<span data-ttu-id="e8ea8-157">Wenn Änderungen an mehreren Objekten vorgenommen werden, können Sie eine registrierte Ratensenke in einem einzigen Aufruf von **OnNotify** oder in mehreren Aufrufen in Abhängigkeit von Speichereinschränkungen benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="e8ea8-158">Dies gilt unabhängig davon, ob die Änderungen das Ergebnis eines oder mehrerer Methodenaufrufe sind.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="e8ea8-159">Ein Aufruf von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) kann sich beispielsweise auf mehrere Nachrichten und Ordner auswirken.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="e8ea8-160">Als Nachrichtenspeicheranbieter können Sie einen Aufruf von **OnNotify** mit einem **fnevObjectModified-Ereignistyp** für den Zielordner oder viele Aufrufe, einen für jede Auswirkung auf Nachrichten, erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="e8ea8-161">Wenn ein Client wiederholt [ImAPIFolder::CreateMessage](imapifolder-createmessage.md)aufruft, können diese Aufrufe in einem **fnevObjectModified-Ereignis** für den Ordner kombiniert oder in einzelne **fnevObjectCreated-Ereignisse** für jede neue Nachricht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="e8ea8-162">Weitere Informationen dazu, wie und wann Benachrichtigungen generiert werden, finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="e8ea8-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8ea8-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="e8ea8-163">MFCMAPI reference</span></span>

<span data-ttu-id="e8ea8-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8ea8-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-165">**File**</span></span>|<span data-ttu-id="e8ea8-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-166">**Function**</span></span>|<span data-ttu-id="e8ea8-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e8ea8-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8ea8-168">AdviseSink.h und AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="e8ea8-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="e8ea8-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="e8ea8-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="e8ea8-170">Die CAdviseSink-Klasse ist implementiert, um alle Benachrichtigungen in MFCMAPI zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="e8ea8-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8ea8-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8ea8-171">See also</span></span>



[<span data-ttu-id="e8ea8-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e8ea8-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="e8ea8-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e8ea8-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="e8ea8-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="e8ea8-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="e8ea8-175">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="e8ea8-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e8ea8-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8ea8-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="e8ea8-177">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e8ea8-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

