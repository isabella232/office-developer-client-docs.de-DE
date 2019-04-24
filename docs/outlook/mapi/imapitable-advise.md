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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329018"
---
# <a name="imapitableadvise"></a><span data-ttu-id="71836-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="71836-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="71836-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71836-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71836-105">Registriert ein Advise-Senke-Objekt, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Tabelle auswirken.</span><span class="sxs-lookup"><span data-stu-id="71836-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="71836-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71836-106">Parameters</span></span>

 <span data-ttu-id="71836-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="71836-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="71836-108">in Wert, der den Typ des Ereignisses angibt, das die Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="71836-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="71836-109">Nur der folgende Wert ist gültig:</span><span class="sxs-lookup"><span data-stu-id="71836-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="71836-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="71836-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="71836-111">in Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="71836-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="71836-112">Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.</span><span class="sxs-lookup"><span data-stu-id="71836-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="71836-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="71836-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="71836-114">Out Zeiger auf einen Wert ungleich NULL, der die erfolgreiche Benachrichtigungs Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="71836-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="71836-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71836-115">Return value</span></span>

<span data-ttu-id="71836-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="71836-116">S_OK</span></span> 
  
> <span data-ttu-id="71836-117">Die Benachrichtigungs Registrierung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="71836-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="71836-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="71836-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="71836-119">Die Tabellen Implementierung unterstützt keine Änderungen an den Zeilen und Spalten oder unterstützt keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="71836-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="71836-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71836-120">Remarks</span></span>

<span data-ttu-id="71836-121">Verwenden Sie die **IMAPITable:: Advise** -Methode, um ein Table-Objekt zu registrieren, das im Anbieter für Benachrichtigungsrückrufe implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="71836-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="71836-122">Wenn eine Änderung für das Table-Objekt auftritt, überprüft der Anbieter, welches Ereignis Masken Bit im Parameter _ulEventMask_ festgelegt wurde und welche Art von Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="71836-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="71836-123">Wenn ein Bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das vom _lpAdviseSink_ -Parameter angegebene Advise-Senke-Objekt auf, um das Ereignis zu melden.</span><span class="sxs-lookup"><span data-stu-id="71836-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="71836-124">Die Daten, die in der Benachrichtigungs \*\*\*\* Struktur an die OnNotify-Routine übergeben werden, beschreiben das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="71836-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="71836-125">Der Aufruf von **OnNotify** kann während des Anrufs auftreten, der das Objekt ändert oder zu einem beliebigen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="71836-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="71836-126">Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann \*\*\*\* der Aufruf von OnNotify in jedem Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="71836-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="71836-127">Damit ein Anruf an onNotify, der \*\*\*\* möglicherweise zu einem ungünstigen Zeitpunkt stattfindet, zu einem sicherer wird, der zu handhaben ist, sollte ein Anbieter die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="71836-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="71836-128">Um Benachrichtigungen bereitzustellen, muss der Anbieter, der **Advise** implementiert, eine Kopie des Zeigers auf das _lpAdviseSink_ -Advise-Objekt beibehalten; Hierzu wird die **IUnknown:: AddRef** -Methode für die Advise-Senke aufgerufen, um den Objektzeiger zu warten, bis die Benachrichtigungs Registrierung mit einem Aufruf der [IMAPITable:: Unadvise](imapitable-unadvise.md) -Methode abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="71836-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="71836-129">Die **Advise** -Implementierung sollte der Benachrichtigungs Registrierung eine Verbindungsnummer zuweisen und **AddRef** für diese Verbindungsnummer aufrufen, bevor Sie im _lpulConnection_ -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="71836-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="71836-130">Dienstanbieter können das Advise-Senke-Objekt freigeben, bevor die Registrierung abgebrochen wird, aber Sie dürfen die Verbindungsnummer erst freigeben, wenn \* \* Unadvise \* \* aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="71836-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="71836-131">Nachdem ein Anruf bei **Advise** erfolgreich war und bevor \* \* Unadvise \* \* aufgerufen wurde, müssen Clients für das Advise-Senke-Objekt freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71836-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="71836-132">Ein Client sollte daher sein Advise-Senke-Objekt freigeben, nachdem **Advise** zurückgegeben wird, es sei denn, er hat eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="71836-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="71836-133">Aufgrund des asynchronen Verhaltens der Benachrichtigung können Implementierungen, die Tabellenspalten Einstellungen ändern, Benachrichtigungen mit Informationen erhalten, die in einer vorherigen Spaltenreihenfolge organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="71836-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="71836-134">Beispielsweise kann eine Tabellenzeile für eine Nachricht zurückgegeben werden, die soeben aus dem Container gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="71836-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="71836-135">Eine solche Benachrichtigung wird gesendet, wenn die Spalten Einstellung geändert wurde und Informationen über Sie gesendet wurden, aber die Benachrichtigungstabellen Ansicht noch nicht mit diesen Informationen aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="71836-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="71836-136">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="71836-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="71836-137">Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellen Benachrichtigungen](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="71836-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="71836-138">Informationen zur Verwendung der **IMAPISupport** -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="71836-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="71836-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="71836-139">MFCMAPI reference</span></span>

<span data-ttu-id="71836-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="71836-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="71836-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="71836-141">**File**</span></span>|<span data-ttu-id="71836-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="71836-142">**Function**</span></span>|<span data-ttu-id="71836-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="71836-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="71836-144">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="71836-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="71836-145">CContestTableListCtrl:: NotificationOn</span><span class="sxs-lookup"><span data-stu-id="71836-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="71836-146">MFCMAPI verwendet die **IMAPITable:: Advise** -Methode, um Benachrichtigungen zu registrieren, damit die Tabellenansicht aktuell bleibt.</span><span class="sxs-lookup"><span data-stu-id="71836-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71836-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71836-147">See also</span></span>



[<span data-ttu-id="71836-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="71836-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="71836-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="71836-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="71836-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="71836-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="71836-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71836-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="71836-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71836-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="71836-153">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="71836-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

