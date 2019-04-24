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
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346648"
---
# <a name="mapilogonex"></a><span data-ttu-id="3facd-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="3facd-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="3facd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3facd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3facd-105">Protokolliert eine Clientanwendung für eine Sitzung mit dem Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="3facd-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3facd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3facd-106">Header file:</span></span>  <br/> |<span data-ttu-id="3facd-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="3facd-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3facd-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3facd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3facd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3facd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3facd-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3facd-110">Called by:</span></span>  <br/> |<span data-ttu-id="3facd-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3facd-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="3facd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3facd-112">Parameters</span></span>

 <span data-ttu-id="3facd-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3facd-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="3facd-114">in Handle für das Fenster, in dem das Anmeldedialogfeld modal ist.</span><span class="sxs-lookup"><span data-stu-id="3facd-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="3facd-115">Wenn während des Anrufs kein Dialogfeld angezeigt wird, wird der _ulUIParam_ -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3facd-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="3facd-116">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3facd-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="3facd-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="3facd-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="3facd-118">in Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das bei der Anmeldung des Benutzers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3facd-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="3facd-119">Diese Zeichenfolge ist auf 64 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3facd-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="3facd-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="3facd-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="3facd-121">in Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält.</span><span class="sxs-lookup"><span data-stu-id="3facd-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="3facd-122">Der _lpszPassword_ -Parameter muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3facd-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="3facd-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="3facd-123">_flFlags_</span></span>
  
> <span data-ttu-id="3facd-124">in Bitmaske der Flags, die verwendet werden, um die Ausführung der Anmeldung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="3facd-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="3facd-125">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3facd-125">The following flags can be set:</span></span>
    
<span data-ttu-id="3facd-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="3facd-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="3facd-127">Die freigegebene Sitzung sollte zurückgegeben werden, sodass spätere Clients die Sitzung ohne Angabe von Benutzeranmeldeinformationen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="3facd-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="3facd-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="3facd-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="3facd-129">Melden Sie sich bei einer Sitzung an, und führen Sie alle Vorgänge im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="3facd-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="3facd-130">Wenn ein Client die Verarbeitung in einem Hintergrundthread oder in einem separaten Prozess auf eine Weise beabsichtigt, die unauffällig für den Vordergrundthread ist, sollte er im Allgemeinen mit dem MAPI_BG_SESSION-Flag aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3facd-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="3facd-131">Eine Clientanwendung wie ein Indizierungsmodul oder das Öffnen einer PST-Datei (Personal Folders) für den Hintergrundtyp Zugriff sind einige Beispiele dafür, wo MAPI_BG_SESSION verwendet werden soll. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="3facd-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="3facd-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="3facd-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="3facd-133">Das Standardprofil sollte nicht verwendet werden, und der Benutzer muss ein Profil angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="3facd-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="3facd-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="3facd-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="3facd-135">Melden Sie sich mit erweiterten Funktionen an.</span><span class="sxs-lookup"><span data-stu-id="3facd-135">Log on with extended capabilities.</span></span> <span data-ttu-id="3facd-136">Dieses Flag sollte immer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3facd-136">This flag should always be set.</span></span>
    
