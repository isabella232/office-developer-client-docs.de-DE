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
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594243"
---
# <a name="imapitableadvise"></a><span data-ttu-id="6684c-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="6684c-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="6684c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6684c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6684c-105">Registriert ein Empfängerobjekt Advise, um die Benachrichtigung der Auswirkungen auf die Tabelle angegebenen Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6684c-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6684c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6684c-106">Parameters</span></span>

 <span data-ttu-id="6684c-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="6684c-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="6684c-108">[in] Wert, der den Typ des Ereignisses, das die Benachrichtigung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="6684c-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="6684c-109">Nur der folgende Wert ist gültig:</span><span class="sxs-lookup"><span data-stu-id="6684c-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="6684c-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="6684c-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="6684c-111">[in] Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="6684c-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="6684c-112">Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="6684c-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="6684c-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="6684c-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="6684c-114">[out] Zeiger auf einen Wert ungleich NULL, der die erfolgreiche benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6684c-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6684c-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6684c-115">Return value</span></span>

<span data-ttu-id="6684c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6684c-116">S_OK</span></span> 
  
> <span data-ttu-id="6684c-117">Die benachrichtigungsregistrierung erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6684c-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="6684c-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6684c-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6684c-119">Die Tabelle-Implementierung unterstützt keine Änderungen auf die Zeilen und Spalten, oder unterstützt keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="6684c-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6684c-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6684c-120">Remarks</span></span>

<span data-ttu-id="6684c-121">Verwenden Sie die **IMAPITable::Advise** -Methode, um ein Table-Objekt im Anbieter für Benachrichtigung Rückrufe implementiert registrieren.</span><span class="sxs-lookup"><span data-stu-id="6684c-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="6684c-122">Bei eine Änderung an das Table-Objekt, überprüft der Anbieter finden Sie unter welche Ereignis Maskenbit im _UlEventMask_ -Parameter festgelegt wurde, und daher, welche Art der Änderung.</span><span class="sxs-lookup"><span data-stu-id="6684c-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="6684c-123">Wenn ein bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Empfängerobjekt durch den Parameter _LpAdviseSink_ Sie das Ereignis melden angegeben.</span><span class="sxs-lookup"><span data-stu-id="6684c-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="6684c-124">Daten, die in der Benachrichtigungsstruktur der **OnNotify** Routine übergeben wird das Ereignis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6684c-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="6684c-125">Der Aufruf von **OnNotify** kann auftreten, während des Anrufs, der das Objekt ändert oder folgenden jederzeit.</span><span class="sxs-lookup"><span data-stu-id="6684c-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="6684c-126">Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auf einem beliebigen Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="6684c-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="6684c-127">Für eine Möglichkeit, einen Anruf an **OnNotify** aktivieren, die zu einem ungünstigen Zeitpunkt in eine auftreten können, die zum Verarbeiten von sicherer ist, sollte ein Anbieter für die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6684c-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="6684c-128">Um Benachrichtigungen zu ermöglichen, beraten die Anbieter implementieren **Advise** muss eine Kopie des Zeigers auf die _LpAdviseSink_ Empfängerobjekt; Hierzu wird die **IUnknown:: AddRef** -Methode für die Advise-Empfänger, dessen Objektzeiger verwalten, bis benachrichtigungsregistrierung mit einem Aufruf der Methode [IMAPITable::Unadvise](imapitable-unadvise.md) abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="6684c-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="6684c-129">Die **Advise** -Implementierung sollte weisen eine Verbindungsnummer zu der benachrichtigungsregistrierung und rufen **AddRef** für diese Verbindungsnummer vor der Rückgabe im _LpulConnection_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6684c-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="6684c-130">Dienstanbieter können das Empfängerobjekt Advise freigeben, bevor die Registrierung wird abgebrochen, aber sie nicht, bis die Nummer freigeben müssen ** Unadvise ** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6684c-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until ** Unadvise ** has been called.</span></span> 
  
<span data-ttu-id="6684c-131">Nach ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor ** Unadvise ** wurde aufgerufen, Clients müssen bereiten Sie für das Empfängerobjekt Advise freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="6684c-131">After a call to **Advise** has succeeded and before ** Unadvise ** has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="6684c-132">Ein Client sollte daher seine Advise-Empfängerobjekt freigeben, nachdem **Advise** zurückgegeben, wenn es eine bestimmte langfristige Verwendung verfügt.</span><span class="sxs-lookup"><span data-stu-id="6684c-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="6684c-133">Aufgrund der asynchronen Verhalten der Benachrichtigung erhalten Implementierungen integrieren, die Tabelle spalteneinstellungen ändern Benachrichtigungen mit Informationen in einer vorherigen Spaltenreihenfolge angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6684c-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="6684c-134">Beispielsweise könnte eine Tabellenzeile für eine Nachricht zurückgegeben werden, die nur aus dem Container gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="6684c-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="6684c-135">Wenn die Änderung der Einstellung wurde, und Informationen gesendet, aber die Benachrichtigung Tabellenansicht mit diesen Informationen noch nicht aktualisiert wurde, wird eine solche Benachrichtigung gesendet.</span><span class="sxs-lookup"><span data-stu-id="6684c-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="6684c-136">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6684c-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="6684c-137">Spezifische Informationen zur Tabelle Benachrichtigung finden Sie unter [Zur Tabelle Benachrichtigungen](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6684c-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="6684c-138">Informationen zur Verwendung der Methods **IMAPISupport** zum Benachrichtigung zu unterstützen finden Sie unter [Event Notification unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="6684c-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6684c-139">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6684c-139">MFCMAPI reference</span></span>

<span data-ttu-id="6684c-140">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6684c-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6684c-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6684c-141">**File**</span></span>|<span data-ttu-id="6684c-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6684c-142">**Function**</span></span>|<span data-ttu-id="6684c-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6684c-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6684c-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="6684c-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="6684c-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="6684c-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="6684c-146">MFCMAPI (engl.) verwendet die **IMAPITable::Advise** -Methode, um für Benachrichtigungen der Tabellenansicht auf dem neuesten Stand zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="6684c-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6684c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6684c-147">See also</span></span>



[<span data-ttu-id="6684c-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6684c-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="6684c-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6684c-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6684c-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6684c-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="6684c-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6684c-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="6684c-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6684c-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="6684c-153">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6684c-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

