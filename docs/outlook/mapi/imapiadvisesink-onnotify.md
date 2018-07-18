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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792058"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="74bbf-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="74bbf-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="74bbf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74bbf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74bbf-105">Antwortet auf eine Benachrichtigung durch eine oder mehrere Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="74bbf-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="74bbf-106">Die Aufgaben ausgeführt, abhängig von den Typ des Ereignisses und das Objekt, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="74bbf-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="74bbf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="74bbf-107">Parameters</span></span>

 <span data-ttu-id="74bbf-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="74bbf-108">_cNotif_</span></span>
  
> <span data-ttu-id="74bbf-109">[in] Die Anzahl der [Benachrichtigung](notification.md) Strukturen auf den durch den Parameter _LpNotifications_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="74bbf-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="74bbf-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="74bbf-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="74bbf-111">[in] Ein Zeiger auf eine oder mehrere **Benachrichtigung** -Strukturen, die Informationen zu den Ereignissen bereitstellen, die aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="74bbf-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="74bbf-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="74bbf-112">Return value</span></span>

<span data-ttu-id="74bbf-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="74bbf-113">S_OK</span></span> 
  
> <span data-ttu-id="74bbf-114">Die Benachrichtigung wurde erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="74bbf-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74bbf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74bbf-115">Remarks</span></span>

<span data-ttu-id="74bbf-116">Der Benachrichtigungsprozess beginnt, wenn ein Client oder MAPI **Advise** -Methode des Dienstanbieters registrieren, um eine Benachrichtigung eines bestimmten Typs für ein bestimmtes Objekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="74bbf-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="74bbf-117">Einer der Parameter der **Advise** -Methode ist ein Zeiger auf ein Objekt der Advise-Empfänger, die die [IMAPIAdviseSink](imapiadvisesinkiunknown.md) -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="74bbf-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="74bbf-118">Bei Auftreten eines Ereignisses auf dem Zielobjekt, das die registrierten Benachrichtigung, den Dienstanbieter entweder direkt oder indirekt über MAPI, entspricht, wird der Advise-Empfänger **OnNotify** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="74bbf-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="74bbf-119">Der Aufruf von **OnNotify** kann auftreten, während der MAPI-Aufruf, der das Ereignis verursacht oder zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="74bbf-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="74bbf-120">Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann die **OnNotify** auf dem gleichen Thread, der für die Registrierung verwendet wurde oder in einem anderen Thread aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="74bbf-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="74bbf-121">Clients können sicherstellen, dass die **OnNotify** , auf dem gleichen Thread, der zum Aufrufen der **Advise aufgerufen wird** durch Erstellen von der Advise-Empfänger, den sie mit der Funktion [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) an **Advise** übergeben verwendet.</span><span class="sxs-lookup"><span data-stu-id="74bbf-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="74bbf-122">Der Parameter _LpNotifications_ verweist auf ein oder mehrere **Benachrichtigung** Strukturen, die beschreiben, was während des Ereignisses geändert hat.</span><span class="sxs-lookup"><span data-stu-id="74bbf-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="74bbf-123">Es ist eine andere Art von **Benachrichtigung** Struktur für jeden Typ von Ereignis.</span><span class="sxs-lookup"><span data-stu-id="74bbf-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="74bbf-124">Die folgende Tabelle enthält die Werte, die zur Darstellung der möglichen Types von Ereignissen und die Verbindung mit jedem Wert Strukturen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74bbf-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="74bbf-125">**Benachrichtigungstyp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74bbf-125">**Notification event type**</span></span>|<span data-ttu-id="74bbf-126">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="74bbf-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="74bbf-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="74bbf-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="74bbf-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="74bbf-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="74bbf-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="74bbf-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="74bbf-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="74bbf-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="74bbf-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="74bbf-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="74bbf-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="74bbf-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="74bbf-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="74bbf-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="74bbf-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="74bbf-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="74bbf-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="74bbf-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="74bbf-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="74bbf-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="74bbf-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="74bbf-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="74bbf-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="74bbf-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="74bbf-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="74bbf-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="74bbf-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="74bbf-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="74bbf-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="74bbf-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="74bbf-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="74bbf-147">Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie unter Referenz Einträge für die **Advise** und **Unadvise** Methoden aus einem der folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="74bbf-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="74bbf-148">Allgemeine Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="74bbf-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="74bbf-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="74bbf-149">Notes to implementers</span></span>

