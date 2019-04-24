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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338619"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="869b2-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="869b2-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="869b2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="869b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="869b2-105">Registriert die Benachrichtigung über die angegebenen Ereignisse, die sich auf die Sitzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="869b2-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="869b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="869b2-106">Parameters</span></span>

 <span data-ttu-id="869b2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="869b2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="869b2-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="869b2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="869b2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="869b2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="869b2-110">in Ein Zeiger auf die Eintrags-ID des Adressbuch-oder Nachrichtenspeicher Objekts, über das Benachrichtigungen generiert werden sollen, oder NULL, was darauf hinweist, dass der Client sich für den Empfang von Benachrichtigungen über Ereignisse registriert, die sich nur auf die Sitzung auswirken.</span><span class="sxs-lookup"><span data-stu-id="869b2-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="869b2-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="869b2-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="869b2-112">in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Client interessiert ist, und die in die Registrierung aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="869b2-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="869b2-113">Wenn _lpEntryID_ ist, registriert MAPI den Client automatisch auf kritische Fehlerereignisse, die nur die Sitzung betreffen.</span><span class="sxs-lookup"><span data-stu-id="869b2-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="869b2-114">Wenn _lpEntryID_ auf eine Eintrags-ID zeigt, sind die folgenden Werte für den _ulEventMask_ -Parameter gültig:</span><span class="sxs-lookup"><span data-stu-id="869b2-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="869b2-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="869b2-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="869b2-116">Registriert Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="869b2-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="869b2-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="869b2-117">fnevExtended</span></span> 
  
> <span data-ttu-id="869b2-118">Registriert Benachrichtigungen zu Ereignissen, die für ein bestimmtes Adressbuch oder einen bestimmten Nachrichtenspeicher Anbieter spezifisch sind, sowie für die Sitzungs Sperrung.</span><span class="sxs-lookup"><span data-stu-id="869b2-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="869b2-119">Uleventmaskfnevnewmail</span><span class="sxs-lookup"><span data-stu-id="869b2-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="869b2-120">Registriert Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="869b2-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="869b2-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="869b2-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="869b2-122">Registriert Benachrichtigungen über die Erstellung eines neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="869b2-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="869b2-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="869b2-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="869b2-124">Registriert Benachrichtigungen zu einem kopierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="869b2-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="869b2-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="869b2-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="869b2-126">Registriert Benachrichtigungen zu einem Objekt, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="869b2-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="869b2-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="869b2-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="869b2-128">Registriert Benachrichtigungen zu einem Objekt, das geändert wird.</span><span class="sxs-lookup"><span data-stu-id="869b2-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="869b2-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="869b2-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="869b2-130">Registriert Benachrichtigungen zu einem Objekt, das verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="869b2-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="869b2-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="869b2-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="869b2-132">Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="869b2-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="869b2-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="869b2-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="869b2-134">in Ein Zeiger auf ein Advise-Senke-Objekt, um die nachfolgenden Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="869b2-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="869b2-135">Dieses Advise-Senke-Objekt muss bereits zugeordnet worden sein.</span><span class="sxs-lookup"><span data-stu-id="869b2-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="869b2-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="869b2-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="869b2-137">Out Ein Zeiger auf eine Zahl ungleich NULL, die die Verbindung zwischen dem Advise-Objekt des Empfängers und der Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="869b2-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="869b2-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="869b2-138">Return value</span></span>

<span data-ttu-id="869b2-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="869b2-139">S_OK</span></span> 
  
> <span data-ttu-id="869b2-140">Die Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="869b2-140">The registration was successful.</span></span>
    
<span data-ttu-id="869b2-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="869b2-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="869b2-142">Die Eintrags-ID, auf die durch _lpEntryID_ verwiesen wird, stellt keine gültige Eintrags-ID dar.</span><span class="sxs-lookup"><span data-stu-id="869b2-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="869b2-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="869b2-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="869b2-144">Der Dienstanbieter, der für den Eintragsbezeichner verantwortlich ist, auf den von _lpEntryID_ verwiesen wird, unterstützt entweder nicht die im Parameter _ulEventMask_ angegebene Art von Ereignissen oder unterstützt die Benachrichtigung nicht.</span><span class="sxs-lookup"><span data-stu-id="869b2-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="869b2-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="869b2-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="869b2-146">Die Eintrags-ID, auf die durch _lpEntryID_ verwiesen wird, kann von keinem der Dienstanbieter im Profil verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="869b2-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="869b2-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="869b2-147">Remarks</span></span>

