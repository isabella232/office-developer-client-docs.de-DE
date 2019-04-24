---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341608"
---
# <a name="msgserviceentry"></a><span data-ttu-id="7f48d-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="7f48d-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="7f48d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f48d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f48d-105">Definiert einen Prototyp für eine Nachrichtendienst-Einstiegspunktfunktion zur Unterstützung der Nachrichtendienst Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f48d-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f48d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7f48d-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f48d-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="7f48d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="7f48d-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7f48d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="7f48d-109">Nachrichtendienste</span><span class="sxs-lookup"><span data-stu-id="7f48d-109">Message services</span></span>  <br/> |
|<span data-ttu-id="7f48d-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7f48d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="7f48d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7f48d-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="7f48d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f48d-112">Parameters</span></span>

 <span data-ttu-id="7f48d-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="7f48d-113">_hInstance_</span></span>
  
> <span data-ttu-id="7f48d-114">in Handle der Instanz des Diensts providerDLL.</span><span class="sxs-lookup"><span data-stu-id="7f48d-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="7f48d-115">Das Handle wird in der Regel zum Abrufen von Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f48d-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="7f48d-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="7f48d-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="7f48d-117">in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="7f48d-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="7f48d-118">Möglicherweise muss der Nachrichtendienst diese Zuordnungsmethode beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f48d-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="7f48d-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="7f48d-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="7f48d-120">in Zeiger auf eine [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstellenimplementierung.</span><span class="sxs-lookup"><span data-stu-id="7f48d-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="7f48d-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7f48d-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="7f48d-122">in Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion oder NULL verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f48d-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="7f48d-123">Der _ulUIParam_ -Parameter ist das übergeordnete Fensterhandle für das Konfigurationsdialogfeld und vom Typ HWND (Umwandlung in einen ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="7f48d-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="7f48d-124">Der Wert 0 (null) gibt an, dass kein übergeordnetes Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7f48d-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="7f48d-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7f48d-125">_ulFlags_</span></span>
  
> <span data-ttu-id="7f48d-126">in Bitmaske von Flags, die Optionen für die Dienst Eingabefunktion angeben.</span><span class="sxs-lookup"><span data-stu-id="7f48d-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="7f48d-127">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7f48d-127">The following flags can be set:</span></span>
    
<span data-ttu-id="7f48d-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f48d-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7f48d-129">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7f48d-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7f48d-130">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7f48d-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="7f48d-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="7f48d-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="7f48d-132">Die Benutzeroberfläche der Konfiguration des Diensts sollte die aktuelle Konfiguration anzeigen, aber nicht zulassen, dass der Benutzer Sie ändern kann.</span><span class="sxs-lookup"><span data-stu-id="7f48d-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="7f48d-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="7f48d-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="7f48d-134">Ermöglicht bei Bedarf ein Konfigurationsdialogfeld.</span><span class="sxs-lookup"><span data-stu-id="7f48d-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="7f48d-135">Wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist, sollte das Dialogfeld nur angezeigt werden, wenn das _lpProps_ -Eigenschaftswert-Array leer ist oder keine gültige Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="7f48d-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="7f48d-136">Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, wird möglicherweise weiterhin ein Dialogfeld angezeigt, wenn das SERVICE_UI_ALWAYS-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7f48d-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="7f48d-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="7f48d-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="7f48d-138">Fordert, dass das Konfigurationsdialogfeld für den aktiven Anbieter über den anderen Dialogfeldern angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7f48d-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="7f48d-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7f48d-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="7f48d-140">Erfordert, dass der Nachrichtendienst ein Konfigurationsdialogfeld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="7f48d-141">Wenn das SERVICE_UI_ALWAYS-Flag nicht festgelegt ist, wird möglicherweise weiterhin ein Konfigurationsdialogfeld angezeigt, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und gültige Konfigurationsinformationen aus dem _lpProps_ -Eigenschaftswert Array nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7f48d-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="7f48d-142">Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, damit eine Benutzeroberfläche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f48d-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="7f48d-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="7f48d-143">_ulContext_</span></span>
  
> <span data-ttu-id="7f48d-144">in Der Konfigurationsvorgang, den MAPI derzeit ausführt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="7f48d-145">Der _ulContext_ -Parameter enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="7f48d-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="7f48d-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="7f48d-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="7f48d-147">Änderungen an der Konfiguration des Diensts sollten im Profil vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="7f48d-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="7f48d-148">Wenn das SERVICE_UI_ALWAYS-Flag festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="7f48d-149">Das Dialogfeld sollte auch angezeigt werden, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und der Parameter _lpProps_ leer ist oder keine gültigen Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7f48d-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="7f48d-150">Wenn _lpProps_ gültige Daten enthält, sollte kein Dialogfeld angezeigt werden, und der Dienst sollte diese Daten zum vornehmen der Konfigurationsänderung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f48d-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="7f48d-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="7f48d-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="7f48d-152">Der Dienst wird einem Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-152">The service is being added to a profile.</span></span> <span data-ttu-id="7f48d-153">Wenn entweder das SERVICE_UI_ALWAYS-oder das SERVICE_UI_ALLOWED-Flag festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="7f48d-154">Wenn kein Flag festgelegt ist, sollte der Dienst einen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="7f48d-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="7f48d-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="7f48d-156">Der Dienst wird aus einem Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-156">The service is being removed from a profile.</span></span> <span data-ttu-id="7f48d-157">Nach dem Empfang dieses Ereignisses sollte der Dienst S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7f48d-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="7f48d-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="7f48d-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="7f48d-159">Der Dienst wurde von einem Netzwerk, einer Diskette oder einem anderen externen Medium auf der Arbeitsstation des Benutzers installiert.</span><span class="sxs-lookup"><span data-stu-id="7f48d-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="7f48d-160">Nach dem Empfang dieses Ereignisses gibt der Dienst in der Regel S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7f48d-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="7f48d-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="7f48d-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="7f48d-162">Fordert, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="7f48d-163">Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="7f48d-164">Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7f48d-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="7f48d-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="7f48d-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="7f48d-166">Fordert, dass der Dienst eine Anbieterinstanz löscht.</span><span class="sxs-lookup"><span data-stu-id="7f48d-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="7f48d-167">Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="7f48d-168">Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7f48d-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="7f48d-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="7f48d-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="7f48d-170">Der Dienst wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-170">The service is being removed.</span></span> <span data-ttu-id="7f48d-171">Nach dem Empfang dieses Ereignisses kann der Dienst alle Bereinigungsaufgaben ausführen, die vor dem Beenden des Diensts ausgeführt werden sollten und dann mit einem Erfolgswert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f48d-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="7f48d-172">Wenn der Benutzer das Entfernen abbricht, sollte der Dienst MAPI_E_USER_CANCEL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7f48d-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="7f48d-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7f48d-173">_cValues_</span></span>
  
> <span data-ttu-id="7f48d-174">in Die Anzahl der Eigenschaftswerte im Array, auf die durch den _lpProps_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7f48d-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="7f48d-175">Der Wert des _cValues_ -Parameters ist NULL, wenn MAPI keine Eigenschaftswerte übergibt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="7f48d-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="7f48d-176">_lpProps_</span></span>
  
> <span data-ttu-id="7f48d-177">in Zeiger auf ein optionales Array von [SPropValue](spropvalue.md) -Strukturen, die Werte für Anbieter gestützte Eigenschaften angeben, die die Funktion beim Konfigurieren des Nachrichtendiensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f48d-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="7f48d-178">Die Funktion verwendet diesen Parameter nur, wenn der _ulContext_ -Parameter auf MSG_SERVICE_CONFIGURE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7f48d-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="7f48d-179">Dieser Parameter wird in der Regel verwendet, um den Pfad an eine Datei für einen dateibasierten Dienst, beispielsweise einen persönlichen Adressbuchdienst, zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="7f48d-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="7f48d-180">Wenn das MSG_SERVICE_CONFIGURE-Flag nicht im _ulFlags_ -Parameter übergeben wird, muss der _lpProps_ -Parameter NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7f48d-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="7f48d-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="7f48d-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="7f48d-182">in Zeiger auf eine [IProviderAdmin: IUnknown](iprovideradminiunknown.md) -Schnittstelle, die die Funktion verwenden kann, um Profilabschnitte für einen bestimmten Anbieter im aktuellen Nachrichtendienst zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="7f48d-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="7f48d-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="7f48d-184">Out Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7f48d-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="7f48d-185">Die Struktur wird mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7f48d-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="7f48d-186">Alle Member sind optional, obwohl die meisten Strukturen eine gültige Fehlermeldungszeichenfolge im _lpszError_ -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="7f48d-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="7f48d-187">Wenn die _lpszComponent_ -oder _lpszError_ -Member der Struktur vorhanden sind, muss Ihr Arbeitsspeicher schließlich durch einen einzelnen Aufruf von [mapifreebufferfreigegeben](mapifreebuffer.md) in der Basisstruktur freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f48d-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7f48d-188">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f48d-188">Return value</span></span>

<span data-ttu-id="7f48d-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f48d-189">S_OK</span></span> 
  
> <span data-ttu-id="7f48d-190">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7f48d-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7f48d-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="7f48d-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="7f48d-192">Der Dienstanbieter wurde nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7f48d-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="7f48d-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7f48d-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7f48d-194">Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="7f48d-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="7f48d-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7f48d-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7f48d-196">Der Anbieter unterstützt entweder keine Änderungen an seinen Objekten oder unterstützt keine Benachrichtigung über Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="7f48d-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7f48d-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7f48d-198">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="7f48d-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f48d-199">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f48d-199">Remarks</span></span>

<span data-ttu-id="7f48d-200">Eine mit dem **MSGSERVICEENTRY** -Funktionsprototyp definierte Funktion ermöglicht es Nachrichtendiensten, sich selbst zu konfigurieren oder andere dienstspezifische Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="7f48d-201">Die Funktion liefert in erster Linie ein Dialogfeld, in dem der Benutzer die Einstellungen für den Nachrichtendienst ändern kann.</span><span class="sxs-lookup"><span data-stu-id="7f48d-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="7f48d-202">Die programmgesteuerte Konfiguration kann auch mithilfe des Eigenschafts Wertarrays unterstützt werden, das im _lpProps_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f48d-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="7f48d-203">Die programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst unterstützt den Profil-Assistenten, für den er erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7f48d-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="7f48d-204">MAPI ruft diesen Einstiegspunkt aus der Systemsteuerungsanwendung oder als Reaktion auf eine Clientanwendung auf, die [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="7f48d-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="7f48d-205">MAPI gibt keine Einschränkung für den Funktionsnamen, den ein Nachrichtendienst für den **MSGSERVICEENTRY** -Prototyp verwendet, aber bevorzugt den Namen **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="7f48d-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="7f48d-206">Es gibt keine Beschränkung für die Ordnungszahl für die Funktion, und eine einzelne Anbieter-DLL kann mehr als eine Funktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="7f48d-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="7f48d-207">Es kann jedoch nur eine der Funktionen mit dem Namen **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="7f48d-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="7f48d-208">Ein Nachrichtendienst kann die [BuildDisplayTable](builddisplaytable.md) -Funktion und die [IMAPISupport::D-oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode verwenden, um die Implementierung der Konfigurationsdialogfelder zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="7f48d-209">Ein Benutzer kann einen MSG_SERVICE_UNINSTALL-Vorgang abbrechen.</span><span class="sxs-lookup"><span data-stu-id="7f48d-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="7f48d-210">In diesem Fall sollte die **ServiceEntry** -Funktion mit dem Benutzer überprüfen, ob der Dienst nicht entfernt werden soll, und MAPI_E_USER_CANCEL zurückgeben, wenn der Dienst installiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="7f48d-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="7f48d-211">Eine auf dem **MSGSERVICEENTRY** -Prototyp basierende Funktion gibt einen der aufgeführten HRESULT-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7f48d-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="7f48d-212">MAPI leitet diesen Wert weiter, wenn er auf den Aufruf eines Clients an [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)reagiert.</span><span class="sxs-lookup"><span data-stu-id="7f48d-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="7f48d-213">Nachrichtendienste, die eine Diensteintrags Funktion exportieren, müssen die Eigenschaften **PR_SERVICE_DLL_NAME** ([Pidtagservicedllname (](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md)) im Abschnitt Nachrichtendienst MAPISVC. INF.</span><span class="sxs-lookup"><span data-stu-id="7f48d-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

