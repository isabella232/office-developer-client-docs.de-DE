---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437385"
---
# <a name="launchwizardentry"></a><span data-ttu-id="b7e90-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="b7e90-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="b7e90-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7e90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7e90-105">Definiert eine Funktion, mit der die Anwendung des Profil-Assistenten gestartet wird, um einem Profil einen oder mehrere Nachrichtendienste hinzufügen zu können.</span><span class="sxs-lookup"><span data-stu-id="b7e90-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7e90-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b7e90-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7e90-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="b7e90-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="b7e90-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b7e90-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="b7e90-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7e90-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7e90-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="b7e90-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="b7e90-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="b7e90-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="b7e90-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7e90-112">Parameters</span></span>

 <span data-ttu-id="b7e90-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="b7e90-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="b7e90-114">[in] Ein Handle zum übergeordneten Fenster des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="b7e90-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="b7e90-115">Wenn der Aufrufer kein übergeordnetes Fenster hat, sollte  _der hParentWnd-Parameter_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b7e90-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="b7e90-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7e90-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b7e90-117">[in] Bitmaske mit Flags, die Optionen für den Profil-Assistenten angibt.</span><span class="sxs-lookup"><span data-stu-id="b7e90-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="b7e90-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b7e90-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b7e90-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b7e90-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="b7e90-120">Der Profil-Assistent fügt nur die Nachrichtendienste hinzu, die über den  _lppszServiceNameToAdd-Parameter_ aufgelistet sind, und nicht seine Seite zum Auswählen von Nachrichtendiensten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7e90-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="b7e90-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b7e90-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="b7e90-122">Das zu erstellende Profil ist das erste für diese Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="b7e90-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="b7e90-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="b7e90-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="b7e90-124">Die Seite des Profil-Assistenten zum Auswählen von Nachrichtendiensten sollte nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7e90-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="b7e90-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="b7e90-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="b7e90-126">Der Profil-Assistent wurde von der Systemsteuerungskonfigurationsanwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="b7e90-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="b7e90-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="b7e90-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="b7e90-128">Es sollten nur die Konfigurationsdialogfelder der Dienstanbieter angezeigt werden, und die Seiten des Profil-Assistenten sollten nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7e90-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="b7e90-129">Dieses Flag kann nur festgelegt werden, wenn MAPI_PW_ADD_SERVICE_ONLY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b7e90-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="b7e90-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="b7e90-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="b7e90-131">[in] Zeiger auf ein Array von Zeichenfolgen, das die Namen der Nachrichtendienste enthält, die dem Profil hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7e90-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="b7e90-132">Das Array muss mit einem NULL-Wert beendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7e90-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="b7e90-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="b7e90-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="b7e90-134">[in] Die Größe des Puffers, auf den der  _lpszNewProfileName-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="b7e90-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="b7e90-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="b7e90-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="b7e90-136">[out] Zeiger auf einen Zeichenfolgenpuffer, in dem die auf **LAUNCHWIZARDENTRY** basierende Funktion den Namen des erstellten Profils zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b7e90-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b7e90-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7e90-137">Return value</span></span>

<span data-ttu-id="b7e90-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7e90-138">S_OK</span></span> 
  
> <span data-ttu-id="b7e90-139">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b7e90-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b7e90-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b7e90-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b7e90-141">Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b7e90-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="b7e90-142">Zu den Möglichkeiten gehören das Nicht initialisieren des MAPI-Subsystems für den Profil-Assistenten, der Nichtzugriff auf das Standardprofil und eine Fehlerrückskehr aus dem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b7e90-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7e90-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7e90-143">Remarks</span></span>

<span data-ttu-id="b7e90-144">Die MAPI-Implementierung des **LAUNCHWIZARDENTRY-Funktionsprototyps** ist der Einstiegspunkt in die MAPI-Profil-Assistenten-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b7e90-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="b7e90-145">MAPI benennt diesen Einstiegspunkt **LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="b7e90-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="b7e90-146">Wenn das MAPI_PW_ADD_SERVICE_ONLY im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="b7e90-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="b7e90-147">Das MAPI_PW_LAUNCHED_BY_CONFIG verhindert, dass die Willkommensseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b7e90-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="b7e90-148">Die MAPI_PW_HIDE_SERVICES_LIST und MAPI_PW_PROVIDER_UI_ONLY sind nur nützlich, wenn kein Standardprofil vorlag.</span><span class="sxs-lookup"><span data-stu-id="b7e90-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="b7e90-149">In diesem Fall bestimmen diese Kennzeichen, welche Seite des Profil-Assistenten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7e90-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="b7e90-150">Wenn ein Standardprofil vorhanden ist, wird keine der Seiten des Profil-Assistenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7e90-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="b7e90-151">Wenn ein Standardprofil vorhanden ist, nur ein Nachrichtendienst über den  _lppszServiceNameToAdd-Parameter_ aufgelistet wird und sich dieser Nachrichtendienst bereits im Standardprofil befindet, gibt der Profil-Assistent S_OK zurück, ohne dem Profil etwas hinzufügen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b7e90-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="b7e90-152">Damit jeder Nachrichtendienst dem Profil hinzugefügt werden kann, ruft der Profil-Assistent die Einstiegspunktfunktion des Diensts basierend auf dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) auf.</span><span class="sxs-lookup"><span data-stu-id="b7e90-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="b7e90-153">Für jeden Dienstanbieter, der aus einem Nachrichtendienst ausgewählt wurde, der dem Profil hinzugefügt werden soll, ruft der Profil-Assistent die Einstiegspunktfunktion des Anbieters basierend auf dem [WIZARDENTRY-Prototyp](wizardentry.md) auf.</span><span class="sxs-lookup"><span data-stu-id="b7e90-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="b7e90-154">Während der interaktiven Konfiguration führt jedes Benutzerereignis auf den Eigenschaftenseiten dazu, dass der Profil-Assistent die Rückruffunktion des Anbieters basierend auf dem [SERVICEWIZARDDLGPROC-Prototyp](servicewizarddlgproc.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="b7e90-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="b7e90-155">Wenn ein Dienstanbieter, der dem Profil hinzugefügt wird, die Seiten des Profil-Assistenten unterstützt, muss er die programmgesteuerte Konfiguration des Profils zulassen.</span><span class="sxs-lookup"><span data-stu-id="b7e90-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

