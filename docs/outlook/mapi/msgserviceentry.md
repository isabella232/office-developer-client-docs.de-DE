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
ms.openlocfilehash: 954609cbc62039c0d60874bde83fde50d1d11c30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591667"
---
# <a name="msgserviceentry"></a><span data-ttu-id="7da6a-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="7da6a-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="7da6a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7da6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7da6a-105">Definiert einen Prototyp für eine Nachricht Service-Einstiegspunkt zu Nachricht Dienstkonfiguration zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7da6a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7da6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7da6a-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="7da6a-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="7da6a-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="7da6a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="7da6a-109">Message-Dienste</span><span class="sxs-lookup"><span data-stu-id="7da6a-109">Message services</span></span>  <br/> |
|<span data-ttu-id="7da6a-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="7da6a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="7da6a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7da6a-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7da6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7da6a-112">Parameters</span></span>

 <span data-ttu-id="7da6a-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="7da6a-113">_hInstance_</span></span>
  
> <span data-ttu-id="7da6a-114">[in] Handle der Instanz von dem Dienst ProviderDLL.</span><span class="sxs-lookup"><span data-stu-id="7da6a-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="7da6a-115">Das Handle ist in der Regel verwendet, um Ressourcen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="7da6a-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="7da6a-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="7da6a-117">[in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="7da6a-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="7da6a-118">Message-Dienst müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="7da6a-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="7da6a-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="7da6a-120">[in] Zeiger auf eine [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle Implementierung.</span><span class="sxs-lookup"><span data-stu-id="7da6a-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="7da6a-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7da6a-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="7da6a-122">[in] Einen implementierungsspezifischen Wert für die Übergabe von Informationen zur Benutzeroberfläche für eine Funktion oder 0 (null) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7da6a-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="7da6a-123">Der Parameter _UlUIParam_ ist das übergeordnete Fensterhandle für das Dialogfeld Konfiguration und vom Typ HWND (Umwandlung in ein ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="7da6a-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="7da6a-124">Der Wert 0 gibt an, dass kein übergeordnetes Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7da6a-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="7da6a-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7da6a-125">_ulFlags_</span></span>
  
> <span data-ttu-id="7da6a-126">[in] Bitmaske aus Flags, die Optionen für die Funktion Eintrag angibt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="7da6a-127">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7da6a-127">The following flags can be set:</span></span>
    
<span data-ttu-id="7da6a-128">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7da6a-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7da6a-129">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7da6a-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7da6a-130">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7da6a-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="7da6a-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="7da6a-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="7da6a-132">Der Dienst Konfigurationsbenutzeroberfläche sollte zeigen Sie die aktuelle Konfiguration jedoch nicht durch den Benutzer zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7da6a-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="7da6a-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="7da6a-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="7da6a-134">Ermöglicht eine Konfigurationsdialogfeld, bei Bedarf angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7da6a-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="7da6a-135">Wenn das Flag SERVICE_UI_ALLOWED festgelegt ist, sollte das Dialogfeld werden nur angezeigt, wenn Wertearray der _LpProps_ -Eigenschaft leer ist oder enthält keine gültige Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7da6a-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="7da6a-136">Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, kann ein Dialogfeld weiterhin angezeigt werden, wenn das Flag SERVICE_UI_ALWAYS festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7da6a-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="7da6a-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="7da6a-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="7da6a-138">Fordert an, dass das Dialogfeld Konfiguration für den aktiven Anbieter über andere Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="7da6a-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="7da6a-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="7da6a-140">Erfordert den Dienst ein Konfigurationsdialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="7da6a-141">Wenn das Flag SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Konfigurationsdialogfeld weiterhin angezeigt werden, wenn das Flag SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen nicht verfügbar aus Wertearray _LpProps_ -Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="7da6a-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="7da6a-142">SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, um eine Benutzeroberfläche anzuzeigende zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="7da6a-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="7da6a-143">_ulContext_</span></span>
  
> <span data-ttu-id="7da6a-144">[in] Der Vorgang zur Konfiguration, mit dem MAPI derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7da6a-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="7da6a-145">Der Parameter _UlContext_ wird einer der folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="7da6a-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="7da6a-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="7da6a-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="7da6a-147">Konfiguration des Dienstes sollte im Profil geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="7da6a-148">Wenn das Flag SERVICE_UI_ALWAYS festgelegt ist, sollte der Dienst seine Konfigurationsdialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="7da6a-149">Das Dialogfeld sollte auch angezeigt werden, wenn das Flag SERVICE_UI_ALLOWED festgelegt ist und der Parameter _LpProps_ ist leer oder enthält keine gültigen Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="7da6a-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="7da6a-150">Wenn _LpProps_ gültige Daten enthält, kein Dialogfeld angezeigt werden soll, und der Dienst sollte diese Daten zur Erhebung von der Änderung der Konfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="7da6a-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="7da6a-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="7da6a-152">Der Dienst wird zu einem Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-152">The service is being added to a profile.</span></span> <span data-ttu-id="7da6a-153">Wenn die SERVICE_UI_ALWAYS oder SERVICE_UI_ALLOWED-Flag festgelegt ist, sollte der Dienst seine Konfigurationsdialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="7da6a-154">Wenn weder Flag festgelegt ist, sollte der Dienst fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="7da6a-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="7da6a-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="7da6a-156">Der Dienst wird aus einem Profil entfernt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-156">The service is being removed from a profile.</span></span> <span data-ttu-id="7da6a-157">Nach dem dieses Ereignis empfangen, sollte der Dienst S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7da6a-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="7da6a-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="7da6a-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="7da6a-159">Der Dienst wurde von einem Netzwerk, Diskette oder anderen externen Datenträger auf dem Computer des Benutzers installiert.</span><span class="sxs-lookup"><span data-stu-id="7da6a-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="7da6a-160">Wenn dieses Ereignis empfangen haben, gibt der Dienst in der Regel S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7da6a-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="7da6a-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="7da6a-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="7da6a-162">Fordert, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="7da6a-163">Wenn der Dienst diesen Vorgang unterstützt, sollten sie [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="7da6a-164">Wenn der Dienst diesen Vorgang nicht unterstützt, kann MAPI_E_NO_SUPPORT zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="7da6a-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="7da6a-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="7da6a-166">Fordert, dass der Dienst eine Anbieterinstanz löschen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="7da6a-167">Wenn der Dienst diesen Vorgang unterstützt, sollten sie [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="7da6a-168">Wenn der Dienst diesen Vorgang nicht unterstützt, kann MAPI_E_NO_SUPPORT zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="7da6a-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="7da6a-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="7da6a-170">Der Dienst wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-170">The service is being removed.</span></span> <span data-ttu-id="7da6a-171">Nach dem dieses Ereignis empfangen, kann der Dienst alle Cleanup Aufgaben, bei denen erfolgen soll, bevor der Dienst beendet, und klicken Sie dann mit einem Erfolgswert zurück.</span><span class="sxs-lookup"><span data-stu-id="7da6a-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="7da6a-172">Wenn der Benutzer die Entfernung abbricht, sollte der Dienst MAPI_E_USER_CANCEL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7da6a-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="7da6a-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7da6a-173">_cValues_</span></span>
  
> <span data-ttu-id="7da6a-174">[in] Anzahl der Eigenschaftswerte im Array auf den durch den Parameter _LpProps_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="7da6a-175">Der Wert des Parameters _cValues_ ist 0 (null), wenn MAPI keine Eigenschaftswerte übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7da6a-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="7da6a-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="7da6a-176">_lpProps_</span></span>
  
> <span data-ttu-id="7da6a-177">[in] Zeiger auf ein optionales Array von [SPropValue](spropvalue.md) Strukturen, der Werte für Anbieter unterstützten Eigenschaften, die die Funktion verwendet wird, konfigurieren Sie den Dienst.</span><span class="sxs-lookup"><span data-stu-id="7da6a-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="7da6a-178">Die Funktion verwendet diesen Parameter nur, wenn der Parameter _UlContext_ auf MSG_SERVICE_CONFIGURE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7da6a-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="7da6a-179">Dieser Parameter wird häufig zum übergeben Sie des Pfads für eine Datei-basierten Dienst, beispielsweise eine persönliche Adressbuchdienst in einer Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="7da6a-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="7da6a-180">Wenn das Flag MSG_SERVICE_CONFIGURE nicht in der _UlFlags_ -Parameter übergeben wird, muss der Parameter _LpProps_ 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7da6a-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="7da6a-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="7da6a-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="7da6a-182">[in] Zeiger auf eine [IProviderAdmin:IUnknown](iprovideradminiunknown.md) -Schnittstelle, die die Funktion zum Ermitteln von Abschnitten Profil für einen bestimmten Anbieter in der aktuellen Nachrichtendienst verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="7da6a-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="7da6a-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="7da6a-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="7da6a-184">[out] Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7da6a-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="7da6a-185">Die Struktur wird mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7da6a-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="7da6a-186">Alle Mitglieder sind optional, obwohl die meisten Strukturen auf eine Meldungszeichenfolge gültige Fehler im _LpszError_ -Member enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7da6a-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="7da6a-187">Wenn die _LpszComponent_ oder _LpszError_ Member der Struktur vorhanden sind, muss ihre Speicher schließlich durch einen einzigen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md) auf der Basis Struktur freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7da6a-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7da6a-188">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7da6a-188">Return value</span></span>

<span data-ttu-id="7da6a-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="7da6a-189">S_OK</span></span> 
  
> <span data-ttu-id="7da6a-190">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7da6a-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7da6a-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="7da6a-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="7da6a-192">Der Dienstanbieter wurde nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7da6a-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="7da6a-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7da6a-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7da6a-194">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="7da6a-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7da6a-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7da6a-196">Der Anbieter unterstützt keine Änderungen auf Objekte, oder Benachrichtigung über Änderungen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="7da6a-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7da6a-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7da6a-198">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="7da6a-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7da6a-199">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7da6a-199">Remarks</span></span>

<span data-ttu-id="7da6a-200">Eine Funktion, mit dem **MSGSERVICEENTRY** Funktionsprototyp definiert ermöglicht Message Dienste so konfigurieren Sie selbst oder andere dienstspezifische Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="7da6a-201">Die Funktion stellt bereit in erster Linie ein Dialogfeld, in dem der Benutzer den Dienst spezifischen Einstellungen ändern kann.</span><span class="sxs-lookup"><span data-stu-id="7da6a-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="7da6a-202">Sie können auch programmgesteuerte Konfiguration unterstützt werden mithilfe des im _LpProps_ -Parameter übergebenen Wertearrays-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7da6a-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="7da6a-203">Programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst der Profil-Assistent unterstützt, ist es erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7da6a-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="7da6a-204">MAPI-Aufrufen dieser Einstiegspunkt in der Systemsteuerung auf oder als Antwort auf eine Clientanwendung [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="7da6a-205">MAPI platziert keine Einschränkung auf den Funktionsnamen, dass eine Message Service für den **MSGSERVICEENTRY** Prototyp verwendet aber den Namen **ServiceEntry**bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="7da6a-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="7da6a-206">Es gibt keine Beschränkung für die Ordinal-Eigenschaft für die Funktion, und ein einzigen Anbieter DLL kann mehr als eine Funktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="7da6a-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="7da6a-207">Allerdings kann nur eine der Funktionen **ServiceEntry**heißen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="7da6a-208">Eine Message Service können die [BuildDisplayTable](builddisplaytable.md) -Funktion und die [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode Sie um Konfiguration Dialogfeld Feld Implementierung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="7da6a-209">Es ist möglich, dass ein Benutzer einen MSG_SERVICE_UNINSTALL-Vorgang abbrechen.</span><span class="sxs-lookup"><span data-stu-id="7da6a-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="7da6a-210">In diesem Fall sollten die **ServiceEntry** -Funktion überprüfen, mit dem Benutzer, um sicherzustellen, dass der Dienst sollte nicht entfernt werden und MAPI_E_USER_CANCEL zurückgeben, wenn der Dienst nicht deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="7da6a-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="7da6a-211">Eine Funktion, die basierend auf den **MSGSERVICEENTRY** Prototyp gibt eine der aufgeführten HRESULT-Werte.</span><span class="sxs-lookup"><span data-stu-id="7da6a-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="7da6a-212">MAPI weiterleitet diesen Wert, wenn die Antwort an einen Client Aufruf von [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="7da6a-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="7da6a-213">Message-Dienste, die eine Service-Eintrag-Funktion exportieren müssen die **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) Eigenschaften im Abschnitt Dienst Nachricht enthalten. MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="7da6a-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

