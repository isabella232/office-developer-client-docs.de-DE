---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424119"
---
# <a name="mapilogonex"></a><span data-ttu-id="b12cf-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="b12cf-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="b12cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b12cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b12cf-105">Protokolliert eine Clientanwendung bei einer Sitzung mit dem Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="b12cf-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b12cf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b12cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="b12cf-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b12cf-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b12cf-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b12cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b12cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b12cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b12cf-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b12cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="b12cf-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="b12cf-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="b12cf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b12cf-112">Parameters</span></span>

 <span data-ttu-id="b12cf-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b12cf-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="b12cf-114">[in] Behandeln Sie das Fenster, in das das Anmeldedialogfeld modal ist.</span><span class="sxs-lookup"><span data-stu-id="b12cf-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="b12cf-115">Wenn während des Aufrufs kein Dialogfeld angezeigt wird, wird der  _ulUIParam-Parameter_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b12cf-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="b12cf-116">Dieser Parameter kann null sein.</span><span class="sxs-lookup"><span data-stu-id="b12cf-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="b12cf-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="b12cf-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="b12cf-118">[in] Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das verwendet werden soll, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b12cf-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="b12cf-119">Diese Zeichenfolge ist auf 64 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b12cf-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="b12cf-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="b12cf-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="b12cf-121">[in] Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält.</span><span class="sxs-lookup"><span data-stu-id="b12cf-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="b12cf-122">Der  _lpszPassword-Parameter_ muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b12cf-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="b12cf-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="b12cf-123">_flFlags_</span></span>
  
> <span data-ttu-id="b12cf-124">[in] Bitmaske von Flags, die verwendet werden, um zu steuern, wie die Anmeldung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b12cf-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="b12cf-125">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b12cf-125">The following flags can be set:</span></span>
    
<span data-ttu-id="b12cf-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="b12cf-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="b12cf-127">Die freigegebene Sitzung sollte zurückgegeben werden, wodurch spätere Clients die Sitzung ohne Angabe von Benutzeranmeldeinformationen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="b12cf-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="b12cf-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="b12cf-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="b12cf-129">Melden Sie sich bei einer Sitzung an, und führen Sie alle Vorgänge im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b12cf-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="b12cf-130">Im Allgemeinen sollte ein Client, wenn er beabsichtigt, die Verarbeitung in einem Hintergrundthread oder in einem separaten Prozess auf eine Weise durchzuführen, die unauffällig für den Vordergrundthread ist, mit dem MAPI_BG_SESSION aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b12cf-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="b12cf-131">Eine Clientanwendung wie ein Indizierungsmodul oder das Öffnen einer Persönlichen Ordnerdatei (Pst) für den Hintergrundtypzugriff sind einige Beispiele für die Verwendung von MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="b12cf-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="b12cf-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b12cf-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="b12cf-133">Das Standardprofil sollte nicht verwendet werden, und der Benutzer sollte zur Bereitstellung eines Profils verpflichtet sein.</span><span class="sxs-lookup"><span data-stu-id="b12cf-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="b12cf-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="b12cf-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="b12cf-135">Melden Sie sich mit erweiterten Funktionen an.</span><span class="sxs-lookup"><span data-stu-id="b12cf-135">Log on with extended capabilities.</span></span> <span data-ttu-id="b12cf-136">Dieses Flag sollte immer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-136">This flag should always be set.</span></span>
    
