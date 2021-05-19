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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427878"
---
# <a name="msgserviceentry"></a><span data-ttu-id="c20e9-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c20e9-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="c20e9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c20e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c20e9-105">Definiert einen Prototyp für eine Nachrichtendienst-Einstiegspunktfunktion, um die Konfiguration des Nachrichtendiensts zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c20e9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c20e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="c20e9-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="c20e9-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="c20e9-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c20e9-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c20e9-109">Nachrichtendienste</span><span class="sxs-lookup"><span data-stu-id="c20e9-109">Message services</span></span>  <br/> |
|<span data-ttu-id="c20e9-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="c20e9-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c20e9-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="c20e9-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c20e9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c20e9-112">Parameters</span></span>

 <span data-ttu-id="c20e9-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="c20e9-113">_hInstance_</span></span>
  
> <span data-ttu-id="c20e9-114">[in] Handle der Instanz des DienstanbietersDLL.</span><span class="sxs-lookup"><span data-stu-id="c20e9-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="c20e9-115">Das Handle wird in der Regel zum Abrufen von Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c20e9-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="c20e9-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="c20e9-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="c20e9-117">[in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll.</span><span class="sxs-lookup"><span data-stu-id="c20e9-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="c20e9-118">Der Nachrichtendienst muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.**</span><span class="sxs-lookup"><span data-stu-id="c20e9-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="c20e9-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="c20e9-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="c20e9-120">[in] Zeiger auf eine [IMAPISupport : IUnknown-Schnittstellenimplementierung.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="c20e9-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="c20e9-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c20e9-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="c20e9-122">[in] Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion oder Null verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c20e9-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="c20e9-123">Der  _ulUIParam-Parameter_ ist das übergeordnete Fensterhandle für das Konfigurationsdialogfeld und hat den Typ HWND (in eine ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="c20e9-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="c20e9-124">Der Wert Null gibt an, dass es kein übergeordnetes Fenster gibt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="c20e9-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c20e9-125">_ulFlags_</span></span>
  
> <span data-ttu-id="c20e9-126">[in] Bitmaske mit Flags, die Optionen für die Diensteingabefunktion angibt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="c20e9-127">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c20e9-127">The following flags can be set:</span></span>
    
<span data-ttu-id="c20e9-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c20e9-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c20e9-129">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c20e9-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c20e9-130">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c20e9-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="c20e9-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="c20e9-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="c20e9-132">Die Benutzeroberfläche für die Konfiguration des Diensts sollte die aktuelle Konfiguration anzeigen, jedoch nicht zulassen, dass der Benutzer sie ändert.</span><span class="sxs-lookup"><span data-stu-id="c20e9-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="c20e9-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="c20e9-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="c20e9-134">Ermöglicht bei Bedarf das Anzeigen eines Konfigurationsdialogfelds.</span><span class="sxs-lookup"><span data-stu-id="c20e9-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="c20e9-135">Wenn das SERVICE_UI_ALLOWED festgelegt ist, sollte das Dialogfeld nur angezeigt werden, wenn das  _lpProps-Eigenschaftswertarray_ leer ist oder keine gültige Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="c20e9-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="c20e9-136">Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, wird möglicherweise weiterhin ein Dialogfeld angezeigt, wenn SERVICE_UI_ALWAYS festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c20e9-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="c20e9-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="c20e9-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="c20e9-138">Fordert an, dass das Konfigurationsdialogfeld für den aktiven Anbieter über anderen Dialogfelder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c20e9-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="c20e9-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="c20e9-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="c20e9-140">Der Nachrichtendienst muss ein Konfigurationsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="c20e9-141">Wenn das SERVICE_UI_ALWAYS nicht festgelegt ist, wird möglicherweise weiterhin ein Konfigurationsdialogfeld angezeigt, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und keine gültigen Konfigurationsinformationen im  _lpProps-Eigenschaftswertarray_ verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c20e9-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="c20e9-142">Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS müssen so festgelegt sein, dass eine Benutzeroberfläche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c20e9-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="c20e9-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="c20e9-143">_ulContext_</span></span>
  
