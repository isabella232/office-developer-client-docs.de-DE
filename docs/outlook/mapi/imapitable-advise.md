---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418813"
---
# <a name="imapitableadvise"></a><span data-ttu-id="ca4a1-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="ca4a1-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="ca4a1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca4a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca4a1-105">Registriert ein Advise Sink-Objekt, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle ausdingen.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ca4a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca4a1-106">Parameters</span></span>

 <span data-ttu-id="ca4a1-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="ca4a1-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="ca4a1-108">[in] Wert, der den Typ des Ereignisses angibt, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="ca4a1-109">Nur der folgende Wert ist gültig:</span><span class="sxs-lookup"><span data-stu-id="ca4a1-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="ca4a1-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="ca4a1-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="ca4a1-111">[in] Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="ca4a1-112">Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="ca4a1-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="ca4a1-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="ca4a1-114">[out] Zeiger auf einen Wert ungleich Null, der die erfolgreiche Benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca4a1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca4a1-115">Return value</span></span>

<span data-ttu-id="ca4a1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca4a1-116">S_OK</span></span> 
  
> <span data-ttu-id="ca4a1-117">Die Benachrichtigungsregistrierung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="ca4a1-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ca4a1-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ca4a1-119">Die Tabellenimplementierung unterstützt entweder keine Änderungen an den Zeilen und Spalten oder keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca4a1-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca4a1-120">Remarks</span></span>

<span data-ttu-id="ca4a1-121">Verwenden Sie die **IMAPITable::Advise-Methode,** um ein im Anbieter implementiertes Tabellenobjekt für Benachrichtigungsrückrufe zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="ca4a1-122">Wenn eine Änderung am Tabellenobjekt auftritt, überprüft der Anbieter, welches Ereignismaskenbit im  _ulEventMask-Parameter_ festgelegt wurde und welche Art von Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="ca4a1-123">Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) auf, damit das durch den  _lpAdviseSink-Parameter_ angegebene Advise-Sink-Objekt das Ereignis melden kann.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="ca4a1-124">Daten, die in der Benachrichtigungsstruktur an die **OnNotify-Routine** übergeben werden, beschreiben das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="ca4a1-125">Der Aufruf von **OnNotify** kann während des Aufrufs erfolgen, der das Objekt ändert, oder zu einem beliebigen nachfolgenden Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="ca4a1-126">Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="ca4a1-127">Um einen Aufruf von **OnNotify,** der zu einem unvorstellbaren Zeitpunkt auftreten kann, in einen anruf zu verwandeln, der sicherer zu behandeln ist, sollte ein Anbieter die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="ca4a1-128">Zum Bereitstellen von Benachrichtigungen muss der Anbieter, der **Advise** implementieren, eine Kopie des Zeigers auf das  _lpAdviseSink-Ratgebersenkenobjekt_ behalten. Dazu ruft sie die **IUnknown::AddRef-Methode** auf, damit die Ratensenke ihren Objektzeiger beibehalten kann, bis die Benachrichtigungsregistrierung mit einem Aufruf der [IMAPITable::Unadvise-Methode](imapitable-unadvise.md) abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="ca4a1-129">Die **Advise-Implementierung** sollte der Benachrichtigungsregistrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor sie im  _lpulConnection-Parameter zurückgesenkt_ wird.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="ca4a1-130">Dienstanbieter können das Advise -Sink-Objekt vor dem Abbrechen der Registrierung los, aber sie dürfen die Verbindungsnummer erst los, wenn \*\* Unadvise \*\* aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="ca4a1-131">Nachdem ein Aufruf von **Advise** erfolgreich war und bevor \*\* Unadvise \*\* aufgerufen wurde, müssen Clients darauf vorbereitet sein, dass das Advise Sink-Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="ca4a1-132">Ein Client sollte daher sein Advise -Sink-Objekt veröffentlichen, nachdem **Advise** zurückgegeben wird, es sei denn, er hat eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="ca4a1-133">Aufgrund des asynchronen Verhaltens von Benachrichtigungen können Implementierungen, die Tabellenspalteneinstellungen ändern, Benachrichtigungen mit Informationen empfangen, die in einer vorherigen Spaltenreihenfolge organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="ca4a1-134">Beispielsweise kann eine Tabellenzeile für eine Nachricht zurückgegeben werden, die gerade aus dem Container gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="ca4a1-135">Eine solche Benachrichtigung wird gesendet, wenn die Änderung der Spalteneinstellung vorgenommen wurde und Informationen darüber gesendet wurden, die Benachrichtigungstabelle jedoch noch nicht mit diesen Informationen aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="ca4a1-136">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ca4a1-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ca4a1-137">Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellenbenachrichtigungen](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ca4a1-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="ca4a1-138">Informationen zur Verwendung der **IMAPISupport-Methoden** zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ca4a1-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ca4a1-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ca4a1-139">MFCMAPI reference</span></span>

<span data-ttu-id="ca4a1-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ca4a1-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ca4a1-141">**File**</span></span>|<span data-ttu-id="ca4a1-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ca4a1-142">**Function**</span></span>|<span data-ttu-id="ca4a1-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ca4a1-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca4a1-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ca4a1-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ca4a1-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="ca4a1-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="ca4a1-146">MFCMAPI verwendet die **IMAPITable::Advise-Methode,** um sich für Benachrichtigungen zu registrieren, damit die Tabellenansicht auf dem aktuellen Stand bleibt.</span><span class="sxs-lookup"><span data-stu-id="ca4a1-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca4a1-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca4a1-147">See also</span></span>



[<span data-ttu-id="ca4a1-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ca4a1-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="ca4a1-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ca4a1-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ca4a1-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ca4a1-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="ca4a1-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ca4a1-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="ca4a1-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca4a1-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ca4a1-153">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ca4a1-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

