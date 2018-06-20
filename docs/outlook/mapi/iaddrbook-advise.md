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
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791997"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="bfd4b-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="bfd4b-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="bfd4b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfd4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfd4b-105">Registriert einen Client oder Dienstanbieter Erhalt von Benachrichtigungen zu Änderungen an einen oder mehrere Einträge im Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bfd4b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfd4b-106">Parameters</span></span>

 <span data-ttu-id="bfd4b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bfd4b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="bfd4b-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bfd4b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bfd4b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="bfd4b-110">[in] Ein Zeiger auf die Eintrags-ID der Adressbuchcontainer messaging-Benutzer oder eine Verteilerliste, die eine Benachrichtigung generiert wird, bei einer Änderung des Typs oder Typen, die im Parameter _UlEventMask_ beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="bfd4b-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="bfd4b-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="bfd4b-112">[in] Eine oder mehrere Benachrichtigungsereignisse, die der Anrufer Empfang registriert wird.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="bfd4b-113">Jedes Ereignis ist eine bestimmte Benachrichtigung-Struktur, die Informationen zum Ändern der aufgetretenen enthält zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="bfd4b-114">Die folgende Tabelle enthält die gültigen Werte für _UlEventMask_ und ihre entsprechenden Strukturen.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="bfd4b-115">**Benachrichtigungsereignis**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-115">**Notification event**</span></span>|<span data-ttu-id="bfd4b-116">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfd4b-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="bfd4b-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="bfd4b-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="bfd4b-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="bfd4b-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="bfd4b-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="bfd4b-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="bfd4b-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="bfd4b-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="bfd4b-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="bfd4b-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="bfd4b-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="bfd4b-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="bfd4b-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="bfd4b-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfd4b-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="bfd4b-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="bfd4b-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="bfd4b-132">[in] Ein Zeiger auf das Empfängerobjekt Advise aufgerufen werden, tritt das Ereignis für das Benachrichtigung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="bfd4b-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="bfd4b-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="bfd4b-134">[out] Ein Zeiger auf eine Verbindung ungleich NULL-Zahl, die benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bfd4b-135">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bfd4b-135">Return value</span></span>

<span data-ttu-id="bfd4b-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfd4b-136">S_OK</span></span> 
  
> <span data-ttu-id="bfd4b-137">Die benachrichtigungsregistrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="bfd4b-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bfd4b-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="bfd4b-139">Verantwortlich für die Eintrags-ID _LpEntryID_ übergebenen Adressbuchanbieter konnte eine Benachrichtigung für den entsprechenden Eintrag nicht registriert werden.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="bfd4b-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bfd4b-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bfd4b-141">Benachrichtigung wird von Adressbuchanbieter verantwortlich für das durch die Eintrags-ID in der _LpEntryID_ -Parameter übergebene Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="bfd4b-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bfd4b-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="bfd4b-143">Die Eintrags-ID _LpEntryID_ übergebenen kann von jedem der adressbuchanbietern implementierte im Profil behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bfd4b-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfd4b-144">Remarks</span></span>

<span data-ttu-id="bfd4b-145">Clients und Dienstanbieter Aufrufen die **Advise** -Methode für einen bestimmten Typ oder Typen der Benachrichtigung auf ein Adressbuch Adresseintrag registriert.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="bfd4b-146">Die Typen der Benachrichtigung werden durch die mit der _UlEventMask_ -Parameter übergebene Ereignismaske angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="bfd4b-147">MAPI leitet diese **Advise** -Anruf an die Adressbuchanbieter, die verantwortlich für den Eintrag wie die Eintrags-ID in der _LpEntryID_ -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="bfd4b-148">Der Adressbuchanbieter behandelt die Registrierung selbst, oder ruft die Support-Methode, [IMAPISupport::Subscribe](imapisupport-subscribe.md), MAPI, um den Anrufer registrieren aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="bfd4b-149">Eine Zahl ungleich NULL Verbindung wird zurückgegeben, um die erfolgreiche Registrierung darzustellen.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="bfd4b-150">Wenn eine Änderung an den Eintrag vom Typ angegeben durch die benachrichtigungsregistrierung auftritt, ruft der Adressbuchanbieter die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für der Advise-Empfängerobjekt im _LpAdviseSink_ -Parameter angegebene.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="bfd4b-151">Die **OnNotify** -Methode enthält eine [Benachrichtigung](notification.md) Struktur als Eingabeparameter, der Daten zur Beschreibung des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="bfd4b-152">Je nach der Adressbuchanbieter kann der Anruf an **OnNotify** unmittelbar nach der Änderung an das registrierte Objekt oder zu einem späteren Zeitpunkt auftreten.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="bfd4b-153">Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auf einem beliebigen Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="bfd4b-154">Clients können anfordern, dass diese Benachrichtigungen erfolgen für einen bestimmten Thread durch Aufrufen der [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion, um das Empfängerobjekt Advise erstellen, das an **Advise**übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="bfd4b-155">Da ein Adressbuchanbieter der Advise-Empfängerobjekt kann jederzeit nach der erfolgreiche Abschluss der **Advise** aufrufen und aufrufen, bevor eine [IAddrBook::Unadvise](iaddrbook-unadvise.md) die Benachrichtigung Abbrechen von Clients übergebenen freigeben kann, sollte Clients freigeben. Ihre Advise Empfängerobjekten, wenn **Advise** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bfd4b-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="bfd4b-156">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="bfd4b-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bfd4b-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfd4b-157">See also</span></span>



[<span data-ttu-id="bfd4b-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="bfd4b-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="bfd4b-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="bfd4b-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="bfd4b-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bfd4b-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bfd4b-161">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="bfd4b-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="bfd4b-162">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bfd4b-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

