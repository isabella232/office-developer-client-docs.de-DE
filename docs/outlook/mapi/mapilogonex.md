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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793116"
---
# <a name="mapilogonex"></a><span data-ttu-id="6d266-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6d266-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="6d266-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d266-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d266-105">Meldet eine Clientanwendung bei einer Sitzung mit der messaging-System.</span><span class="sxs-lookup"><span data-stu-id="6d266-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d266-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6d266-106">Header file:</span></span>  <br/> |<span data-ttu-id="6d266-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="6d266-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6d266-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6d266-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6d266-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6d266-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6d266-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6d266-110">Called by:</span></span>  <br/> |<span data-ttu-id="6d266-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="6d266-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="6d266-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d266-112">Parameters</span></span>

 <span data-ttu-id="6d266-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6d266-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6d266-114">[in] Handle für das Fenster, das Anmeldedialogfeld gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="6d266-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="6d266-115">Wenn kein Dialogfeld während des Anrufs angezeigt wird, wird der Parameter _UlUIParam_ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6d266-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="6d266-116">Dieser Parameter kann 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6d266-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="6d266-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6d266-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6d266-118">[in] Zeiger auf eine Zeichenfolge, die enthält den Namen des Profils beim Anmelden des Benutzers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d266-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="6d266-119">Diese Zeichenfolge ist auf 64 Zeichen begrenzt.</span><span class="sxs-lookup"><span data-stu-id="6d266-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="6d266-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="6d266-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="6d266-121">[in] Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält.</span><span class="sxs-lookup"><span data-stu-id="6d266-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="6d266-122">Der Parameter _LpszPassword_ muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6d266-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="6d266-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="6d266-123">_flFlags_</span></span>
  
> <span data-ttu-id="6d266-124">[in] Bitmaske aus Flags verwendet, um zu steuern, wie die Anmeldung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d266-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="6d266-125">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6d266-125">The following flags can be set:</span></span>
    
<span data-ttu-id="6d266-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="6d266-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="6d266-127">Die freigegebene Sitzung sollte zurückgegeben werden, wodurch höher Clients erhalten die Sitzung ohne Angabe von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="6d266-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="6d266-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="6d266-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="6d266-129">Melden Sie sich bei einer Sitzung, und alle Vorgänge im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d266-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="6d266-130">Im Allgemeinen Clientidentität will Verarbeitung in einem Hintergrundthread oder in einem gesonderten Prozess in einer Weise, die nicht störend auf den Vordergrundthread ist, muss sie mit dem MAPI_BG_SESSION-Flag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6d266-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="6d266-131">Eine Clientanwendung wie indexing-Engine oder öffnen eine Persönliche Ordner Datei (PST) für den Hintergrund Typ Zugriff sind einige Beispiele für die Verwendung mit dem MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="6d266-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="6d266-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="6d266-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="6d266-133">Das Standardprofil sollte nicht verwendet werden, und der Benutzer sollte erforderlich, um ein Profil angeben.</span><span class="sxs-lookup"><span data-stu-id="6d266-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="6d266-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="6d266-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="6d266-135">Melden Sie sich mit erweiterten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6d266-135">Log on with extended capabilities.</span></span> <span data-ttu-id="6d266-136">Dieses Kennzeichen sollte immer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6d266-136">This flag should always be set.</span></span>
    
