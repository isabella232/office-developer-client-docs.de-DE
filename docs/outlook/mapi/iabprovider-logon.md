---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348783"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="0d837-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="0d837-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="0d837-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d837-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d837-105">Stellt eine Verbindung mit einer aktiven Sitzung her.</span><span class="sxs-lookup"><span data-stu-id="0d837-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="0d837-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d837-106">Parameters</span></span>

 <span data-ttu-id="0d837-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="0d837-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="0d837-108">in Ein Zeiger auf das Support Objekt des Adressbuch Anbieters.</span><span class="sxs-lookup"><span data-stu-id="0d837-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="0d837-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0d837-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="0d837-110">in Ein Handle für das übergeordnete Fenster für das Anmeldedialogfeld, das von der **Anmelde** Methode angezeigt wird, falls zulässig.</span><span class="sxs-lookup"><span data-stu-id="0d837-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="0d837-111">Der Parameter _ulUIParam_ enthält den Wert des Parameters mit demselben Namen, der an MAPI im vorherigen Aufruf der [MAPILogonEx](mapilogonex.md) -Funktion übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0d837-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="0d837-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="0d837-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="0d837-113">in Ein Zeiger auf den Namen des Sitzungs Profils.</span><span class="sxs-lookup"><span data-stu-id="0d837-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="0d837-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d837-114">_ulFlags_</span></span>
  
> <span data-ttu-id="0d837-115">in Eine Bitmaske von Flags, die die Ausführung der Anmeldung steuert.</span><span class="sxs-lookup"><span data-stu-id="0d837-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="0d837-116">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0d837-116">The following flags can be set:</span></span>
    
<span data-ttu-id="0d837-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0d837-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="0d837-118">Der Anbieter sollte während der Anmeldung kein Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d837-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="0d837-119">Wenn dieses Flag nicht festgelegt ist, kann der Anbieter ein Dialogfeld anzeigen, in dem der Benutzer nach fehlenden Konfigurationsinformationen gefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0d837-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="0d837-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0d837-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0d837-121">Ermöglicht die erfolgreiche Rückgabe der **Anmeldung** , bevor der Anmeldevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0d837-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="0d837-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d837-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0d837-123">Alle Zeichenfolgen sollten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="0d837-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="0d837-124">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format sein.</span><span class="sxs-lookup"><span data-stu-id="0d837-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="0d837-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="0d837-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="0d837-126">[in, out] Ein Zeiger auf die Größe der Sicherheitsanmeldeinformationen, auf die durch den _lppbSecurity_ -Parameter verwiesen wird, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0d837-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="0d837-127">Bei der Eingabe muss der Wert ungleich NULL sein. bei der Ausgabe muss der Wert NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0d837-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="0d837-128">In beiden Fällen müssen die Zeiger gültig sein.</span><span class="sxs-lookup"><span data-stu-id="0d837-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="0d837-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="0d837-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="0d837-130">[in, out] Ein Zeiger auf einen Zeiger auf Sicherheitsanmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0d837-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="0d837-131">Bei der Eingabe muss der Wert ungleich NULL sein. bei der Ausgabe muss der Wert NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0d837-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="0d837-132">In beiden Fällen muss der Zeiger gültig sein.</span><span class="sxs-lookup"><span data-stu-id="0d837-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="0d837-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0d837-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0d837-134">Out Ein Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0d837-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="0d837-135">Der _lppMAPIError_ -Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR** -Struktur zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d837-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="0d837-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="0d837-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="0d837-137">Out Ein Zeiger auf einen Zeiger auf das Anmeldeobjekt des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="0d837-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d837-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d837-138">Return value</span></span>

<span data-ttu-id="0d837-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d837-139">S_OK</span></span> 
  
