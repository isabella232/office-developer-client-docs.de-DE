---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419835"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="0c172-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="0c172-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="0c172-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c172-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c172-105">Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf die Sitzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="0c172-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0c172-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c172-106">Parameters</span></span>

 <span data-ttu-id="0c172-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0c172-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0c172-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="0c172-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0c172-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0c172-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0c172-110">[in] Ein Zeiger auf die Eintrags-ID des Adressbuch- oder Nachrichtenspeicherobjekts, über das Benachrichtigungen generiert werden sollen, oder NULL, der angibt, dass der Client sich für den Empfang von Benachrichtigungen über Ereignisse registriert, die sich nur auf die Sitzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="0c172-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="0c172-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="0c172-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="0c172-112">[in] Eine Maske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, für die der Client interessiert ist und in die Registrierung einbezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="0c172-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="0c172-113">Wenn  _lpEntryID_ NULL ist, registriert MAPI den Client automatisch für kritische Fehlerereignisse, die sich nur auf die Sitzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="0c172-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="0c172-114">Wenn  _lpEntryID_ auf einen Eintragsbezeichner verweist, sind die folgenden Werte für den  _ulEventMask-Parameter_ gültig:</span><span class="sxs-lookup"><span data-stu-id="0c172-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="0c172-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="0c172-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="0c172-116">Registriert für Benachrichtigungen über schwerwiegende Fehler, z. B. unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0c172-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="0c172-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="0c172-117">fnevExtended</span></span> 
  
> <span data-ttu-id="0c172-118">Registriert für Benachrichtigungen über Ereignisse, die für ein bestimmtes Adressbuch oder einen bestimmten Nachrichtenspeicheranbieter spezifisch sind, und für das Herunterfahren der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0c172-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="0c172-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="0c172-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="0c172-120">Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="0c172-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="0c172-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="0c172-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="0c172-122">Registriert für Benachrichtigungen über die Erstellung eines neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c172-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="0c172-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="0c172-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="0c172-124">Registriert für Benachrichtigungen über ein objekt, das kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="0c172-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="0c172-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="0c172-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="0c172-126">Registriert für Benachrichtigungen über ein zu löschendes Objekt.</span><span class="sxs-lookup"><span data-stu-id="0c172-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="0c172-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="0c172-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="0c172-128">Registriert für Benachrichtigungen über ein zu änderndes Objekt.</span><span class="sxs-lookup"><span data-stu-id="0c172-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="0c172-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="0c172-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="0c172-130">Registriert für Benachrichtigungen über ein verschobenes Objekt.</span><span class="sxs-lookup"><span data-stu-id="0c172-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="0c172-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="0c172-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="0c172-132">Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="0c172-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="0c172-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="0c172-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="0c172-134">[in] Ein Zeiger auf ein Advise Sink-Objekt, um die nachfolgenden Benachrichtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0c172-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="0c172-135">Dieses Ratensenkenobjekt muss bereits zugewiesen worden sein.</span><span class="sxs-lookup"><span data-stu-id="0c172-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="0c172-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="0c172-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="0c172-137">[out] Ein Zeiger auf eine Nullnummer, die die Verbindung zwischen dem Ratensenkenobjekt des Anrufers und der Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c172-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c172-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c172-138">Return value</span></span>

<span data-ttu-id="0c172-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c172-139">S_OK</span></span> 
  
> <span data-ttu-id="0c172-140">Die Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0c172-140">The registration was successful.</span></span>
    
<span data-ttu-id="0c172-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0c172-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="0c172-142">Der Eintragsbezeichner, auf den  _lpEntryID verweist,_ stellt keinen gültigen Eintragsbezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="0c172-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="0c172-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0c172-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0c172-144">Der Dienstanbieter, der für den Eintragsbezeichner verantwortlich ist, auf den  _lpEntryID_ verweist, unterstützt entweder den im  _ulEventMask-Parameter_ angegebenen Ereignistyp nicht oder unterstützt keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0c172-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="0c172-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0c172-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0c172-146">Der Eintragsbezeichner, auf den  _lpEntryID verweist,_ kann nicht von einem der Dienstanbieter im Profil verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0c172-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c172-147">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c172-147">Remarks</span></span>