<span data-ttu-id="3facd-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="3facd-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="3facd-138">Es sollte versucht werden, alle Nachrichten des Benutzers herunterzuladen, bevor Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="3facd-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="3facd-139">Wenn das MAPI_FORCE_DOWNLOAD-Flag nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Aufruf von MAPILogonEx zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3facd-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="3facd-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="3facd-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="3facd-141">Es sollte ein Dialogfeld angezeigt werden, um den Benutzer bei Bedarf um Anmeldeinformationen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="3facd-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="3facd-142">Wenn das MAPI_LOGON_UI-Flag nicht festgelegt ist, zeigt der aufrufende Client kein Anmeldedialogfeld an und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="3facd-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="3facd-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="3facd-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="3facd-144">Es sollte versucht werden, eine neue MAPI-Sitzung zu erstellen, anstatt die freigegebene Sitzung zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="3facd-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="3facd-145">Wenn das MAPI_NEW_SESSION-Flag nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, auch wenn der _lpszprofileName_ -Parameter nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="3facd-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="3facd-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="3facd-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="3facd-147">MAPI sollte den MAPI-Spooler nicht über die Existenz der Sitzung informieren.</span><span class="sxs-lookup"><span data-stu-id="3facd-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="3facd-148">Das Ergebnis ist, dass keine Nachrichten in der Sitzung gesendet oder empfangen werden können, mit Ausnahme eines eng gekoppelten Speicher-und Transport Paars.</span><span class="sxs-lookup"><span data-stu-id="3facd-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="3facd-149">Ein aufrufende Client legt dieses Flag fest, wenn es als Agent fungiert, wenn Konfigurationsaufgaben ausgeführt werden müssen oder wenn der Client die verfügbaren Nachrichtenspeicher durchsucht.</span><span class="sxs-lookup"><span data-stu-id="3facd-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="3facd-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="3facd-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="3facd-151">Der Anrufer wird als Windows-Dienst gestartet.</span><span class="sxs-lookup"><span data-stu-id="3facd-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="3facd-152">Anrufer, die nicht als Windows-Dienst gestartet werden, sollten dieses Flag nicht festlegen; Aufrufer, die als Dienst gestartet werden, müssen dieses Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="3facd-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="3facd-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="3facd-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="3facd-154">MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3facd-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="3facd-155">Die Dialogfelder werden angezeigt, nachdem das Profil ausgewählt wurde, aber bevor ein Nachrichtendienst angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="3facd-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="3facd-156">Das allgemeine MAPI-Dialogfeld für die Anmeldung enthält auch ein Kontrollkästchen, das den gleichen Vorgang anfordert.</span><span class="sxs-lookup"><span data-stu-id="3facd-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="3facd-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="3facd-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="3facd-158">Die Anmeldung sollte fehlschlagen, wenn Sie für mehr als ein paar Sekunden gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="3facd-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="3facd-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3facd-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3facd-160">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="3facd-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="3facd-161">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="3facd-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="3facd-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3facd-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="3facd-163">Das Messaging Subsystem sollte den Profilnamen des Standardprofils des _lpszProfileName_ -Parameters ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3facd-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="3facd-164">Das MAPI_EXPLICIT_PROFILE-Flag wird ignoriert, es sei denn, _lpszProfileName_ ist NULL oder leer.</span><span class="sxs-lookup"><span data-stu-id="3facd-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="3facd-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="3facd-165">_lppSession_</span></span>
  
> <span data-ttu-id="3facd-166">Out Zeiger auf einen Zeiger auf die MAPI-Sitzungs Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3facd-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3facd-167">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3facd-167">Return value</span></span>

<span data-ttu-id="3facd-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="3facd-168">S_OK</span></span> 
  
> <span data-ttu-id="3facd-169">Die Anmeldung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3facd-169">The logon succeeded.</span></span>
    
<span data-ttu-id="3facd-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="3facd-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="3facd-171">Die Anmeldung war erfolglos, da mindestens einer der Parameter für MAPILogonEx ungültig war oder weil zu viele Sitzungen bereits geöffnet waren.</span><span class="sxs-lookup"><span data-stu-id="3facd-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="3facd-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3facd-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="3facd-173">MAPI serialisiert alle Anmeldungen über einen Mutex.</span><span class="sxs-lookup"><span data-stu-id="3facd-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="3facd-174">Dieser Wert wird zurückgegeben, wenn das MAPI_TIMEOUT_SHORT-Flag festgelegt wurde und ein anderer Thread den Mutex gehalten hat.</span><span class="sxs-lookup"><span data-stu-id="3facd-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="3facd-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="3facd-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="3facd-176">Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="3facd-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3facd-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3facd-177">Remarks</span></span>

