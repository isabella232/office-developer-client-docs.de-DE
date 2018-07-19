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
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792911"
---
# <a name="launchwizardentry"></a><span data-ttu-id="c53df-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="c53df-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="c53df-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c53df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c53df-105">Definiert eine Funktion, die die Anwendung-Profil-Assistent zum Hinzufügen von mindestens eine Nachricht-Diensten zu einem Profil gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c53df-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c53df-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c53df-106">Header file:</span></span>  <br/> |<span data-ttu-id="c53df-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="c53df-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="c53df-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="c53df-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c53df-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c53df-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c53df-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="c53df-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c53df-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="c53df-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="c53df-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c53df-112">Parameters</span></span>

 <span data-ttu-id="c53df-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="c53df-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="c53df-114">[in] Ein Handle für den Anrufer übergeordnetes Fenster.</span><span class="sxs-lookup"><span data-stu-id="c53df-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="c53df-115">Wenn der Aufrufer übergeordnetes Fenster nicht vorhanden ist, sollte der _hParentWnd_ -Parameter auf NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c53df-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="c53df-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c53df-116">_ulFlags_</span></span>
  
> <span data-ttu-id="c53df-117">[in] Bitmaske der Flags, die Optionen für den Assistenten-Profil angeben.</span><span class="sxs-lookup"><span data-stu-id="c53df-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="c53df-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c53df-118">The following flags can be set:</span></span>
    
<span data-ttu-id="c53df-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c53df-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="c53df-120">Der Profil-Assistent ist nur die Message-Dienste aufgeführt, die über den _LppszServiceNameToAdd_ -Parameter hinzufügen und zeigen auf der Seite für die Auswahl von Message-Dienste nicht.</span><span class="sxs-lookup"><span data-stu-id="c53df-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="c53df-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="c53df-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="c53df-122">Das zu erstellende Profil ist der erste für diese Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="c53df-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="c53df-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="c53df-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="c53df-124">Der Profil-Assistent-Seite für die Auswahl von Message Dienste sollte nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c53df-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="c53df-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="c53df-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="c53df-126">Der Profil-Assistent wurde von der Systemsteuerung Konfiguration Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="c53df-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="c53df-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="c53df-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="c53df-128">Nur die Dienstanbieter Konfigurationsdialogfelder angezeigt werden sollen, und der Profil-Assistent Seiten sollte nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c53df-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="c53df-129">Dieses Kennzeichen können nur festgelegt werden, wenn das Flag MAPI_PW_ADD_SERVICE_ONLY festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c53df-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="c53df-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="c53df-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="c53df-131">[in] Zeiger auf ein Array von Zeichenfolgen mit den Namen der Nachrichtendienste, die dem Profil hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c53df-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="c53df-132">Das Array muss mit einem NULL-Wert enden.</span><span class="sxs-lookup"><span data-stu-id="c53df-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="c53df-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="c53df-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="c53df-134">[in] Größe des Puffers, auf den durch den Parameter _LpszNewProfileName_ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c53df-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="c53df-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="c53df-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="c53df-136">[out] Zeiger auf einen Puffer vom Typ String, in dem die Funktion basierend auf **LAUNCHWIZARDENTRY** den Namen des erstellten Profils zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c53df-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c53df-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c53df-137">Return value</span></span>

<span data-ttu-id="c53df-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="c53df-138">S_OK</span></span> 
  
> <span data-ttu-id="c53df-139">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c53df-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c53df-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c53df-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c53df-141">Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c53df-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="c53df-142">Mögliche Werte Fehler beim Initialisieren des MAPI-Subsystems für den Benutzerprofildienst-Assistenten eingeschlossen, der Fehler beim Zugriff auf das Standardprofil und einen Fehler zurück, aus dem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c53df-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c53df-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c53df-143">Remarks</span></span>

<span data-ttu-id="c53df-144">Die MAPI-Implementierung der Funktion **LAUNCHWIZARDENTRY** Prototyp ist der Einstiegspunkt in die Anwendung MAPI-Profil-Assistent.</span><span class="sxs-lookup"><span data-stu-id="c53df-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="c53df-145">Den Namen dieser Einstiegspunkt **LaunchWizard**MAPI.</span><span class="sxs-lookup"><span data-stu-id="c53df-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="c53df-146">Wenn das Flag MAPI_PW_ADD_SERVICE_ONLY im _UlFlags_ -Parameter festgelegt ist, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="c53df-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="c53df-147">Das Flag MAPI_PW_LAUNCHED_BY_CONFIG unterdrückt die Seite Willkommen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c53df-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="c53df-148">Die Flags MAPI_PW_HIDE_SERVICES_LIST und MAPI_PW_PROVIDER_UI_ONLY eignen sich nur, wenn kein Standardprofil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c53df-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="c53df-149">In diesem Fall bestimmen diese Flags welche-Profil-Assistent Seite ist, angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c53df-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="c53df-150">Wenn ein Standardprofil vorhanden ist, werden keine der Profil-Assistent Seiten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c53df-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="c53df-151">Wenn ein Standardprofil vorhanden ist, wird nur eine Nachricht-Dienst über den Parameter _LppszServiceNameToAdd_ aufgeführt, und Messagingdiensts bereits im Standardprofil lautet, gibt der Profil-Assistent S_OK zurück, ohne das Profil nichts hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c53df-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="c53df-152">Für jeden Nachrichtendienst, die dem Profil hinzugefügt werden soll ruft der Profil-Assistent des Dienstes Eintrag Funktion basierend auf den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp.</span><span class="sxs-lookup"><span data-stu-id="c53df-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="c53df-153">Für jede Dienstanbieter ausgewählt aus einem Nachrichtendienst, die dem Profil hinzugefügt werden soll ruft der Profil-Assistent des Anbieters Eintrag Funktion basierend auf den [WIZARDENTRY](wizardentry.md) Prototyp.</span><span class="sxs-lookup"><span data-stu-id="c53df-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="c53df-154">Während der interaktiven Konfiguration bewirkt, dass jedes Benutzerereignis in die Eigenschaftenseiten Profil des Anbieters Callback-Funktion basierend auf den Prototyp [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c53df-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="c53df-155">Wenn ein Dienstanbieter, die dem Profil hinzugefügt wird die Seiten des Assistenten Profil unterstützt, müssen sie programmgesteuerte Konfiguration des Profils zulassen.</span><span class="sxs-lookup"><span data-stu-id="c53df-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