<span data-ttu-id="0c172-148">Die **IMAPISession::Advise-Methode** stellt eine Verbindung zwischen dem Ratgebersenkenobjekt des Anrufers, der Sitzung und optional einem Dienstanbieter fest.</span><span class="sxs-lookup"><span data-stu-id="0c172-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="0c172-149">Diese Verbindung wird verwendet, um Benachrichtigungen an die Ratensenke zu senden, wenn mindestens ein im _ulEventMask-Parameter_ angegebenes Ereignis auf das Objekt auftritt, auf das _von lpEntryID verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="0c172-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="0c172-150">Wenn  _lpEntryID_ NULL ist, ist das Zielobjekt die Sitzung, und Benachrichtigungen werden nur für kritische Fehler und erweiterte Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="0c172-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="0c172-151">Wenn  _lpEntryID_ auf einen gültigen Eintragsbezeichner verweist, ruft MAPI die **Advise-Methode** des Anmeldeobjekts auf, das zum zuständigen Dienstanbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="0c172-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="0c172-152">Wenn beispielsweise  _lpEntryID_ auf den Eintragsbezeichner einer Verteilerliste verweist, ruft MAPI die [IABLogon::Advise-Methode](iablogon-advise.md) des entsprechenden Adressbuchanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="0c172-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="0c172-153">Zum Senden einer Benachrichtigung ruft der Dienstanbieter oder die MAPI die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der registrierten Hinweissenke auf.</span><span class="sxs-lookup"><span data-stu-id="0c172-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="0c172-154">Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0c172-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0c172-155">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0c172-155">Notes to callers</span></span>

<span data-ttu-id="0c172-156">Auf Systemen, die mehrere Ausführungsthreads unterstützen, kann der Aufruf von **OnNotify** jederzeit auch in jedem Thread erfolgen.</span><span class="sxs-lookup"><span data-stu-id="0c172-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="0c172-157">Wenn Sie sicher sein müssen, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink-Funktion](hrthisthreadadvisesink.md) auf, um das Advise Sink-Objekt zu generieren, das Sie an die **Advise-Methode** übergeben.</span><span class="sxs-lookup"><span data-stu-id="0c172-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="0c172-158">Um zu bestimmen, wann sich ein Client abgemeldet hat, registrieren Sie sich für Benachrichtigungen in Ihrem Dienstanbieter, indem Sie **Advise** aufrufen,  _wenn lpEntryID_ auf NULL und  _cbEntryID_ auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c172-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="0c172-159">Wenn die Abmeldung auftritt, erhalten Sie eine fnevExtended-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="0c172-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="0c172-160">Nachdem ein Aufruf von **Advise** erfolgreich war und [bevor IMAPISession::Unadvise](imapisession-unadvise.md) zum Abbrechen der Registrierung aufgerufen wurde, geben Sie Ihr Advise Sink-Objekt frei, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="0c172-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="0c172-161">Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0c172-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="0c172-162">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0c172-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0c172-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="0c172-163">MFCMAPI reference</span></span>

<span data-ttu-id="0c172-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0c172-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0c172-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0c172-165">**File**</span></span>|<span data-ttu-id="0c172-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0c172-166">**Function**</span></span>|<span data-ttu-id="0c172-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0c172-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c172-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="0c172-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="0c172-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="0c172-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="0c172-170">MFCMAPI verwendet die **IMAPISession::Advise-Methode, um** sich für Benachrichtigungen für die Sitzung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0c172-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c172-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c172-171">See also</span></span>



[<span data-ttu-id="0c172-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="0c172-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="0c172-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0c172-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="0c172-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0c172-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0c172-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0c172-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="0c172-176">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c172-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="0c172-177">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0c172-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0c172-178">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="0c172-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

