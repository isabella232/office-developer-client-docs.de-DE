---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334755"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="9efc7-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="9efc7-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="9efc7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9efc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9efc7-105">Registriert einen Client oder Dienstanbieter für den Empfang von Benachrichtigungen zu Änderungen an einem oder mehreren Einträgen im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="9efc7-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="9efc7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9efc7-106">Parameters</span></span>

 <span data-ttu-id="9efc7-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9efc7-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="9efc7-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9efc7-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9efc7-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9efc7-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="9efc7-110">in Ein Zeiger auf die Eintrags-ID des Adressbuch Containers, des Messaging Benutzers oder der Verteilerliste, der eine Benachrichtigung generiert, wenn eine Änderung der im _ulEventMask_ -Parameter beschriebenen Typen auftritt.</span><span class="sxs-lookup"><span data-stu-id="9efc7-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="9efc7-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="9efc7-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="9efc7-112">in Ein oder mehrere Benachrichtigungsereignisse, die der Anrufer für den Empfang registriert.</span><span class="sxs-lookup"><span data-stu-id="9efc7-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="9efc7-113">Jedes Ereignis ist einer bestimmten Benachrichtigungsstruktur zugeordnet, die Informationen zu der eingetretenen Änderung enthält.</span><span class="sxs-lookup"><span data-stu-id="9efc7-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="9efc7-114">In der folgenden Tabelle sind die gültigen Werte für _ulEventMask_ und die entsprechenden Strukturen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9efc7-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="9efc7-115">**Benachrichtigungsereignis**</span><span class="sxs-lookup"><span data-stu-id="9efc7-115">**Notification event**</span></span>|<span data-ttu-id="9efc7-116">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="9efc7-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9efc7-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="9efc7-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="9efc7-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="9efc7-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="9efc7-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="9efc7-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9efc7-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="9efc7-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="9efc7-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9efc7-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="9efc7-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="9efc7-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9efc7-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="9efc7-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="9efc7-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9efc7-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="9efc7-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="9efc7-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="9efc7-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="9efc7-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="9efc7-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9efc7-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="9efc7-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="9efc7-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="9efc7-132">in Ein Zeiger auf das Advise-Senke-Objekt, das aufgerufen werden soll, wenn das Ereignis, für das die Benachrichtigung angefordert wurde, auftritt.</span><span class="sxs-lookup"><span data-stu-id="9efc7-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="9efc7-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="9efc7-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="9efc7-134">Out Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Benachrichtigungs Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9efc7-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9efc7-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9efc7-135">Return value</span></span>

<span data-ttu-id="9efc7-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="9efc7-136">S_OK</span></span> 
  
> <span data-ttu-id="9efc7-137">Die Benachrichtigungs Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9efc7-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="9efc7-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9efc7-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="9efc7-139">Der Adressbuchanbieter, der für die in _lpEntryID_ übergebene Eintrags-ID zuständig ist, konnte keine Benachrichtigung für den entsprechenden Eintrag registrieren.</span><span class="sxs-lookup"><span data-stu-id="9efc7-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="9efc7-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9efc7-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9efc7-141">Die Benachrichtigung wird nicht vom Adressbuchanbieter unterstützt, der für das durch den _lpEntryID_ -Parameter übergebene Eintragsbezeichner verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="9efc7-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="9efc7-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9efc7-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="9efc7-143">Die in _lpEntryID_ übergebene Eintrags-ID kann von keinem der Adressbuchanbieter im Profil verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9efc7-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9efc7-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9efc7-144">Remarks</span></span>

<span data-ttu-id="9efc7-145">Clients und Dienstanbieter rufen die **Advise** -Methode auf, um für einen bestimmten Typ oder eine Art von Benachrichtigung für einen Adressbucheintrag zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="9efc7-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="9efc7-146">Die Benachrichtigungstypen werden durch die Ereignismaske angezeigt, die mit dem _ulEventMask_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9efc7-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="9efc7-147">MAPI leitet diesen **Advise** -Aufruf an den Adressbuchanbieter weiter, der für den Eintrag verantwortlich ist, wie durch die Eintrags-ID im _lpEntryID_ -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="9efc7-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="9efc7-148">Der Adressbuchanbieter behandelt die Registrierung selbst oder ruft die Support Methode [IMAPISupport:: subscribe](imapisupport-subscribe.md)auf, um MAPI zur Registrierung des Anrufers aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="9efc7-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="9efc7-149">Eine Verbindungsnummer, die ungleich NULL ist, wird zurückgegeben, um die erfolgreiche Registrierung darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9efc7-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="9efc7-150">Bei jeder Änderung des Eintrags des Typs, der durch die Benachrichtigungs Registrierung angegeben wird, ruft der Adressbuchanbieter die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das Advise-Senke-Objekt auf, das im _lpAdviseSink_ -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9efc7-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="9efc7-151">Die **OnNotify** -Methode enthält [](notification.md) eine Benachrichtigungsstruktur als Eingabeparameter, der Daten zum Beschreiben des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="9efc7-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="9efc7-152">Je nach Adressbuchanbieter kann der Aufruf von onNotify \*\*\*\* unmittelbar nach der Änderung des registrierten Objekts oder zu einem späteren Zeitpunkt erfolgen.</span><span class="sxs-lookup"><span data-stu-id="9efc7-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="9efc7-153">Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann \*\*\*\* der Aufruf von OnNotify in jedem Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="9efc7-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="9efc7-154">Clients können diese Benachrichtigungen für einen bestimmten Thread anfordern, indem Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion zum Erstellen des Advise-Senke-Objekts aufrufen, das an **Advise**übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9efc7-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="9efc7-155">Da ein Adressbuchanbieter das Advise-Senke-Objekt, das von Clients übergeben wird, jederzeit freigeben kann, nachdem der **Advise** -Aufruf erfolgreich abgeschlossen wurde, und bevor ein [IAddrBook:: Unadvise](iaddrbook-unadvise.md) -Aufruf zum Abbrechen der Benachrichtigung ausgeführt wird, sollten Clients die Freigabe Ihre Advise-Senke-Objekte, wenn **Advise** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9efc7-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="9efc7-156">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="9efc7-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9efc7-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9efc7-157">See also</span></span>



[<span data-ttu-id="9efc7-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9efc7-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="9efc7-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="9efc7-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="9efc7-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="9efc7-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="9efc7-161">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="9efc7-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="9efc7-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9efc7-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