> <span data-ttu-id="c20e9-144">[in] Der Konfigurationsvorgang, den MAPI derzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="c20e9-145">Der  _ulContext-Parameter_ enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c20e9-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="c20e9-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="c20e9-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="c20e9-147">Änderungen an der Konfiguration des Diensts sollten im Profil vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c20e9-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="c20e9-148">Wenn das SERVICE_UI_ALWAYS festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="c20e9-149">Das Dialogfeld sollte auch angezeigt werden, wenn das SERVICE_UI_ALLOWED festgelegt ist und der  _lpProps-Parameter_ leer ist oder keine gültigen Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="c20e9-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="c20e9-150">Wenn  _lpProps_ gültige Daten enthält, sollte kein Dialogfeld angezeigt werden, und der Dienst sollte diese Daten für die Konfigurationsänderung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c20e9-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="c20e9-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="c20e9-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="c20e9-152">Der Dienst wird einem Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-152">The service is being added to a profile.</span></span> <span data-ttu-id="c20e9-153">Wenn das SERVICE_UI_ALWAYS oder SERVICE_UI_ALLOWED festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="c20e9-154">Wenn keines der Kennzeichen festgelegt ist, sollte der Dienst fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="c20e9-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="c20e9-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="c20e9-156">Der Dienst wird aus einem Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-156">The service is being removed from a profile.</span></span> <span data-ttu-id="c20e9-157">Nachdem dieses Ereignis empfangen wurde, sollte der Dienst S_OK.</span><span class="sxs-lookup"><span data-stu-id="c20e9-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="c20e9-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="c20e9-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="c20e9-159">Der Dienst wurde auf der Arbeitsstation des Benutzers über ein Netzwerk, eine Diskette oder ein anderes externes Medium installiert.</span><span class="sxs-lookup"><span data-stu-id="c20e9-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="c20e9-160">Nach dem Empfang dieses Ereignisses gibt der Dienst in der Regel S_OK.</span><span class="sxs-lookup"><span data-stu-id="c20e9-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="c20e9-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="c20e9-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="c20e9-162">Fordert an, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="c20e9-163">Wenn der Dienst diesen Vorgang unterstützt, sollte [er IProviderAdmin::CreateProvider aufrufen.](iprovideradmin-createprovider.md)</span><span class="sxs-lookup"><span data-stu-id="c20e9-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="c20e9-164">Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c20e9-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="c20e9-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="c20e9-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="c20e9-166">Fordert an, dass der Dienst eine Anbieterinstanz löscht.</span><span class="sxs-lookup"><span data-stu-id="c20e9-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="c20e9-167">Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin::D eleteProvider aufrufen.](iprovideradmin-deleteprovider.md)</span><span class="sxs-lookup"><span data-stu-id="c20e9-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="c20e9-168">Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c20e9-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="c20e9-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="c20e9-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="c20e9-170">Der Dienst wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-170">The service is being removed.</span></span> <span data-ttu-id="c20e9-171">Nach dem Empfang dieses Ereignisses kann der Dienst alle Bereinigungsaufgaben ausführen, die vor dem Ende des Diensts ausgeführt werden sollten, und dann mit einem Erfolgswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c20e9-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="c20e9-172">Wenn der Benutzer die Entfernung abbricht, sollte der Dienst MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="c20e9-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="c20e9-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="c20e9-173">_cValues_</span></span>
  
> <span data-ttu-id="c20e9-174">[in] Anzahl der Eigenschaftswerte im Array, auf die der  _lpProps-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="c20e9-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="c20e9-175">Der Wert des  _cValues-Parameters_ ist null, wenn MAPI keine Eigenschaftswerte übergeben.</span><span class="sxs-lookup"><span data-stu-id="c20e9-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="c20e9-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="c20e9-176">_lpProps_</span></span>
  
> <span data-ttu-id="c20e9-177">[in] Zeiger auf ein optionales Array von [SPropValue-Strukturen,](spropvalue.md) das Werte für vom Anbieter unterstützte Eigenschaften angibt, die die Funktion beim Konfigurieren des Nachrichtendiensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="c20e9-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="c20e9-178">Die Funktion verwendet diesen Parameter nur, wenn  _der ulContext-Parameter_ auf MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="c20e9-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="c20e9-179">Dieser Parameter wird häufig verwendet, um den Pfad zu einer Datei für einen dateibasierten Dienst, z. B. einen persönlichen Adressbuchdienst, zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c20e9-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="c20e9-180">Wenn das MSG_SERVICE_CONFIGURE im  _ulFlags-Parameter_ nicht übergeben wird, muss  _der lpProps-Parameter_ null sein.</span><span class="sxs-lookup"><span data-stu-id="c20e9-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="c20e9-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="c20e9-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="c20e9-182">[in] Zeiger auf eine [IProviderAdmin:IUnknown-Schnittstelle,](iprovideradminiunknown.md) die die Funktion zum Suchen von Profilabschnitten für einen bestimmten Anbieter im aktuellen Nachrichtendienst verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="c20e9-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="c20e9-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="c20e9-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="c20e9-184">[out] Zeiger auf eine [MAPIERROR-Struktur.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="c20e9-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="c20e9-185">Die Struktur wird mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="c20e9-186">Alle Member sind optional, obwohl die meisten Strukturen eine gültige Fehlermeldungszeichenfolge im  _lpszError-Element_ enthalten.</span><span class="sxs-lookup"><span data-stu-id="c20e9-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="c20e9-187">Wenn  _die lpszComponent-_ oder  _lpszError-Elemente_ der Struktur vorhanden sind, muss ihr Arbeitsspeicher schließlich durch einen einzelnen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md) in der Basisstruktur frei werden.</span><span class="sxs-lookup"><span data-stu-id="c20e9-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c20e9-188">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c20e9-188">Return value</span></span>

