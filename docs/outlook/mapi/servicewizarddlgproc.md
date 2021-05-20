---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432380"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="58b55-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="58b55-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="58b55-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58b55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58b55-105">Definiert eine Rückruffunktion, die vom Profil-Assistenten aufgerufen wird, damit ein Dienstanbieter auf Benutzerereignisse reagieren kann, wenn die Eigenschaftenblätter oder Seiten des Anbieters angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58b55-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58b55-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="58b55-106">Header file:</span></span>  <br/> |<span data-ttu-id="58b55-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="58b55-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="58b55-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="58b55-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="58b55-109">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="58b55-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="58b55-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="58b55-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="58b55-111">MAPI-Profil-Assistent</span><span class="sxs-lookup"><span data-stu-id="58b55-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="58b55-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="58b55-112">Parameters</span></span>

<span data-ttu-id="58b55-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="58b55-113">_hDlg_</span></span>
  
> <span data-ttu-id="58b55-114">[in] Fensterhandle zum Dialogfeld Profil-Assistent.</span><span class="sxs-lookup"><span data-stu-id="58b55-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="58b55-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="58b55-115">_wMsgID_</span></span>
  
> <span data-ttu-id="58b55-116">[in] Die zu verarbeitende Fensternachricht.</span><span class="sxs-lookup"><span data-stu-id="58b55-116">[in] The window message to be processed.</span></span> <span data-ttu-id="58b55-117">Zusätzlich zu den regulären Fenstermeldungen, die von einem modalen Dialogfeld erwartet werden, können die folgenden Nachrichten empfangen werden:</span><span class="sxs-lookup"><span data-stu-id="58b55-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="58b55-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="58b55-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="58b55-119">Der Profil-Assistent wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="58b55-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="58b55-120">Der Dienstanbieter sollte alle erforderlichen Bereinigungen, z. B. die Zuweisung eines dynamisch zugewiesenen Arbeitsspeichers, tun.</span><span class="sxs-lookup"><span data-stu-id="58b55-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="58b55-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="58b55-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="58b55-122">Eines der Steuerelemente des Anbieters wurde ausgewählt,  oder auf die **Schaltfläche Weiter** oder Zurück wurde geklickt.</span><span class="sxs-lookup"><span data-stu-id="58b55-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="58b55-123">Der Wert im  _wParam-Parameter_ gibt an, welches dieser Benutzerereignisse aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="58b55-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="58b55-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="58b55-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="58b55-125">Der Benutzer wurde zu einer anderen Eigenschaftenseite verschoben, für die das Dialogfeld initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="58b55-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="58b55-126">Der Anbieter sollte die Steuerelemente initialisieren, die der Profil-Assistent dem Dialogfeld hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="58b55-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="58b55-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="58b55-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="58b55-128">Der Profil-Assistent fordert die Anzahl der Seiten auf, die der Anbieter anzeigen muss.</span><span class="sxs-lookup"><span data-stu-id="58b55-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="58b55-129">Der Anbieter sollte die Anzahl der Seiten anstelle von TRUE oder FALSE zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="58b55-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="58b55-130">Verwenden Sie beispielsweise die folgende Return-Anweisung, um anzugeben, dass drei Seiten angezeigt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="58b55-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="58b55-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="58b55-131">_wParam_</span></span>
  
> <span data-ttu-id="58b55-132">[in] Ein 32-Bit-Parameter, der Fenstermeldungen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="58b55-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="58b55-133">Mögliche Werte hängen von der im  _wMsgID-Parameter angegebenen Nachricht_ ab.</span><span class="sxs-lookup"><span data-stu-id="58b55-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="58b55-134">Zusätzlich zu den werten, die mit den regulären Fenstermeldungen für ein modales Dialogfeld erwartet werden, können die folgenden Werte empfangen werden:</span><span class="sxs-lookup"><span data-stu-id="58b55-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="58b55-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="58b55-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="58b55-136">Wenn _wMsgID_ WM_COMMAND, hat der Benutzer auf die Schaltfläche **Weiter geklickt.**</span><span class="sxs-lookup"><span data-stu-id="58b55-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="58b55-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="58b55-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="58b55-138">Wenn _wMsgID_ WM_COMMAND, hat der Benutzer auf die Schaltfläche **Zurück geklickt.**</span><span class="sxs-lookup"><span data-stu-id="58b55-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="58b55-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="58b55-139">_lParam_</span></span>
  
> <span data-ttu-id="58b55-140">[in] Ein 32-Bit-Parameter, der Fenstermeldungen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="58b55-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="58b55-141">Mögliche Werte hängen von der im  _wMsgID-Parameter angegebenen Nachricht_ ab.</span><span class="sxs-lookup"><span data-stu-id="58b55-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="58b55-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58b55-142">Return value</span></span>