<span data-ttu-id="b12cf-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="b12cf-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="b12cf-138">Es sollte versucht werden, alle Nachrichten des Benutzers herunterzuladen, bevor sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="b12cf-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="b12cf-139">Wenn das MAPI_FORCE_DOWNLOAD nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Aufruf von MAPILogonEx zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b12cf-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="b12cf-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="b12cf-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="b12cf-141">Es sollte ein Dialogfeld angezeigt werden, in dem der Benutzer bei Bedarf zur Eingabe von Anmeldeinformationen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="b12cf-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="b12cf-142">Wenn das MAPI_LOGON_UI nicht festgelegt ist, zeigt der aufrufende Client kein Anmeldedialogfeld an und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b12cf-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="b12cf-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="b12cf-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="b12cf-144">Es sollte versucht werden, eine neue MAPI-Sitzung zu erstellen, anstatt die freigegebene Sitzung zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="b12cf-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="b12cf-145">Wenn das MAPI_NEW_SESSION nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, auch wenn der  _lpszprofileName-Parameter_ nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b12cf-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="b12cf-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="b12cf-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="b12cf-147">MAPI sollte den MAPI-Spooler nicht über das Vorhandensein der Sitzung informieren.</span><span class="sxs-lookup"><span data-stu-id="b12cf-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="b12cf-148">Das Ergebnis ist, dass keine Nachrichten in der Sitzung gesendet oder empfangen werden können, außer über ein eng gekoppeltes Speicher- und Transportpaar.</span><span class="sxs-lookup"><span data-stu-id="b12cf-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="b12cf-149">Ein aufrufender Client legt dieses Flag fest, wenn er als Agent agiert, wenn Konfigurationsarbeiten ausgeführt werden müssen oder wenn der Client die verfügbaren Nachrichtenspeicher durchstöbert.</span><span class="sxs-lookup"><span data-stu-id="b12cf-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="b12cf-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b12cf-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="b12cf-151">Der Anrufer wird als Dienst Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b12cf-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="b12cf-152">Anrufer, die nicht als Dienst Windows, sollten dieses Flag nicht festlegen. Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="b12cf-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="b12cf-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="b12cf-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="b12cf-154">MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b12cf-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="b12cf-155">Die Dialogfelder werden angezeigt, nachdem das Profil ausgewählt wurde, aber bevor ein Nachrichtendienst angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="b12cf-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="b12cf-156">Das allgemeine Dialogfeld MAPI für die Anmeldung enthält auch ein Kontrollkästchen, das denselben Vorgang anfordert.</span><span class="sxs-lookup"><span data-stu-id="b12cf-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="b12cf-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="b12cf-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="b12cf-158">Die Anmeldung sollte fehlschlagen, wenn sie länger als ein paar Sekunden blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="b12cf-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="b12cf-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b12cf-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b12cf-160">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b12cf-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b12cf-161">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b12cf-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="b12cf-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b12cf-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="b12cf-163">Das Messagingsubsystem sollte den Profilnamen des Standardprofils durch den  _lpszProfileName-Parameter_ ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b12cf-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="b12cf-164">Das MAPI_EXPLICIT_PROFILE wird ignoriert, es sei  _denn, lpszProfileName_ ist NULL oder leer.</span><span class="sxs-lookup"><span data-stu-id="b12cf-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="b12cf-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="b12cf-165">_lppSession_</span></span>
  
> <span data-ttu-id="b12cf-166">[out] Zeiger auf einen Zeiger auf die MAPI-Sitzungsschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b12cf-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b12cf-167">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b12cf-167">Return value</span></span>

<span data-ttu-id="b12cf-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="b12cf-168">S_OK</span></span> 
  
> <span data-ttu-id="b12cf-169">Die Anmeldung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b12cf-169">The logon succeeded.</span></span>
    
<span data-ttu-id="b12cf-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="b12cf-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="b12cf-171">Die Anmeldung war nicht erfolgreich, weil einer oder mehrere Parameter für MAPILogonEx ungültig waren oder weil bereits zu viele Sitzungen geöffnet waren.</span><span class="sxs-lookup"><span data-stu-id="b12cf-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="b12cf-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b12cf-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="b12cf-173">MAPI serialisiert alle Anmeldungen über ein Mutex.</span><span class="sxs-lookup"><span data-stu-id="b12cf-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="b12cf-174">Dies wird zurückgegeben, wenn das MAPI_TIMEOUT_SHORT festgelegt wurde und ein anderer Thread den Mutex gehalten hat.</span><span class="sxs-lookup"><span data-stu-id="b12cf-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="b12cf-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b12cf-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b12cf-176">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b12cf-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b12cf-177">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b12cf-177">Remarks</span></span>

