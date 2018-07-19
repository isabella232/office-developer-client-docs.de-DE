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
ms.openlocfilehash: db23d1801bf32fd947a77dfd887c56f75ded5681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792388"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="deb1a-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="deb1a-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="deb1a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="deb1a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="deb1a-105">Sendet eine Benachrichtigung über ein bestimmtes Ereignis mit einer Advise-Datenquelle, die ursprünglich für die Benachrichtigung über die [IMAPISupport::Subscribe](imapisupport-subscribe.md) -Methode registriert.</span><span class="sxs-lookup"><span data-stu-id="deb1a-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="deb1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="deb1a-106">Parameters</span></span>

<span data-ttu-id="deb1a-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="deb1a-107">_lpKey_</span></span>
  
> <span data-ttu-id="deb1a-108">[in] Ein Zeiger auf die Benachrichtigung Schlüssel für das Quellobjekt Advise.</span><span class="sxs-lookup"><span data-stu-id="deb1a-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="deb1a-109">Der Parameter _LpKey_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="deb1a-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="deb1a-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="deb1a-110">_cNotification_</span></span>
  
> <span data-ttu-id="deb1a-111">[in] Die Anzahl der Benachrichtigung Strukturen auf den durch den Parameter _LpNotifications_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="deb1a-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="deb1a-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="deb1a-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="deb1a-113">[in] Ein Zeiger auf ein Array von [Benachrichtigung](notification.md) Strukturen, die ausstehende Benachrichtigungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="deb1a-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="deb1a-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="deb1a-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="deb1a-115">[in, out] Eine Bitmaske aus Flags, die den Benachrichtigungsprozess steuert.</span><span class="sxs-lookup"><span data-stu-id="deb1a-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="deb1a-116">Bei der Eingabe kann das folgende Flag festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="deb1a-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="deb1a-117">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="deb1a-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="deb1a-118">Die Zeichenfolgen in der Benachrichtigung Strukturen auf den _LpNotifications_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="deb1a-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="deb1a-119">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="deb1a-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="deb1a-120">Bei der Ausgabe kann MAPI das folgende Flag festlegen:</span><span class="sxs-lookup"><span data-stu-id="deb1a-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="deb1a-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="deb1a-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="deb1a-122">Eine Rückruffunktion abgebrochen eine synchrone Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="deb1a-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="deb1a-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deb1a-123">Return value</span></span>

<span data-ttu-id="deb1a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="deb1a-124">S_OK</span></span> 
  
> <span data-ttu-id="deb1a-125">Die Benachrichtigungen wurden erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="deb1a-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="deb1a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="deb1a-126">Remarks</span></span>

<span data-ttu-id="deb1a-127">Die **IMAPISupport::Notify** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="deb1a-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="deb1a-128">Dienstanbieter anrufen **Benachrichtigen** , um anzufordern, dass MAPI generieren eine Benachrichtigung für eine Advise-Empfänger, die für die Benachrichtigung über die **IMAPISupport::Subscribe** -Methode zuvor registriert hat.</span><span class="sxs-lookup"><span data-stu-id="deb1a-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="deb1a-129">**Benachrichtigen** Kopien die Strukturen durch den Parameter _LpNotifications_ auf das in den Speicher und die entsprechenden Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="deb1a-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="deb1a-130">Wenn mit der Benachrichtigung **OnNotify** abgeschlossen ist, wird den Beteiligten Speicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="deb1a-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="deb1a-131">Der Aufrufer muss nicht Speicher zugewiesen werden. MAPI führt alle erforderlichen arbeitsspeicherreservierung.</span><span class="sxs-lookup"><span data-stu-id="deb1a-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="deb1a-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="deb1a-132">Notes to callers</span></span>

<span data-ttu-id="deb1a-133">Die Benachrichtigung-Taste im _LpKey_ -Parameter übergeben müssen Sie zum Schlüssel _LpKey_ an die **IMAPISupport::Subscribe** -Methode übergebenen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="deb1a-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="deb1a-134">Viele Anbieter für die Eintrags-ID der Advise-Quelle als Schlüssel verwenden, aber andere Daten enthält, wie ein Dateipfad verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="deb1a-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="deb1a-135">MAPI verwendet diesen Schlüssel, um alle Registrierungen für Benachrichtigungen für die identifizierten Advise-Quelle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="deb1a-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="deb1a-136">Stellen Sie sicher, dass Sie das **LpEntryID** Mitglied der Benachrichtigungsstruktur auf langfristige Eintrags-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="deb1a-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="deb1a-137">Wenn Sie festlegen, rufen Sie das NOTIFY_SYNC-Flag auf die **Subscribe** für eines der ausstehenden Benachrichtigungen, **Benachrichtigen** Anrufe Rückruffunktionen **IMAPIAdviseSink::OnNotify** -Methode vor der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="deb1a-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="deb1a-138">Advise-Empfänger kann manuell oder durch Aufrufen von [HrAllocAdviseSink](hrallocadvisesink.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="deb1a-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="deb1a-139">Die Funktion **HrAllocAdviseSink** ermöglicht dessen Aufrufer einer Callback-Funktion als Teil der Benachrichtigung, **Notify** -Aufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="deb1a-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="deb1a-140">Die Callback-Funktion entspricht der [NOTIFCALLBACK](notifcallback.md) Prototyp.</span><span class="sxs-lookup"><span data-stu-id="deb1a-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="deb1a-141">Rückruffunktionen immer durch Clients implementiert geben S_OK zurück. Implementierung von Dienstanbietern Rückruffunktionen können CALLBACK_DISCONTINUE zurück.</span><span class="sxs-lookup"><span data-stu-id="deb1a-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="deb1a-142">Wenn eine Rückruffunktion CALLBACK_DISCONTINUE zurückgibt, MAPI beendet Senden von Benachrichtigungen und NOTIFY_CANCELED in _LpulFlags_ -Parameter die **Notify** -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="deb1a-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="deb1a-143">Sie können davon ausgehen, dass der Prozess inaktiv und Generieren von Benachrichtigungen für diesen Prozess beenden ist.</span><span class="sxs-lookup"><span data-stu-id="deb1a-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="deb1a-144">Wenn **Benachrichtigen** in _LpulFlags_gibt 0 zurück, der Prozess noch aktiv ist, und Sie sollten weiterhin zum Senden von Benachrichtigungen, nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="deb1a-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="deb1a-145">Wenn Sie synchrone Benachrichtigungen verwenden, sollten Sie darauf achten Sie, Deadlocks zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="deb1a-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="deb1a-146">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="deb1a-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="deb1a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="deb1a-147">See also</span></span>

- [<span data-ttu-id="deb1a-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="deb1a-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="deb1a-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="deb1a-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="deb1a-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="deb1a-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="deb1a-151">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="deb1a-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="deb1a-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="deb1a-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="deb1a-153">PidTagRecordKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="deb1a-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="deb1a-154">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="deb1a-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