<span data-ttu-id="58b55-143">Der von einer **SERVICEWIZARDDLGPROC-basierten** Funktion zurückgegebene Wert hängt von der empfangenen Fensternachricht ab.</span><span class="sxs-lookup"><span data-stu-id="58b55-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="58b55-144">Beachten Sie insbesondere den außergewöhnlichen Rückgabewert für die WIZ_QUERYNUMPAGES Nachricht.</span><span class="sxs-lookup"><span data-stu-id="58b55-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="58b55-145">Die normalen Rückgabewerte sind:</span><span class="sxs-lookup"><span data-stu-id="58b55-145">The normal return values are:</span></span> 
  
<span data-ttu-id="58b55-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="58b55-146">TRUE</span></span> 
  
> <span data-ttu-id="58b55-147">Der Dienstanbieter hat die empfangene Fensternachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="58b55-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="58b55-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="58b55-148">FALSE</span></span> 
  
> <span data-ttu-id="58b55-149">Der Dienstanbieter hat die empfangene Fensternachricht nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="58b55-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58b55-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58b55-150">Remarks</span></span>

<span data-ttu-id="58b55-151">Wenn der Benutzer von einer Eigenschaftenseite zu einer anderen wechselt, ist der Anbieter dafür verantwortlich, die Steuerelemente der alten Seite zu ausblenden und die Steuerelemente für die nächste oder vorherige Seite zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="58b55-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="58b55-152">Wenn der Benutzer auf die **Schaltfläche Weiter** klickt, wird die **serviceWIZARDDLGPROC-basierte** Funktion mit der WM_COMMAND und WIZ_NEXT im  _wParam-Parameter_ aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="58b55-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="58b55-153">In den folgenden Schritten wird beschrieben, was zwischen dem Zeitpunkt, zu dem der Benutzer auf **Weiter** klickt, und dem Rendern der Konfigurationsseiten des ersten Anbieters geschieht.</span><span class="sxs-lookup"><span data-stu-id="58b55-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="58b55-154">Der Profil-Assistent blendet alle Steuerelemente aus, die sich im Fenster befinden.</span><span class="sxs-lookup"><span data-stu-id="58b55-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="58b55-155">Der Profil-Assistent fügt der Seite die ausgeblendeten Steuerelemente des Anbieters hinzu.</span><span class="sxs-lookup"><span data-stu-id="58b55-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="58b55-156">Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC** auf und sendet die WM_INITDIALOG, damit der Anbieter die Steuerelemente initialisieren kann.</span><span class="sxs-lookup"><span data-stu-id="58b55-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="58b55-157">Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC auf** und sendet WIZ_QUERYNUMPAGES Nachricht.</span><span class="sxs-lookup"><span data-stu-id="58b55-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="58b55-158">Der Anbieter gibt die Anzahl der Seiten zurück, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58b55-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="58b55-159">Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC** auf und sendet die WM_COMMAND-Nachricht, bei der der  _wParam-Parameter_ auf WIZ_NEXT oder WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="58b55-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="58b55-160">An diesem Punkt gibt der Anbieter entweder FALSE {error} zurück oder zeigt seine Steuerelemente an und gibt TRUE {success} zurück.</span><span class="sxs-lookup"><span data-stu-id="58b55-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="58b55-161">Wenn der Profil-Assistent ID_NEXT, wird die erste Seite des Anbieters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58b55-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="58b55-162">Wenn ID_PREV übergeben wird, wird die letzte Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58b55-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="58b55-163">Der Profil-Assistent ruft die **SERVICEWIZARDDLGPROC-Funktion** des Anbieters auf und sendet die WM_COMMAND-Nachricht mit dem  _wParam-Parameter,_ der auf WIZ_NEXT oder WIZ_PREV festgelegt ist (je nachdem, auf welche Schaltfläche der Benutzer geklickt hat).</span><span class="sxs-lookup"><span data-stu-id="58b55-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="58b55-164">Der Anbieter ist dafür verantwortlich, seine Steuerelemente ein- oder ausblenden und seine Daten in den **IMAPIProp** zu schreiben, der an den Profil-Assistenten übergeben wurde, um die Seitenabfolge zu durchblättern.</span><span class="sxs-lookup"><span data-stu-id="58b55-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="58b55-165">Der Anbieter sollte TRUE zurückgeben, wenn die nächste oder vorherige Seite erfolgreich angezeigt wurde, und FALSE, wenn weder die nächste noch die vorherige Seite angezeigt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="58b55-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="58b55-166">Der Anbieter muss sich bewusst sein, wann er außerhalb seiner Seitenabfolge tritt, und entsprechend reagieren, indem er seine Steuerelemente ausblenden und seine Daten in das Profil schreibt.</span><span class="sxs-lookup"><span data-stu-id="58b55-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="58b55-167">Wenn der Benutzer den Seitenbereich des Anbieters überschritt, löscht der Profil-Assistent die ausgeblendeten Steuerelemente des Anbieters aus dem Dialogfeld und ruft den nächsten Anbieter auf oder zeigt die nächste Seite an, wenn dies der letzte Anbieter war.</span><span class="sxs-lookup"><span data-stu-id="58b55-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

