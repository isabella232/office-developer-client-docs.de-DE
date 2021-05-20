---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430679"
---
# <a name="wizardentry"></a><span data-ttu-id="eaa2c-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="eaa2c-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="eaa2c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaa2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaa2c-105">Definiert eine Einstiegspunktfunktion des Dienstanbieters, die vom Profil-Assistenten aufgerufen wird, um genügend Informationen zum Anzeigen der Konfigurationseigenschaftsblätter des Anbieters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eaa2c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="eaa2c-106">Header file:</span></span>  <br/> |<span data-ttu-id="eaa2c-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="eaa2c-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="eaa2c-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="eaa2c-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="eaa2c-109">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="eaa2c-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="eaa2c-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="eaa2c-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="eaa2c-111">MAPI-Profil-Assistent</span><span class="sxs-lookup"><span data-stu-id="eaa2c-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="eaa2c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaa2c-112">Parameters</span></span>

 <span data-ttu-id="eaa2c-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="eaa2c-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="eaa2c-114">[in] Instanzhandle der DLL des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="eaa2c-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="eaa2c-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="eaa2c-116">[out] Zeiger auf eine Zeichenfolge, die den vollständigen Namen der Dialogressource enthält, die während der Konfiguration vom Profil-Assistenten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="eaa2c-117">Die maximale Größe der Zeichenfolge, einschließlich des NULL-Abschlusszeichens, beträgt 32 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="eaa2c-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="eaa2c-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="eaa2c-119">[out] Zeiger auf eine standardmäßige Windows, die vom Profil-Assistenten aufgerufen wird, um den Anbieter über verschiedene Ereignisse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="eaa2c-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="eaa2c-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="eaa2c-121">[in] Zeiger auf eine Eigenschaftsschnittstellenimplementierung, die Zugriff auf die Konfigurationseigenschaften bietet.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="eaa2c-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="eaa2c-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="eaa2c-123">[in] Zeiger auf das MAPI-Unterstützungsobjekt, das für diese Sitzung gilt.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eaa2c-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaa2c-124">Return value</span></span>

<span data-ttu-id="eaa2c-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="eaa2c-125">S_OK</span></span> 
  
> <span data-ttu-id="eaa2c-126">Die **WIZARDENTRY-Funktion** des Dienstanbieters wurde erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="eaa2c-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="eaa2c-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="eaa2c-128">Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaa2c-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eaa2c-129">Remarks</span></span>

<span data-ttu-id="eaa2c-130">Der Profil-Assistent ruft die **WIZARDENTRY-basierte** Funktion auf, wenn die Konfigurationsbenutzerschnittstelle des Dienstanbieters angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="eaa2c-131">Wenn der Profil-Assistent alle Anbieter konfiguriert hat, schreibt er die Konfigurationseigenschaften in das Profil, indem er [IMsgServiceAdmin::ConfigureMsgService aufruft.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="eaa2c-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eaa2c-132">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="eaa2c-132">Notes to implementers</span></span>

<span data-ttu-id="eaa2c-133">Der Name der **WIZARDENTRY-basierten** Funktion muss im WIZARD_ENTRY_NAME MAPISVC.INF platziert werden.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="eaa2c-134">Der Ressourcenname ist der der Dialogfeldressource, die im Bereich des Profil-Assistenten gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="eaa2c-135">Die übergebene Ressource muss alle Seiten in einer einzelnen Dialogressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="eaa2c-136">Wenn der Profil-Assistent diese Ressource empfängt, ignoriert er die Dialogformatvorlage, aber nicht die Steuerelementformatvorlagen und erstellt alle Steuerelemente als untere Steuerelemente der Seite Profil-Assistent.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="eaa2c-137">Alle Steuerelemente werden zunächst ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-137">All controls are initially hidden.</span></span> <span data-ttu-id="eaa2c-138">Anbieter sollten sicherstellen, dass die Koordinaten für ihre Steuerelemente null- oder nullbasierte Sind und eine maximale Breite von 200 Dialogeinheiten und eine maximale Höhe von 150 Dialogeinheiten nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="eaa2c-139">Steuerelementbezeichner unter 400 sind für den Profil-Assistenten reserviert.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="eaa2c-140">Der Profil-Assistent zeigt den Titel des Anbieters in fett formatierten Text über der Benutzeroberfläche des Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="eaa2c-141">Der im  _lpMAPIProp-Parameter_ bereitgestellte Eigenschaftsschnittstellenzeiger sollte vom Anbieter für zukünftige Verweise beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="eaa2c-142">Der Profil-Assistent behandelt nur die grundlegendsten Eigenschaften, und der Anbieter kann die Implementierung der Eigenschaftenschnittstelle verwenden, um zusätzliche Eigenschaften zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="eaa2c-143">Während der Konfiguration sollten Anbieter dem Objekt, das die Eigenschaftsschnittstelle implementiert, ihre Konfigurationseigenschaften hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="eaa2c-144">Nachdem alle Anbieter konfiguriert wurden, fügt der Profil-Assistent diese Eigenschaften dem Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="eaa2c-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="eaa2c-145">Weitere Informationen zur Verwendung dieser Funktion finden Sie unter [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="eaa2c-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