<span data-ttu-id="c20e9-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="c20e9-189">S_OK</span></span> 
  
> <span data-ttu-id="c20e9-190">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c20e9-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c20e9-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="c20e9-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="c20e9-192">Der Dienstanbieter wurde nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c20e9-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="c20e9-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c20e9-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c20e9-194">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c20e9-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="c20e9-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c20e9-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c20e9-196">Der Anbieter unterstützt entweder keine Änderungen an seinen Objekten oder keine Benachrichtigung über Änderungen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="c20e9-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c20e9-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c20e9-198">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c20e9-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c20e9-199">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c20e9-199">Remarks</span></span>

<span data-ttu-id="c20e9-200">Eine funktion, die mithilfe des **MSGSERVICEENTRY-Funktionsprototyps** definiert wurde, ermöglicht Nachrichtendiensten, sich selbst zu konfigurieren oder andere dienstspezifische Aktionen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="c20e9-201">Die Funktion bietet in erster Linie ein Dialogfeld, in dem der Benutzer einstellungen speziell für den Nachrichtendienst ändern kann.</span><span class="sxs-lookup"><span data-stu-id="c20e9-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="c20e9-202">Sie kann auch die programmgesteuerte Konfiguration mithilfe des Eigenschaftswertarrays unterstützen, das im  _lpProps-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="c20e9-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="c20e9-203">Die programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst unterstützt den Profil-Assistenten, für den er erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c20e9-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="c20e9-204">MAPI ruft diesen Einstiegspunkt aus der Systemsteuerungsanwendung oder als Reaktion auf eine Clientanwendung auf, die [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin::ConfigureMsgService aufruft.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="c20e9-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="c20e9-205">MAPI legt keine Einschränkung auf den Funktionsnamen fest, den ein Nachrichtendienst für den **MSGSERVICEENTRY-Prototyp** verwendet, bevorzugt jedoch den Namen **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="c20e9-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="c20e9-206">Es gibt keine Einschränkung für die Ordnungszahl für die Funktion, und eine einzelne Anbieter-DLL kann mehrere Funktionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c20e9-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="c20e9-207">Allerdings kann nur eine der Funktionen den Namen **ServiceEntry haben.**</span><span class="sxs-lookup"><span data-stu-id="c20e9-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="c20e9-208">Ein Nachrichtendienst kann die [BuildDisplayTable-Funktion](builddisplaytable.md) und die [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) verwenden, um die Implementierung des Konfigurationsdialogfelds zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="c20e9-209">Ein Benutzer kann einen Vorgang MSG_SERVICE_UNINSTALL abbrechen.</span><span class="sxs-lookup"><span data-stu-id="c20e9-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="c20e9-210">In diesem Fall sollte die **ServiceEntry-Funktion** mit dem Benutzer überprüfen, ob der Dienst nicht entfernt werden soll, und MAPI_E_USER_CANCEL, wenn der Dienst installiert bleibt.</span><span class="sxs-lookup"><span data-stu-id="c20e9-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="c20e9-211">Eine Funktion, die auf dem **MSGSERVICEENTRY-Prototyp** basiert, gibt einen der aufgeführten HRESULT-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c20e9-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="c20e9-212">MAPI gibt diesen Wert weiter, wenn er auf den Aufruf eines Clients an [IMsgServiceAdmin::ConfigureMsgService reagiert.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="c20e9-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="c20e9-213">Nachrichtendienste, die eine Diensteintragsfunktion exportieren, müssen die **Eigenschaften PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) im Nachrichtendienstabschnitt von MAPISVC.INF enthalten.</span><span class="sxs-lookup"><span data-stu-id="c20e9-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

