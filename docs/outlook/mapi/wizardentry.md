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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2c307d18c5b62e5190aa10632a47a3f16b80e81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795849"
---
# <a name="wizardentry"></a><span data-ttu-id="510f3-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="510f3-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="510f3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="510f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="510f3-105">Definiert eine Funktion Service Provider Eintrag Punkt, der der Profil-Assistent zurückruft ausreichend Informationen zum Anzeigen des Anbieters Konfiguration-Eigenschaftenblätter abgerufen.</span><span class="sxs-lookup"><span data-stu-id="510f3-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="510f3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="510f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="510f3-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="510f3-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="510f3-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="510f3-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="510f3-109">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="510f3-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="510f3-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="510f3-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="510f3-111">MAPI-Profil-Assistent</span><span class="sxs-lookup"><span data-stu-id="510f3-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="510f3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="510f3-112">Parameters</span></span>

 <span data-ttu-id="510f3-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="510f3-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="510f3-114">[in] Instanzzugriffsnummer der DLL des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="510f3-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="510f3-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="510f3-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="510f3-116">[out] Zeiger auf eine Zeichenfolge, die den vollständigen Namen der die Ressource enthält, die während der Konfiguration von der Profil-Assistent angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="510f3-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="510f3-117">Die maximale Größe der Zeichenfolge, einschließlich der NULL-Terminator beträgt 32 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="510f3-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="510f3-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="510f3-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="510f3-119">[out] Zeiger auf eine standard Windows Dialogfeld Feld Prozedur, die mithilfe des Profil-Assistenten, um die Anbieter von verschiedenen Ereignisse benachrichtigen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="510f3-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="510f3-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="510f3-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="510f3-121">[in] Zeiger auf eine Implementierung der Eigenschaft-Schnittstelle, die Zugriff auf die Konfigurationseigenschaften bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="510f3-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="510f3-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="510f3-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="510f3-123">[in] Zeiger auf das Objekt der MAPI-Unterstützung für diese Sitzung gelten.</span><span class="sxs-lookup"><span data-stu-id="510f3-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="510f3-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="510f3-124">Return value</span></span>

<span data-ttu-id="510f3-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="510f3-125">S_OK</span></span> 
  
> <span data-ttu-id="510f3-126">Der Dienstanbieter **WIZARDENTRY** Funktion wurde erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="510f3-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="510f3-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="510f3-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="510f3-128">Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="510f3-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="510f3-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="510f3-129">Remarks</span></span>

<span data-ttu-id="510f3-130">Der Profil-Assistent Ruft die **WIZARDENTRY** Basis-Funktion, wenn der Dienstanbieter Konfigurationsbenutzeroberfläche anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="510f3-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="510f3-131">Nach Abschluss der Profil-Assistent alle Anbieter konfigurieren, werden die Konfigurationseigenschaften auf das Profil durch Aufrufen von [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)schreibt.</span><span class="sxs-lookup"><span data-stu-id="510f3-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="510f3-132">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="510f3-132">Notes to implementers</span></span>

<span data-ttu-id="510f3-133">Der Name der Funktion **WIZARDENTRY** basierend muss im Eintrag WIZARD_ENTRY_NAME MAPISVC.INF platziert werden.</span><span class="sxs-lookup"><span data-stu-id="510f3-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="510f3-134">Der Ressourcenname ist, der die Ressource, die im Bereich des Assistenten Profil gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="510f3-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="510f3-135">Die Ressource, die Back muss alle Seiten in einer einzelnen Ressource enthalten übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="510f3-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="510f3-136">Wenn der Profil-Assistent diese Ressource empfängt, wird das Dialogfeld Formatvorlage, aber nicht die Steuerelement-Formatvorlagen ignoriert, und alle Steuerelemente als untergeordnete Elemente des der Profil-Assistent-Seite erstellt.</span><span class="sxs-lookup"><span data-stu-id="510f3-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="510f3-137">Alle Steuerelemente sind anfangs ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="510f3-137">All controls are initially hidden.</span></span> <span data-ttu-id="510f3-138">Anbieter sollte stellen Sie sicher, dass die Koordinaten für die Steuerelemente auf 0 (null) sind oder nullbasierte und, dass sie eine maximale Breite von 200 Dialogfeld Einheiten und eine maximale Höhe von 150 Dialogfeld Einheiten nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="510f3-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="510f3-139">Steuerelement-IDs unter 400 sind für das Profil-Assistent reserviert.</span><span class="sxs-lookup"><span data-stu-id="510f3-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="510f3-140">Der Profil-Assistent des Anbieters Titel in Fettschrift oberhalb des Anbieters-Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="510f3-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="510f3-141">Eigenschaft Schnittstellenzeiger im _LpMAPIProp_ -Parameter sollte vom Anbieter für die zukünftige beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="510f3-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="510f3-142">Der Profil-Assistent befasst sich mit den grundlegenden Satz Eigenschaften, und der Anbieter kann die Implementierung der Eigenschaft-Schnittstelle verwenden, um zusätzliche Eigenschaften gehören.</span><span class="sxs-lookup"><span data-stu-id="510f3-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="510f3-143">Während der Konfiguration sollten Anbieter ihre Konfigurationseigenschaften auf das Objekt, das die Eigenschaft-Schnittstelle implementieren hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="510f3-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="510f3-144">Nachdem alle Anbieter konfiguriert wurden, fügt der Profil-Assistent diese Eigenschaften auf das Profil.</span><span class="sxs-lookup"><span data-stu-id="510f3-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="510f3-145">Weitere Informationen zu dieser Funktion finden Sie unter [Message-Dienstkonfiguration unterstützen](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="510f3-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

