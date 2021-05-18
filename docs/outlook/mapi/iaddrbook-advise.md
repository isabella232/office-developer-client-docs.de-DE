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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406276"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="d5d54-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="d5d54-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="d5d54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5d54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5d54-105">Registriert einen Client oder Dienstanbieter, um Benachrichtigungen über Änderungen an einem oder mehreren Einträgen im Adressbuch zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5d54-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d5d54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5d54-106">Parameters</span></span>

 <span data-ttu-id="d5d54-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d5d54-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d5d54-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="d5d54-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d5d54-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d5d54-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d5d54-110">[in] Ein Zeiger auf die Eintrags-ID des Adressbuchcontainers, des Messagingbenutzers oder der Verteilerliste, der eine Benachrichtigung generiert, wenn eine Änderung des im  _ulEventMask-Parameter_ beschriebenen Typs oder Typs erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d5d54-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="d5d54-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="d5d54-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="d5d54-112">[in] Mindestens ein Benachrichtigungsereignisse, das der Anrufer für den Empfang registriert.</span><span class="sxs-lookup"><span data-stu-id="d5d54-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="d5d54-113">Jedes Ereignis ist einer bestimmten Benachrichtigungsstruktur zugeordnet, die Informationen zur aufgetretenen Änderung enthält.</span><span class="sxs-lookup"><span data-stu-id="d5d54-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="d5d54-114">In der folgenden Tabelle sind die gültigen Werte für  _ulEventMask und_ deren entsprechende Strukturen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5d54-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="d5d54-115">**Benachrichtigungsereignis**</span><span class="sxs-lookup"><span data-stu-id="d5d54-115">**Notification event**</span></span>|<span data-ttu-id="d5d54-116">**Entsprechende Struktur**</span><span class="sxs-lookup"><span data-stu-id="d5d54-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5d54-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="d5d54-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="d5d54-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="d5d54-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="d5d54-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="d5d54-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d5d54-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="d5d54-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="d5d54-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d5d54-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="d5d54-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="d5d54-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d5d54-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="d5d54-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="d5d54-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d5d54-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="d5d54-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="d5d54-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="d5d54-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="d5d54-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="d5d54-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5d54-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="d5d54-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="d5d54-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="d5d54-132">[in] Ein Zeiger auf das objekt advise sink, das aufgerufen werden soll, wenn das Ereignis auftritt, für das eine Benachrichtigung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5d54-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="d5d54-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="d5d54-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="d5d54-134">[out] Ein Zeiger auf eine Verbindungsnummer ungleich Null, die die Benachrichtigungsregistrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="d5d54-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5d54-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5d54-135">Return value</span></span>

<span data-ttu-id="d5d54-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5d54-136">S_OK</span></span> 
  
> <span data-ttu-id="d5d54-137">Die Benachrichtigungsregistrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d5d54-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="d5d54-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d5d54-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="d5d54-139">Der Adressbuchanbieter, der für die in  _lpEntryID_ übergebene Eintrags-ID verantwortlich ist, konnte keine Benachrichtigung für den entsprechenden Eintrag registrieren.</span><span class="sxs-lookup"><span data-stu-id="d5d54-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="d5d54-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d5d54-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d5d54-141">Die Benachrichtigung wird vom Adressbuchanbieter nicht unterstützt, der für das objekt verantwortlich ist, das durch den eintragsbezeichner identifiziert wird, der im  _lpEntryID-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="d5d54-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="d5d54-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d5d54-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="d5d54-143">Der in  _lpEntryID_ übergebene Eintragsbezeichner kann nicht von einem der Adressbuchanbieter im Profil verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d54-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d5d54-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5d54-144">Remarks</span></span>

<span data-ttu-id="d5d54-145">Clients und Dienstanbieter rufen die **Advise-Methode** auf, um sich für einen bestimmten Typ oder Benachrichtigungstyp für einen Adressbucheintrag zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d5d54-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="d5d54-146">Die Benachrichtigungstypen werden durch die Ereignismaske angegeben, die mit dem  _ulEventMask-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="d5d54-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="d5d54-147">MAPI gibt diesen **Advise-Aufruf** an den Adressbuchanbieter weiter, der für den Eintrag verantwortlich ist, wie durch den Eintragsbezeichner im  _lpEntryID-Parameter_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="d5d54-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="d5d54-148">Der Adressbuchanbieter übernimmt entweder die Registrierung selbst oder ruft die Supportmethode [IMAPISupport::Subscribe](imapisupport-subscribe.md)auf, um MAPI zur Registrierung des Anrufers auffordern.</span><span class="sxs-lookup"><span data-stu-id="d5d54-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="d5d54-149">Eine Verbindungsnummer ungleich Null wird zurückgegeben, um die erfolgreiche Registrierung zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="d5d54-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="d5d54-150">Wenn eine Änderung am Eintrag des durch die Benachrichtigungsregistrierung angegebenen Typs auftritt, ruft der Adressbuchanbieter die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das im  _lpAdviseSink-Parameter_ angegebene Advise-Sink-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="d5d54-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="d5d54-151">Die **OnNotify-Methode** enthält eine [NOTIFICATION-Struktur](notification.md) als Eingabeparameter, der Daten zur Beschreibung des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="d5d54-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="d5d54-152">Je nach Adressbuchanbieter kann der Aufruf von **OnNotify** unmittelbar nach der Änderung am registrierten Objekt oder zu einem späteren Zeitpunkt erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d5d54-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="d5d54-153">Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** in jedem Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d5d54-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="d5d54-154">Clients können anfordern, dass diese Benachrichtigungen in einem bestimmten Thread auftreten, indem sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) aufrufen, um das an Advise übergebene Advise-Sink-Objekt **zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="d5d54-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="d5d54-155">Da ein Adressbuchanbieter das von Clients übergebene Advise-Sink-Objekt jederzeit nach erfolgreichem Abschluss des **Aufrufs "Advise"** und vor einem [IAddrBook::Unadvise-Aufruf](iaddrbook-unadvise.md) zum Abbrechen der Benachrichtigung lossagen kann, sollten Clients ihre Ratgebersenkenobjekte los, wenn **Advise** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d5d54-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="d5d54-156">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="d5d54-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5d54-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5d54-157">See also</span></span>



[<span data-ttu-id="d5d54-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="d5d54-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="d5d54-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="d5d54-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="d5d54-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d5d54-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d5d54-161">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="d5d54-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="d5d54-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d5d54-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