> <span data-ttu-id="0d837-140">Eine Verbindung mit einer aktiven Sitzung wurde erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="0d837-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="0d837-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="0d837-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="0d837-142">Der Anbieter kann sich nicht anmelden, aber MAPI kann sich weiterhin bei den anderen Anbietern im Nachrichtendienst anmelden, zu dem der Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="0d837-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="0d837-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="0d837-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="0d837-144">Der Anbieter verfügt nicht über genügend Informationen, um die Anmeldung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0d837-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="0d837-145">MAPI Ruft die Nachrichtendienst-Eintrags Funktion des Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="0d837-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="0d837-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="0d837-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="0d837-147">Der Server ist nicht für die Unterstützung der Codeseite des Clients konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="0d837-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="0d837-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="0d837-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="0d837-149">Der Server ist nicht für die Unterstützung der Gebietsschemainformationen des Clients konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="0d837-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="0d837-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0d837-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0d837-151">Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im Anmeldedialogfeld geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="0d837-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0d837-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d837-152">Remarks</span></span>

<span data-ttu-id="0d837-153">Verbindungen werden mit jedem Adressbuchanbieter im Sitzungsprofil hergestellt, wenn ein Client die [IMAPISession:: openaddressbook](imapisession-openaddressbook.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="0d837-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="0d837-154">**Openaddressbook** ruft dann die **Anmelde** Methode jedes Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="0d837-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="0d837-155">Der Profilname, auf den durch den _lpszProfileName_ -Parameter verwiesen wird, wird im Zeichensatz des Clients des Benutzers angezeigt, der durch das vorhanden sein oder Fehlen des MAPI_UNICODE-Kennzeichens im _ulFlags_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d837-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0d837-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="0d837-156">Notes to implementers</span></span>

<span data-ttu-id="0d837-157">Rufen Sie in der Implementierung der **Anmelde** Methode die [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode auf, um einen eindeutigen Bezeichner oder eine [MAPIUID](mapiuid.md) -Struktur zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0d837-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="0d837-158">Jedes Objekt verfügt über eine Eintrags-ID, die diese **MAPIUID**enthält.</span><span class="sxs-lookup"><span data-stu-id="0d837-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="0d837-159">MAPI verwendet die **MAPIUID** , um ein Objekt mit seinem Anbieter abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="0d837-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="0d837-160">Wenn ein Client beispielsweise die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode aufruft, um einen Messagingbenutzer zu öffnen, unterSucht OpenEntry den \*\*\*\* **MAPIUID** -Teil des Eintrags Bezeichners, der übergeben wurde, und vergleicht ihn mit einem **MAPIUID** , der von einem registrierten Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="0d837-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="0d837-161">Wenn sich ein Client mehr als einmal bei Ihrem Anbieter anmeldet, können Sie für jede Anmeldung eine andere **MAPIUID** registrieren.</span><span class="sxs-lookup"><span data-stu-id="0d837-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="0d837-162">Das Registrieren eindeutiger **MAPIUID** -Strukturen ermöglicht MAPI das ordnungsgemäße Weiterleiten von Anforderungen an die entsprechende Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="0d837-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="0d837-163">Möglicherweise möchten Sie jedoch, dass jedes Logon-Objekt eine **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="0d837-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="0d837-164">In diesem Fall müssen Sie in der Lage sein, das Routing selbst zu behandeln, statt sich auf MAPI zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="0d837-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="0d837-165">Weitere Informationen zum Erstellen eines **MAPIUID**finden Sie unter Registrieren von [eindeutigen Bezeichnern des Dienstanbieters](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="0d837-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="0d837-166">Das Unterstützungsobjekt, das MAPI an Ihre **Anmelde** Methode im _lpMAPISup_ -Parameter übergibt, ermöglicht den Zugriff auf viele der Methoden, die in der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0d837-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="0d837-167">MAPI erstellt ein Support Objekt, das an den Anbietertyp angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="0d837-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="0d837-168">Wenn Sie sich beispielsweise bei einem zugrunde liegenden Messagingsystem oder Verzeichnisdienst anmelden müssen, wenn Sie Ihre Verbindung herstellen, können Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode aufrufen, um Sicherheitsanmeldeinformationen für diese bestimmte Anmeldesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d837-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="0d837-169">Wenn die **Anmeldung** erfolgreich ist, stellen Sie sicher, dass Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode des Support-Objekts aufrufen, um den Verweiszähler zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0d837-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="0d837-170">Auf diese Weise kann der Anbieter den Support Objektzeiger für den Rest der Sitzung aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="0d837-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="0d837-171">Wenn Sie diese **AddRef** -Methode nicht aufrufen, wird der Anbieter von MAPI entladen.</span><span class="sxs-lookup"><span data-stu-id="0d837-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="0d837-172">Sie können den im Parameter _lpszProfileName_ übergebenen Profilnamen in Fehler Dialogfeldern, Anmeldebildschirmen oder anderen Benutzeroberflächen angeben.</span><span class="sxs-lookup"><span data-stu-id="0d837-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="0d837-173">Um den Profilnamen zu verwenden, kopieren Sie ihn in den Speicher, den Sie zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="0d837-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="0d837-174">Erstellen Sie ein LOGON-Objekt, und geben Sie im _lppABLogon_ -Parameter einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="0d837-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="0d837-175">MAPI verwendet dieses Logon-Objekt, um Aufrufe der Methoden in der [IABLogon](iablogoniunknown.md) -Implementierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0d837-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="0d837-176">Wenn Sie während der Anmeldung ein Kennwort anfordern, zeigen Sie nur dann ein Anmeldedialogfeld an, wenn das AB_NO_DIALOG-Flag nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0d837-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="0d837-177">Wenn der Benutzer den Anmeldevorgang abbricht, indem er in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld MAPI_E_USER_CANCEL von der **Anmeldung**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d837-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="0d837-178">Wenn sich ein Adressbuchanbieter nicht anmelden kann, deaktiviert MAPI in der Regel den Nachrichtendienst, zu dem der fehlerhafte Anbieter gehört, d. h., MAPI versucht nicht, Verbindungen für andere Anbieter herzustellen, die für den Rest der Sitzung zum Dienst gehören. Leben.</span><span class="sxs-lookup"><span data-stu-id="0d837-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="0d837-179">Wenn Ihr Anbieter jedoch keine Verbindung herstellen kann und Sie den gesamten Dienst nicht deaktivieren möchten, geben Sie entweder MAPI_E_FAILONEPROVIDER oder MAPI_E_UNCONFIGURED zurück.</span><span class="sxs-lookup"><span data-stu-id="0d837-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="0d837-180">Der Nachrichtendienst, zu dem der Anbieter gehört, wird von MAPI nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0d837-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="0d837-181">Geben Sie MAPI_E_FAILONEPROVIDER zurück, wenn ein Fehler auftritt, der nicht schwer genug ist, um zu verhindern, dass die anderen Anbieter im Nachrichtendienst Verbindungen herstellen.</span><span class="sxs-lookup"><span data-stu-id="0d837-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="0d837-182">Geben Sie MAPI_E_UNCONFIGURED zurück, wenn die erforderlichen Konfigurationsinformationen im Profil fehlen, und Sie können kein Dialogfeld anzeigen, um den Benutzer aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="0d837-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="0d837-183">MAPI antwortet, indem er die Einstiegspunktfunktion des Anbieters für den Nachrichtendienst aufruft, wobei MSG_SERVICE_CONFIGURE als _ulContext_ -Parameter festgelegt ist, um dem Dienst die Möglichkeit zu geben, sich selbst programmgesteuert oder mithilfe eines Eigenschaftenblatts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0d837-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="0d837-184">Wenn die Nachrichtendienst-Einstiegspunktfunktion beendet wurde, versucht MAPI die Anmeldung erneut.</span><span class="sxs-lookup"><span data-stu-id="0d837-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d837-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d837-185">See also</span></span>



[<span data-ttu-id="0d837-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="0d837-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="0d837-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0d837-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="0d837-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0d837-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="0d837-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="0d837-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="0d837-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="0d837-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="0d837-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d837-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

