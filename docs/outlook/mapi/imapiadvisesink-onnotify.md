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
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351443"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="d335a-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d335a-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="d335a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d335a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d335a-105">Reagiert auf eine Benachrichtigung, indem eine oder mehrere Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d335a-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="d335a-106">Die ausgeführten Aufgaben hängen vom Ereignistyp und dem Objekt ab, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="d335a-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="d335a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d335a-107">Parameters</span></span>

 <span data-ttu-id="d335a-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="d335a-108">_cNotif_</span></span>
  
> <span data-ttu-id="d335a-109">in Die Anzahl der [Benachrichtigungs](notification.md) Strukturen, auf die durch den _lpNotifications_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d335a-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="d335a-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="d335a-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="d335a-111">in Ein Zeiger auf eine oder mehrere **Benachrichtigungs** Strukturen, die Informationen zu den aufgetretenen Ereignissen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d335a-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d335a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d335a-112">Return value</span></span>

<span data-ttu-id="d335a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d335a-113">S_OK</span></span> 
  
> <span data-ttu-id="d335a-114">Die Benachrichtigung wurde erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d335a-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d335a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d335a-115">Remarks</span></span>

<span data-ttu-id="d335a-116">Der Benachrichtigungsprozess wird gestartet, wenn ein Client oder eine MAPI einen Anruf an die **Advise** -Methode eines Dienstanbieters durchführt, um sich für ein bestimmtes Objekt für eine Benachrichtigung eines bestimmten Typs zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d335a-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="d335a-117">Einer der Parameter für die **Advise** -Methode ist ein Zeiger auf ein Advise-Objekt, das die [IMAPIAdviseSink](imapiadvisesinkiunknown.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="d335a-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="d335a-118">Wenn ein Ereignis für das Zielobjekt auftritt, das der registrierten Benachrichtigung entspricht, ruft der Dienstanbieter, entweder direkt oder indirekt über MAPI, die onNotify- \*\*\*\* Methode der Advise-Senke auf.</span><span class="sxs-lookup"><span data-stu-id="d335a-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="d335a-119">Der Aufruf von **OnNotify** kann entweder während des MAPI-Aufrufs auftreten, der das Ereignis verursacht, oder zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="d335a-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="d335a-120">Auf Systemen, die mehrere Threads der Ausführung unter \*\*\*\* stützen, kann OnNotify entweder im gleichen Thread aufgerufen werden, der für die Registrierung oder in einem anderen Thread verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d335a-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="d335a-121">Clients können sicherstellen, dass \*\*\*\* der OnNotify-Aufruf über den gleichen Thread erfolgt, der zum Aufrufen von **Advise** verwendet wird, indem die Advise-Senke erstellt wird, die Sie an **Advise** mit der [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="d335a-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="d335a-122">Der _lpNotifications_ -Parameter verweist auf eine oder \*\*\*\* mehrere Benachrichtigungs Strukturen, die beschreiben, was während des Ereignisses geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d335a-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="d335a-123">Es gibt eine andere Art von **Benachrichtigungs** Struktur für jede Art von Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d335a-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="d335a-124">In der folgenden Tabelle sind die Werte aufgeführt, die verwendet werden, um die möglichen Ereignistypen und die jedem Wert zugeordneten Strukturen darzustellen:</span><span class="sxs-lookup"><span data-stu-id="d335a-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="d335a-125">**Benachrichtigungs Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="d335a-125">**Notification event type**</span></span>|<span data-ttu-id="d335a-126">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="d335a-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d335a-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="d335a-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="d335a-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="d335a-129">**Uleventmaskfnevnewmail**</span><span class="sxs-lookup"><span data-stu-id="d335a-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="d335a-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="d335a-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="d335a-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="d335a-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d335a-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="d335a-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="d335a-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d335a-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="d335a-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="d335a-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d335a-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="d335a-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="d335a-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d335a-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="d335a-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="d335a-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d335a-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="d335a-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="d335a-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="d335a-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="d335a-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="d335a-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="d335a-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="d335a-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="d335a-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d335a-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="d335a-147">Weitere Informationen zum Einrichten und Beenden von Benachrichtigungen finden Sie in den Referenz Einträgen für die Methoden **Advise** und **Unadvise** für die folgenden Schnittstellen: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)und [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d335a-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="d335a-148">Allgemeine Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="d335a-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d335a-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d335a-149">Notes to implementers</span></span>

<span data-ttu-id="d335a-150">Ihre **OnNotify** -Implementierung besteht in der Regel aus einem oder mehreren Codeblöcken für jeden Benachrichtigungstyp, den Sie erwarten.</span><span class="sxs-lookup"><span data-stu-id="d335a-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="d335a-151">Führen Sie innerhalb dieser Codeblöcke alle Aufgaben aus, die Sie als Antwort auf die Benachrichtigung als erforderlich betrachten.</span><span class="sxs-lookup"><span data-stu-id="d335a-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="d335a-152">Angenommen, Sie registrieren, um **fnevObjectModified** -Benachrichtigungen für einen Ordner zu erhalten, der in einer Dialogfeldanzeige enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d335a-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="d335a-153">In dem Codeblock, den Sie in Ihre **OnNotify** -Methode aufnehmen, um **fnevObjectModified** -Benachrichtigungen zu behandeln, können Sie eine Windows-Meldung an das Dialogfeld senden, um eine aktualisierte Anzeige anzufordern.</span><span class="sxs-lookup"><span data-stu-id="d335a-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="d335a-154">Ändern oder freigeben Sie die **Benachrichtigungs** Struktur, die an OnNotify übergeben wurde, nicht. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d335a-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="d335a-155">Die Daten in der Struktur sind nur gültig, \*\*\*\* wenn OnNotify zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d335a-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d335a-156">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d335a-156">Notes to callers</span></span>

<span data-ttu-id="d335a-157">Wenn Änderungen an mehreren Objekten auftreten, können Sie eine registrierte Advise-Senke in einem einzelnen Aufruf \*\*\*\* von OnNotify oder in mehreren anrufen abhängig von Arbeitsspeichereinschränkungen benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="d335a-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="d335a-158">Dies gilt unabhängig davon, ob die Änderungen das Ergebnis eines Methodenaufrufs oder mehrere sind.</span><span class="sxs-lookup"><span data-stu-id="d335a-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="d335a-159">Beispielsweise kann ein Aufruf von [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) mehrere Nachrichten und Ordner betreffen.</span><span class="sxs-lookup"><span data-stu-id="d335a-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="d335a-160">Als Nachrichtenspeicher Anbieter können Sie einen Aufruf von onNotify mit \*\*\*\* einem **fnevObjectModified** -Ereignistyp für den Zielordner oder zahlreiche Aufrufe durchführen, und zwar einen für jeden Nachrichten Affekt.</span><span class="sxs-lookup"><span data-stu-id="d335a-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="d335a-161">Wenn ein Client wiederholt [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md)aufruft, können diese Aufrufe in einem **fnevObjectModified** -Ereignis für den Ordner kombiniert oder für jede neue Nachricht in einzelne **fnevObjectCreated** -Ereignisse aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d335a-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="d335a-162">Weitere Informationen dazu, wie und wann Benachrichtigungen generiert werden, finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="d335a-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d335a-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d335a-163">MFCMAPI reference</span></span>

<span data-ttu-id="d335a-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d335a-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d335a-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d335a-165">**File**</span></span>|<span data-ttu-id="d335a-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d335a-166">**Function**</span></span>|<span data-ttu-id="d335a-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d335a-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d335a-168">AdviseSink. h und AdviseSink. cpp</span><span class="sxs-lookup"><span data-stu-id="d335a-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="d335a-169">CAdviseSink:: OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="d335a-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="d335a-170">Die CAdviseSink-Klasse wird implementiert, um alle Benachrichtigungen in MFCMAPI zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="d335a-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d335a-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d335a-171">See also</span></span>



[<span data-ttu-id="d335a-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d335a-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="d335a-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d335a-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="d335a-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="d335a-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="d335a-175">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="d335a-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="d335a-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d335a-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="d335a-177">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d335a-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