<span data-ttu-id="6d266-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="6d266-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="6d266-138">Es sollten Sie alle Nachrichten des Benutzers vor der Rückgabe herunterladen versucht werden.</span><span class="sxs-lookup"><span data-stu-id="6d266-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="6d266-139">Wenn das Flag MAPI_FORCE_DOWNLOAD nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Anruf an MAPILogonEx zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d266-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="6d266-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="6d266-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="6d266-141">Ein Dialogfeld sollte angezeigt werden, um den Benutzer zur Anmeldeinformationen auffordern, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6d266-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="6d266-142">Wenn das Flag MAPI_LOGON_UI nicht festgelegt ist, der aufrufende Client ein Anmeldedialogfeld wird nicht angezeigt und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="6d266-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="6d266-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="6d266-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="6d266-144">Soll versucht werden, erstellen Sie eine neue MAPI-Sitzung anstelle die freigegebene Sitzung erwerben.</span><span class="sxs-lookup"><span data-stu-id="6d266-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="6d266-145">Wenn das Flag MAPI_NEW_SESSION nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, selbst wenn der Parameter _LpszprofileName_ nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="6d266-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="6d266-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="6d266-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="6d266-147">MAPI informiert sollte nicht die MAPI-Warteschlange des Vorhandenseins der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6d266-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="6d266-148">Das Ergebnis ist, dass keine Nachrichten gesendet oder in der Sitzung außer über einen eng gekoppelten speichern und-Paar Transport empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="6d266-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="6d266-149">Ein aufrufende Client wird dieses Flag, wenn es als ein Agent fungiert, wenn Sie Konfigurationsarbeit erledigt werden muss, oder wenn der Client den verfügbaren Nachrichtenspeicher durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6d266-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="6d266-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6d266-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6d266-151">Der Anrufer wird als Windows-Dienst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d266-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="6d266-152">Anrufer, die wie ein Windows-Dienst nicht dieses Flag festlegen sollten nicht ausgeführt werden; Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d266-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="6d266-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="6d266-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="6d266-154">MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d266-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="6d266-155">Die Dialogfelder werden angezeigt, nachdem das Profil gewählt wurde, jedoch bevor eine beliebige Nachricht Service angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="6d266-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="6d266-156">MAPI-Standarddialogfeld für die Anmeldung enthält auch ein Kontrollkästchen, die den gleichen Vorgang anfordert.</span><span class="sxs-lookup"><span data-stu-id="6d266-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="6d266-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="6d266-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="6d266-158">Wenn für mehr als ein paar Sekunden blockiert, sollte die Anmeldung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="6d266-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="6d266-159">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6d266-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6d266-160">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6d266-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6d266-161">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6d266-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="6d266-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6d266-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="6d266-163">Das messaging Subsystem sollten den Profilnamen des Standardprofils für den Parameter _LpszProfileName_ ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6d266-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="6d266-164">Das Flag MAPI_EXPLICIT_PROFILE wird ignoriert, es sei denn, _LpszProfileName_ NULL oder leer ist.</span><span class="sxs-lookup"><span data-stu-id="6d266-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="6d266-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="6d266-165">_lppSession_</span></span>
  
> <span data-ttu-id="6d266-166">[out] Zeiger auf einen Zeiger auf die MAPI-Sitzung-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6d266-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6d266-167">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6d266-167">Return value</span></span>

<span data-ttu-id="6d266-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d266-168">S_OK</span></span> 
  
> <span data-ttu-id="6d266-169">Die Anmeldung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6d266-169">The logon succeeded.</span></span>
    
<span data-ttu-id="6d266-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="6d266-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="6d266-171">Die Anmeldung ist fehlgeschlagen, da eine oder mehrere der Parameter MAPILogonEx ungültig waren oder bereits zu viele Sitzungen geöffnet waren.</span><span class="sxs-lookup"><span data-stu-id="6d266-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="6d266-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6d266-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="6d266-173">MAPI serialisiert alle Anmeldungen über einen Mutex.</span><span class="sxs-lookup"><span data-stu-id="6d266-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="6d266-174">Dies wird zurückgegeben, wenn das Flag MAPI_TIMEOUT_SHORT festgelegt wurde, und ein anderer Thread den Mutex frei.</span><span class="sxs-lookup"><span data-stu-id="6d266-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="6d266-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6d266-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6d266-176">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6d266-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6d266-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d266-177">Remarks</span></span>