<span data-ttu-id="74bbf-150">Die Implementierung **OnNotify** wird in der Regel eine oder mehrere Codeblöcke für jede Art von Benachrichtigung bestehen, den Sie erwarten.</span><span class="sxs-lookup"><span data-stu-id="74bbf-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="74bbf-151">Führen Sie in diese Codeblöcke alle Aufgaben, die Sie als Antwort auf die Benachrichtigung erforderlichen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="74bbf-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="74bbf-152">Angenommen Sie, dass Sie registrieren Erhalt von Benachrichtigungen der **FnevObjectModified** für einen Ordner, die in einem Dialogfeld Feld enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="74bbf-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="74bbf-153">In den Block mit Code, die Sie in Ihre **OnNotify** -Methode zum Behandeln von Benachrichtigungen **FnevObjectModified** enthalten sind können Sie eine Windows-Nachricht an das Dialogfeld zum Anfordern einer aktualisierten Anzeige senden.</span><span class="sxs-lookup"><span data-stu-id="74bbf-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="74bbf-154">Nicht ändern oder die **Benachrichtigung** Struktur übergeben **OnNotify**frei.</span><span class="sxs-lookup"><span data-stu-id="74bbf-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="74bbf-155">Die Daten in der Struktur ist gültig, nur bis **OnNotify** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74bbf-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="74bbf-156">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="74bbf-156">Notes to callers</span></span>

<span data-ttu-id="74bbf-157">Beim Auftreten von Änderungen auf mehrere Objekte können Sie eine registrierten Advise-Empfänger in einem einzigen Aufruf von **OnNotify** oder mehrere Anrufe je nach Speicherkapazität benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="74bbf-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="74bbf-158">Dies gilt unabhängig davon, ob die Änderungen das Ergebnis der Methodenaufruf eine oder mehrere sind.</span><span class="sxs-lookup"><span data-stu-id="74bbf-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="74bbf-159">Beispielsweise kann ein Aufruf von [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) mehrere Nachrichten und Ordnern auswirken.</span><span class="sxs-lookup"><span data-stu-id="74bbf-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="74bbf-160">Als einen Anbieter für Nachricht anmelden können Sie durch Aufrufen von **OnNotify** für den Zielordner oder viele Anrufe, eine für die einzelnen Nachrichten einen Einfluss darauf zu einem Ereignistyp **FnevObjectModified** machen.</span><span class="sxs-lookup"><span data-stu-id="74bbf-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="74bbf-161">Auf ähnliche Weise, wenn ein Client wiederholte Aufrufe [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), diesen anrufen oder werden können kombiniert ein **FnevObjectModified** -Ereignis für den Ordner in einzelne **FnevObjectCreated** Ereignisse für jede neue Nachricht getrennt.</span><span class="sxs-lookup"><span data-stu-id="74bbf-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="74bbf-162">Weitere Informationen dazu, wie und wann Benachrichtigungen generiert finden Sie unter [Benachrichtigung in MAPI](event-notification-in-mapi.md) und [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="74bbf-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="74bbf-163">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="74bbf-163">MFCMAPI reference</span></span>

<span data-ttu-id="74bbf-164">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74bbf-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="74bbf-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="74bbf-165">**File**</span></span>|<span data-ttu-id="74bbf-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="74bbf-166">**Function**</span></span>|<span data-ttu-id="74bbf-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="74bbf-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74bbf-168">AdviseSink.h und AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="74bbf-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="74bbf-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="74bbf-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="74bbf-170">Zum Behandeln von alle Benachrichtigungen in MFCMAPI (engl.), wird die CAdviseSink-Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="74bbf-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74bbf-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74bbf-171">See also</span></span>



[<span data-ttu-id="74bbf-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="74bbf-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="74bbf-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="74bbf-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="74bbf-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="74bbf-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="74bbf-175">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="74bbf-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="74bbf-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74bbf-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="74bbf-177">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="74bbf-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