<span data-ttu-id="b12cf-178">MAPI-Clientanwendungen rufen die MAPILogonEx-Funktion auf, um sich bei einer Sitzung mit dem Messagingsystem zu anmelden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="b12cf-179">Alle Zeichenfolgen, die an und von MAPI-Aufrufen übergeben und von diesen zurückgegeben werden, sind null-terminated und müssen im aktuellen Zeichensatz oder der Codeseite des Betriebssystems des aufrufenden Clients oder Anbieters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="b12cf-180">Der  _lpszProfileName-Parameter_ wird ignoriert, wenn es eine vorhandene vorherige Sitzung mit dem Namen MapiLogonEx mit dem MAPI_ALLOW_OTHERS-Flag gibt und das Flag MAPI_NEW_SESSION nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b12cf-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="b12cf-181">Wenn der  _lpszProfileName-Parameter_ NULL ist oder auf eine leere Zeichenfolge verweist und der  _flFlags-Parameter_ das MAPI_LOGON_UI-Flag enthält, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld mit einem leeren Feld für den Profilnamen.</span><span class="sxs-lookup"><span data-stu-id="b12cf-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="b12cf-182">Bei der Anmeldung bei einem bestimmten Profil sollte ein Client das MAPI_NEW_SESSION zusätzlich zum Profilnamen an MAPILogonEx übergeben.</span><span class="sxs-lookup"><span data-stu-id="b12cf-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="b12cf-183">Andernfalls wird der Client bei der freigegebenen Sitzung anstelle des angeforderten Profils angemeldet, wenn ein anderer Client eine freigegebene Sitzung durch die Anmeldung bei MAPI_ALLOW_OTHERS eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="b12cf-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="b12cf-184">Das MAPI_EXPLICIT_PROFILE führt nicht dazu, dass der Standardprofilname verwendet wird, wenn  _lpszProfileName_ NULL oder leer ist, es sei denn, das MAPI_USE_DEFAULT-Flag ist ebenfalls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="b12cf-185">Das MAPI_NO_MAIL hat mehrere Effekte, die Folgendes verursachen, wenn der MAPI-Spooler nicht verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="b12cf-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="b12cf-186">Während dieser Sitzung können keine Nachrichten vom MAPI-Spooler gesendet oder zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="b12cf-187">Nur eng gekoppelte Speicher- und Transportanbieter können Nachrichten senden und senden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="b12cf-188">Serverbasierte Speicher senden oder senden möglicherweise weiterhin Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="b12cf-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="b12cf-189">Nachrichten, die von serverbasierten Speichern gesendet oder zugestellt werden, werden von keinem Hookanbieter verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b12cf-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="b12cf-190">Optionen pro Nachricht und Empfänger für Transporte sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b12cf-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="b12cf-191">Die Statustabelle enthält keine Einträge für Transportanbieter, und von Statusobjekten (z. B. Konfiguration) abhängige Transportfunktionen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b12cf-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="b12cf-192">Die Zeile "Nachrichtenspooler" in der Statustabelle enthält den STATUS_FAILURE Wert.</span><span class="sxs-lookup"><span data-stu-id="b12cf-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="b12cf-193">Schweinchen-Anmeldungen sind zulässig, aber diese Anmeldungen führen nicht dazu, dass die vorherige Anmeldung Statusobjektaktualisierungen erhält.</span><span class="sxs-lookup"><span data-stu-id="b12cf-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="b12cf-194">Ein Dienst sollte sich immer mit dem MAPI_NO_MAIL anmelden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b12cf-195">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b12cf-195">MFCMAPI reference</span></span>

<span data-ttu-id="b12cf-196">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b12cf-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b12cf-197">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b12cf-197">**File**</span></span>|<span data-ttu-id="b12cf-198">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b12cf-198">**Function**</span></span>|<span data-ttu-id="b12cf-199">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b12cf-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b12cf-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="b12cf-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="b12cf-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="b12cf-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="b12cf-202">MFCMAPI verwendet die MAPILogonEx-Methode, um sich bei MAPI zu anmelden.</span><span class="sxs-lookup"><span data-stu-id="b12cf-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b12cf-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b12cf-203">See also</span></span>



[<span data-ttu-id="b12cf-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="b12cf-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="b12cf-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b12cf-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="b12cf-206">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b12cf-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

