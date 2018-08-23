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
ms.openlocfilehash: 704a556b97f5fd90989641a17afe5a11d127e51b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577170"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="96d90-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="96d90-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="96d90-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96d90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96d90-105">Um die Benachrichtigung der angegebenen Ereignisse, die Einfluss auf die Sitzung registriert.</span><span class="sxs-lookup"><span data-stu-id="96d90-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="96d90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96d90-106">Parameters</span></span>

 <span data-ttu-id="96d90-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="96d90-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="96d90-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="96d90-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="96d90-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="96d90-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="96d90-110">[in] Ein Zeiger auf die Eintrags-ID des Adressbuch oder Message Store-Objekts darüber, welche Benachrichtigungen generiert werden soll, oder NULL-Wert gibt an, dass der Client Erhalt von Benachrichtigungen zu Ereignissen, die nur die Sitzung betreffen registriert wird.</span><span class="sxs-lookup"><span data-stu-id="96d90-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="96d90-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="96d90-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="96d90-112">[in] Eine Maske von Werten, mit die die Typen von Benachrichtigungsereignisse anzugeben, die der Client ist daran interessiert, und in der Registrierung eingeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="96d90-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="96d90-113">Wenn _LpEntryID_ NULL ist, registriert MAPI automatisch den Client für kritische Fehlerereignisse, die nur die Sitzung zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="96d90-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="96d90-114">Wenn _LpEntryID_ auf einen Eintrag Bezeichner verweist, sind die folgenden Werte für den Parameter _UlEventMask_ gültig:</span><span class="sxs-lookup"><span data-stu-id="96d90-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="96d90-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="96d90-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="96d90-116">Register für Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="96d90-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="96d90-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="96d90-117">fnevExtended</span></span> 
  
> <span data-ttu-id="96d90-118">Register für Benachrichtigungen über Ereignisse, die speziell für ein bestimmtes Adressbuch oder einer Nachricht Speicheranbieter und zur Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="96d90-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="96d90-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="96d90-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="96d90-120">Register für die Benachrichtigung über den Empfang von neuen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="96d90-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="96d90-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="96d90-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="96d90-122">Register für die Benachrichtigung über die Erstellung eines neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="96d90-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="96d90-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="96d90-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="96d90-124">Register für Benachrichtigungen zu einem Objekt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="96d90-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="96d90-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="96d90-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="96d90-126">Register für Benachrichtigungen zu einem Objekt, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="96d90-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="96d90-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="96d90-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="96d90-128">Register für Benachrichtigungen zu einem Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="96d90-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="96d90-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="96d90-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="96d90-130">Register für Benachrichtigungen zu einem Objekt verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="96d90-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="96d90-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="96d90-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="96d90-132">Register für die Benachrichtigung über den Abschluss der Suchvorgang.</span><span class="sxs-lookup"><span data-stu-id="96d90-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="96d90-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="96d90-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="96d90-134">[in] Ein Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="96d90-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="96d90-135">Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="96d90-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="96d90-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="96d90-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="96d90-137">[out] Ein Zeiger auf eine Zahl ungleich NULL für die Verbindung zwischen des Anrufers advise-Empfängerobjekt und der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="96d90-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="96d90-138">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="96d90-138">Return value</span></span>

<span data-ttu-id="96d90-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="96d90-139">S_OK</span></span> 
  
> <span data-ttu-id="96d90-140">Die Registrierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="96d90-140">The registration was successful.</span></span>
    
<span data-ttu-id="96d90-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="96d90-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="96d90-142">Die Eintrags-ID auf den _LpEntryID_ stellt keinen gültige Eingabe Bezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="96d90-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="96d90-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="96d90-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="96d90-144">Der Dienstanbieter verantwortlich für die Eintrags-ID auf den _LpEntryID_ unterstützt nicht die Art der Ereignisse in der _UlEventMask_ -Parameter angegeben, oder unterstützt keine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="96d90-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="96d90-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="96d90-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="96d90-146">Die Eintrags-ID auf den _LpEntryID_ kann von jedem-Dienstanbieter im Profil behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="96d90-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="96d90-147">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="96d90-147">Remarks</span></span>

