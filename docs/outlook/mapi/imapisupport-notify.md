---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435936"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="74464-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="74464-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="74464-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74464-105">Sendet eine Benachrichtigung über ein angegebenes Ereignis an eine Hinweisquelle, die ursprünglich über die [IMAPISupport::Subscribe-Methode](imapisupport-subscribe.md) für die Benachrichtigung registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="74464-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="74464-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74464-106">Parameters</span></span>

<span data-ttu-id="74464-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="74464-107">_lpKey_</span></span>
  
> <span data-ttu-id="74464-108">[in] Ein Zeiger auf den Benachrichtigungsschlüssel für das advise-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="74464-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="74464-109">Der  _lpKey-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="74464-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="74464-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="74464-110">_cNotification_</span></span>
  
> <span data-ttu-id="74464-111">[in] Die Anzahl der Benachrichtigungsstrukturen, auf die der  _lpNotifications-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="74464-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="74464-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="74464-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="74464-113">[in] Ein Zeiger auf ein Array von [NOTIFICATION-Strukturen,](notification.md) die ausstehende Benachrichtigungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="74464-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="74464-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="74464-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="74464-115">[in, out] Eine Bitmaske mit Flags, die den Benachrichtigungsprozess steuert.</span><span class="sxs-lookup"><span data-stu-id="74464-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="74464-116">Bei der Eingabe kann das folgende Flag festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="74464-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="74464-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74464-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="74464-118">Die Zeichenfolgen in den Benachrichtigungsstrukturen, auf die  _von lpNotifications_ verwiesen wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="74464-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="74464-119">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="74464-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="74464-120">Bei der Ausgabe kann MAPI das folgende Flag festlegen:</span><span class="sxs-lookup"><span data-stu-id="74464-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="74464-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="74464-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="74464-122">Eine Rückruffunktion hat eine synchrone Benachrichtigung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="74464-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74464-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74464-123">Return value</span></span>

<span data-ttu-id="74464-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="74464-124">S_OK</span></span> 
  
> <span data-ttu-id="74464-125">Die Benachrichtigungen wurden erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="74464-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74464-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="74464-126">Remarks</span></span>

<span data-ttu-id="74464-127">Die **IMAPISupport::Notify-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="74464-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="74464-128">Dienstanbieter rufen **Notify auf,** um an zu fordern, dass MAPI eine Benachrichtigung für eine Ratgebersenke generiert, die zuvor über die **IMAPISupport::Subscribe-Methode** für die Benachrichtigung registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="74464-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="74464-129">**Notify** kopiert die Strukturen, auf die der  _lpNotifications-Parameter_ verweist, in den Arbeitsspeicher und ruft die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der entsprechenden Ratensenke auf.</span><span class="sxs-lookup"><span data-stu-id="74464-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="74464-130">Wenn **OnNotify** mit der Benachrichtigung fertig ist, gibt es den betroffenen Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="74464-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="74464-131">Der Aufrufer muss keinen Arbeitsspeicher zuweisen. MAPI führt alle erforderlichen Speicherzuweisungen durch.</span><span class="sxs-lookup"><span data-stu-id="74464-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="74464-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="74464-132">Notes to callers</span></span>

<span data-ttu-id="74464-133">Der im  _lpKey-Parameter_ übergebene Benachrichtigungsschlüssel sollte mit dem schlüssel identisch sein, der in  _lpKey_ an die **IMAPISupport::Subscribe-Methode übergeben** wurde.</span><span class="sxs-lookup"><span data-stu-id="74464-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="74464-134">Viele Anbieter verwenden den Eintragsbezeichner der Quelle "Advise" als Schlüssel, aber andere Daten, z. B. ein Dateipfad, können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74464-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="74464-135">MAPI verwendet diesen Schlüssel, um alle Registrierungen für Benachrichtigungen in der identifizierten Informationsquelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="74464-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="74464-136">Stellen Sie sicher, dass Sie das **lpEntryID-Element** der Benachrichtigungsstruktur auf einen langfristigen Eintragsbezeichner festlegen.</span><span class="sxs-lookup"><span data-stu-id="74464-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="74464-137">Wenn Sie das NOTIFY_SYNC für den  Aufruf abonnieren für eine der ausstehenden Benachrichtigungen festlegen, ruft **Notify** die Rückruffunktionen der **IMAPIAdviseSink::OnNotify-Methode** auf, bevor sie zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="74464-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="74464-138">Eine Ratensenke kann manuell oder durch Aufrufen von [HrAllocAdviseSink erstellt werden.](hrallocadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="74464-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="74464-139">Die **HrAllocAdviseSink-Funktion** ermöglicht es dem Aufrufer, eine Rückruffunktion anzugeben, die **Aufrufe** als Teil der Benachrichtigung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="74464-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="74464-140">Die Rückruffunktion entspricht dem [NOTIFCALLBACK-Prototyp.](notifcallback.md)</span><span class="sxs-lookup"><span data-stu-id="74464-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="74464-141">Von Clients implementierte Rückruffunktionen geben immer S_OK; Rückruffunktionen, die von Dienstanbietern implementiert werden, können CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="74464-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="74464-142">Wenn eine Rückruffunktion CALLBACK_DISCONTINUE, beendet MAPI das Senden von Benachrichtigungen und gibt NOTIFY_CANCELED _LpulFlags-Parameter_ der **Notify-Methode** zurück.</span><span class="sxs-lookup"><span data-stu-id="74464-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="74464-143">Sie können davon ausgehen, dass der Prozess inaktiv ist, und die Generierung von Benachrichtigungen für diesen Prozess beenden.</span><span class="sxs-lookup"><span data-stu-id="74464-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="74464-144">Wenn **Notify** 0 in  _lpulFlags_ zurückgibt, ist der Prozess weiterhin aktiv, und Sie sollten weiterhin Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="74464-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="74464-145">Wenn Sie synchrone Benachrichtigungen verwenden, achten Sie darauf, Deadlocksituationen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="74464-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="74464-146">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="74464-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74464-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74464-147">See also</span></span>

- [<span data-ttu-id="74464-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="74464-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="74464-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="74464-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="74464-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="74464-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="74464-151">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="74464-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="74464-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="74464-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="74464-153">PidTagRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="74464-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="74464-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="74464-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