<span data-ttu-id="869b2-148">Die **IMAPISession:: Advise** -Methode stellt eine Verbindung zwischen dem Advise-Objekt des Anrufers, der Sitzung und optional einem Dienstanbieter her.</span><span class="sxs-lookup"><span data-stu-id="869b2-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="869b2-149">Diese Verbindung wird verwendet, um Benachrichtigungen an die Advise-Senke zu senden, wenn ein oder mehrere im _ulEventMask_ -Parameter angegebene Ereignisse für das Objekt auftreten, auf das durch _lpEntryID_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="869b2-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="869b2-150">Wenn _lpEntryID_ ist, ist das Zielobjekt die Sitzung, und Benachrichtigungen werden nur für kritische Fehler und erweiterte Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="869b2-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="869b2-151">Wenn _lpEntryID_ auf eine gültige Eintrags-ID zeigt, ruft MAPI die **Advise** -Methode des LOGON-Objekts auf, das zum Verantwortlichen Dienstanbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="869b2-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="869b2-152">Wenn _lpEntryID_ beispielsweise auf den Eintragsbezeichner einer Verteilerliste zeigt, ruft MAPI die [IABLogon:: Advise](iablogon-advise.md) -Methode des entsprechenden Adressbuch Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="869b2-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="869b2-153">Zum Senden einer Benachrichtigung ruft der Dienstanbieter oder die MAPI die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der registrierten Advise-Senke auf.</span><span class="sxs-lookup"><span data-stu-id="869b2-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="869b2-154">Einer der Parameter für **OnNotify**, eine Benachrichtigungsstruktur, enthält Informationen, die das spezifische Ereignis beschreiben.</span><span class="sxs-lookup"><span data-stu-id="869b2-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="869b2-155">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="869b2-155">Notes to callers</span></span>

<span data-ttu-id="869b2-156">Auf Systemen, die mehrere Threads der Ausführung unterstützen, kann \*\*\*\* der Aufruf von OnNotify auch jederzeit in jedem Thread auftreten.</span><span class="sxs-lookup"><span data-stu-id="869b2-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="869b2-157">Wenn Sie sicherstellen möchten, dass Benachrichtigungen nur zu einem bestimmten Zeitpunkt für einen bestimmten Thread auftreten, rufen Sie die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion auf, um das Advise-Senke-Objekt zu generieren, das Sie an die **Advise** -Methode weitergeben.</span><span class="sxs-lookup"><span data-stu-id="869b2-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="869b2-158">Um zu bestimmen, wann sich ein Client abgemeldet hat, registrieren Sie sich in Ihrem Dienstanbieter, indem Sie **Advise** aufrufen, wobei _lpEntryID_ auf NULL festgelegt und _cbEntryID_ auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="869b2-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="869b2-159">Wenn die Abmeldung auftritt, erhalten Sie eine fnevExtended-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="869b2-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="869b2-160">Nachdem ein Anruf bei **Advise** erfolgreich abgeschlossen wurde und bevor [IMAPISession:: Unadvise](imapisession-unadvise.md) aufgerufen wurde, um die Registrierung abzubrechen, lassen Sie Ihr Advise-Senke-Objekt Los, es sei denn, Sie haben eine bestimmte langfristige Verwendung dafür.</span><span class="sxs-lookup"><span data-stu-id="869b2-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="869b2-161">Eine Übersicht über den Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="869b2-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="869b2-162">Weitere Informationen zum Behandeln von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="869b2-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="869b2-163">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="869b2-163">MFCMAPI reference</span></span>

<span data-ttu-id="869b2-164">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="869b2-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="869b2-165">**Datei**</span><span class="sxs-lookup"><span data-stu-id="869b2-165">**File**</span></span>|<span data-ttu-id="869b2-166">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="869b2-166">**Function**</span></span>|<span data-ttu-id="869b2-167">**Comment**</span><span class="sxs-lookup"><span data-stu-id="869b2-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="869b2-168">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="869b2-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="869b2-169">CBaseDialog:: OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="869b2-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="869b2-170">MFCMAPI verwendet die **IMAPISession:: Advise** -Methode, um Benachrichtigungen für die Sitzung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="869b2-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="869b2-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="869b2-171">See also</span></span>



[<span data-ttu-id="869b2-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="869b2-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="869b2-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="869b2-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="869b2-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="869b2-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="869b2-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="869b2-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="869b2-176">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="869b2-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="869b2-177">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="869b2-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="869b2-178">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="869b2-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