<span data-ttu-id="96d90-148">Die **IMAPISession::Advise** -Methode richtet eine Verbindung zwischen dem Anrufer der advise-Empfängerobjekt, die Sitzung und optional einem Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="96d90-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="96d90-149">Diese Verbindung wird verwendet, um das Senden von Benachrichtigungen an der Advise-Empfänger, wenn sich ein oder mehr Ereignisse in der _UlEventMask_ -Parameter angegebene auf das Objekt, auf das _LpEntryID_auftreten.</span><span class="sxs-lookup"><span data-stu-id="96d90-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="96d90-150">Wenn _LpEntryID_ NULL ist, das Zielobjekt ist die Sitzung und Benachrichtigungen werden nur für schwerwiegende Fehler und erweiterte Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="96d90-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="96d90-151">Wenn _LpEntryID_ auf einen gültigen Eintrag Bezeichner verweist, ruft MAPI die **Advise** -Methode des Anmeldung-Objekts, das an den zuständigen Dienstanbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="96d90-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="96d90-152">Beispielsweise ruft _LpEntryID_ auf die Eintrags-ID einer Verteilerliste verweist, MAPI die entsprechenden-Adressbuchanbieter [IABLogon::Advise](iablogon-advise.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="96d90-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="96d90-153">Um eine Benachrichtigung zu senden, Dienstanbieter oder MAPI der registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="96d90-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="96d90-154">Einer der Parameter zu **OnNotify**, eine Benachrichtigungsstruktur enthält Informationen des jeweiligen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="96d90-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="96d90-155">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="96d90-155">Notes to callers</span></span>

<span data-ttu-id="96d90-156">Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auch jederzeit auf einem beliebigen Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="96d90-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="96d90-157">Wenn Sie Benachrichtigungen nur zu einem bestimmten Zeitpunkt in einem bestimmten Thread treten Assurance benötigen, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion, um das Empfängerobjekt Advise generieren, das Sie an der **Advise** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="96d90-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="96d90-158">Um zu bestimmen, wann ein Client abgemeldet, registrieren Sie sich für Benachrichtigungen in Ihren Dienstanbieter durch Aufrufen von **Advise** mit _LpEntryID_ festlegen auf NULL und _CbEntryID_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="96d90-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="96d90-159">Wenn die Abmeldung auftritt, erhalten Sie eine Benachrichtigung FnevExtended.</span><span class="sxs-lookup"><span data-stu-id="96d90-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="96d90-160">Freigeben Sie nach ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor [IMAPISession::Unadvise](imapisession-unadvise.md) aufgerufen wurde, um die Registrierung abzubrechen, Ihrer Advise-Empfängerobjekt, es sei denn, Sie eine bestimmte langfristige Verwendung dafür haben.</span><span class="sxs-lookup"><span data-stu-id="96d90-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="96d90-161">Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="96d90-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="96d90-162">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Behandeln von Benachrichtigungen](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="96d90-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="96d90-163">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="96d90-163">MFCMAPI reference</span></span>

<span data-ttu-id="96d90-164">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="96d90-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="96d90-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="96d90-165">**File**</span></span>|<span data-ttu-id="96d90-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="96d90-166">**Function**</span></span>|<span data-ttu-id="96d90-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="96d90-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96d90-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="96d90-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="96d90-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="96d90-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="96d90-170">MFCMAPI (engl.) verwendet die **IMAPISession::Advise** -Methode, um für Benachrichtigungen vor der Sitzung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="96d90-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96d90-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96d90-171">See also</span></span>



[<span data-ttu-id="96d90-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="96d90-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="96d90-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="96d90-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="96d90-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="96d90-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="96d90-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="96d90-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="96d90-176">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="96d90-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="96d90-177">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="96d90-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="96d90-178">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="96d90-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