<span data-ttu-id="3facd-178">MAPI-Clientanwendungen rufen die MAPILogonEx-Funktion auf, um sich bei einer Sitzung mit dem Messagingsystem anzumelden.</span><span class="sxs-lookup"><span data-stu-id="3facd-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="3facd-179">Alle Zeichenfolgen, die übergeben und an und von MAPI-Aufrufen zurückgegeben werden, werden mit Null beendet und müssen im aktuellen Zeichensatz oder der Codepage des Betriebssystems des aufrufenden Clients oder Anbieters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3facd-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="3facd-180">Der Parameter _lpszProfileName_ wird ignoriert, wenn eine frühere Sitzung mit dem Namen MapiLogonEx mit dem MAPI_ALLOW_OTHERS-Flag festgelegt ist und das Flag MAPI_NEW_SESSION nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3facd-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="3facd-181">Wenn der _lpszProfileName_ -Parameter NULL ist oder auf eine leere Zeichenfolge verweist und der Parameter _flFlags_ das MAPI_LOGON_UI-Flag enthält, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld mit einem leeren Feld für den Profilnamen.</span><span class="sxs-lookup"><span data-stu-id="3facd-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="3facd-182">Bei der Anmeldung an einem bestimmten Profil sollte ein Client das MAPI_NEW_SESSION-Flag zusätzlich zu dem Profilnamen an MAPILogonEx weitergeben.</span><span class="sxs-lookup"><span data-stu-id="3facd-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="3facd-183">Wenn ein anderer Client eine freigegebene Sitzung durch Anmelden bei MAPI_ALLOW_OTHERS erstellt hat, wird der Client bei der freigegebenen Sitzung anstelle des angeforderten Profils angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3facd-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="3facd-184">Das MAPI_EXPLICIT_PROFILE-Flag bewirkt nicht, dass der Standardprofilname verwendet wird, wenn _LPSZPROFILENAME_ NULL oder leer ist, es sei denn, das MAPI_USE_DEFAULT-Flag ist ebenfalls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3facd-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="3facd-185">Das MAPI_NO_MAIL-Flag weist mehrere Effekte auf, die Folgendes verursachen, wenn der MAPI-Spooler nicht verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="3facd-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="3facd-186">Während dieser Sitzung können keine Nachrichten vom MAPI-Spooler gesendet oder übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3facd-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="3facd-187">Nur eng gekoppelte Speicher-und Transportanbieter können Nachrichten senden und übermitteln.</span><span class="sxs-lookup"><span data-stu-id="3facd-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="3facd-188">Server basierte Speicher können weiterhin Nachrichten senden oder übermitteln.</span><span class="sxs-lookup"><span data-stu-id="3facd-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="3facd-189">Nachrichten, die von Server basierten Stores gesendet oder übermittelt werden, werden von keinem Hook-Anbieter verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3facd-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="3facd-190">Pro Nachricht und pro-Empfänger-Optionen für den Verkehr sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3facd-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="3facd-191">Die Statustabelle enthält keine Einträge für Transportanbieter, und alle Transportfunktionen, die von Statusobjekten (wie Konfiguration) abhängig sind, sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3facd-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="3facd-192">Die Zeile Nachrichtenwarteschlange in der Statustabelle enthält den STATUS_FAILURE-Wert.</span><span class="sxs-lookup"><span data-stu-id="3facd-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="3facd-193">Huckepack Anmeldungen sind zulässig, aber diese Anmeldungen führen nicht dazu, dass die vorherige Anmeldung Statusobjekt Aktualisierungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3facd-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="3facd-194">Ein Dienst sollte sich immer mit dem MAPI_NO_MAIL-Flag anmelden.</span><span class="sxs-lookup"><span data-stu-id="3facd-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3facd-195">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="3facd-195">MFCMAPI reference</span></span>

<span data-ttu-id="3facd-196">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3facd-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3facd-197">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3facd-197">**File**</span></span>|<span data-ttu-id="3facd-198">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3facd-198">**Function**</span></span>|<span data-ttu-id="3facd-199">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3facd-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3facd-200">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="3facd-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="3facd-201">CMapiObjects:: MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="3facd-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="3facd-202">MFCMAPI verwendet die MAPILogonEx-Methode, um sich bei MAPI anzumelden.</span><span class="sxs-lookup"><span data-stu-id="3facd-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3facd-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3facd-203">See also</span></span>



[<span data-ttu-id="3facd-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="3facd-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="3facd-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="3facd-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="3facd-206">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3facd-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