<span data-ttu-id="6d266-178">MAPI-Clientanwendungen rufen Sie die Funktion MAPILogonEx zur Anmeldung bei einer Sitzung mit der messaging-System.</span><span class="sxs-lookup"><span data-stu-id="6d266-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="6d266-179">Alle Zeichenfolgen, die übergeben und zurückgegeben, zu und von MAPI-Aufrufe Null endende werden und müssen in der aktuellen Zeichensatz angegeben werden oder Codepage des aufrufenden Client oder Anbieter des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="6d266-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="6d266-180">Der Parameter _LpszProfileName_ wird ignoriert, wenn eine vorhandene vorherige Sitzung, die mit dem MAPI_ALLOW_OTHERS-Flag MapiLogonEx aufgerufen vorhanden ist und das Flag MAPI_NEW_SESSION nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6d266-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="6d266-181">Wenn der Parameter _LpszProfileName_ NULL ist oder verweist auf eine leere Zeichenfolge und der Parameter _FlFlags_ umfasst das MAPI_LOGON_UI-Flag, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld, die ein leeres Feld für den Namen des Profils verfügt.</span><span class="sxs-lookup"><span data-stu-id="6d266-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="6d266-182">Bei der Anmeldung an einem bestimmten Profil sollte ein Client das Flag MAPI_NEW_SESSION in MAPILogonEx zusätzlich zu den Profilnamen übergeben.</span><span class="sxs-lookup"><span data-stu-id="6d266-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="6d266-183">Andernfalls, wenn ein anderer Client eine freigegebene Sitzung anmelden, auf mit MAPI_ALLOW_OTHERS hergestellt, wird der Client an der freigegebenen Sitzung anstatt auf das Profil angefordert angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="6d266-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="6d266-184">Das Flag MAPI_EXPLICIT_PROFILE nicht dazu führen, dass der Name verwendet werden, wenn _LpszProfileName_ NULL ist oder leer, wenn das Flag MAPI_USE_DEFAULT auch vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d266-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="6d266-185">Das Flag MAPI_NO_MAIL hat mehrere Effekte, die die folgenden verursachen, wenn die Warteschlange MAPI nicht verwenden:</span><span class="sxs-lookup"><span data-stu-id="6d266-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="6d266-186">Keine Nachrichten können gesendet oder durch die MAPI-Warteschlange diese Sitzung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d266-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="6d266-187">Nur eng gekoppelten Store und Transport-Provider können senden und Nachrichten übermitteln.</span><span class="sxs-lookup"><span data-stu-id="6d266-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="6d266-188">Serverbasierte Speicher möglicherweise noch senden oder Nachrichten übermitteln.</span><span class="sxs-lookup"><span data-stu-id="6d266-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="6d266-189">Nachrichten gesendet oder von Server-basierte Speicher bereitgestellt werden von Anbietern Hook nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6d266-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="6d266-190">Optionen für einzelne Nachrichten und pro Empfänger für Transporten sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d266-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="6d266-191">Die Statustabelle enthält keine Einträge für Transportanbieter für, und alle Transport-Funktionalität abhängig vom Status-Objekte (Konfiguration) ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d266-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="6d266-192">Die Nachricht Warteschlange Zeile in der Tabelle "Status" enthält den STATUS_FAILURE-Wert.</span><span class="sxs-lookup"><span data-stu-id="6d266-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="6d266-193">Anmeldungen Benachtichtigung sind zulässig, aber diese Anmeldungen führen nicht die vorherige Anmeldung Statusupdates-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d266-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="6d266-194">Ein Dienst sollte immer melden Sie sich mit dem MAPI_NO_MAIL-Flag.</span><span class="sxs-lookup"><span data-stu-id="6d266-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6d266-195">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6d266-195">MFCMAPI reference</span></span>

<span data-ttu-id="6d266-196">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6d266-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6d266-197">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6d266-197">**File**</span></span>|<span data-ttu-id="6d266-198">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6d266-198">**Function**</span></span>|<span data-ttu-id="6d266-199">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6d266-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d266-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="6d266-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="6d266-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6d266-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="6d266-202">MFCMAPI (engl.) verwendet die MAPILogonEx-Methode zur Anmeldung bei MAPI an.</span><span class="sxs-lookup"><span data-stu-id="6d266-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d266-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d266-203">See also</span></span>



[<span data-ttu-id="6d266-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="6d266-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="6d266-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="6d266-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="6d266-206">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6d266-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

