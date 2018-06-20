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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 649046aa48f293caa5bd71cc670481b5c205459a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795514"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="c0746-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="c0746-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="c0746-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0746-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0746-105">Definiert eine Callback-Funktion aufgerufen, die vom Assistenten Profil zu einem Dienstanbieter reagieren auf Benutzerereignisse, wenn der Anbieters Eigenschaftenseiten oder Seiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0746-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0746-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c0746-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0746-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="c0746-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="c0746-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="c0746-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c0746-109">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c0746-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="c0746-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="c0746-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c0746-111">MAPI-Profil-Assistent</span><span class="sxs-lookup"><span data-stu-id="c0746-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="c0746-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0746-112">Parameters</span></span>

<span data-ttu-id="c0746-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="c0746-113">_hDlg_</span></span>
  
> <span data-ttu-id="c0746-114">[in] Fensterhandle an, das Dialogfeld-Profil-Assistent.</span><span class="sxs-lookup"><span data-stu-id="c0746-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="c0746-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="c0746-115">_wMsgID_</span></span>
  
> <span data-ttu-id="c0746-116">[in] Die Fensternachricht im verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c0746-116">[in] The window message to be processed.</span></span> <span data-ttu-id="c0746-117">Zusätzlich zu den regulären Fenster-Nachrichten von einem modalen Dialogfeld erwartet können die folgenden Nachrichten empfangen werden:</span><span class="sxs-lookup"><span data-stu-id="c0746-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="c0746-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="c0746-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="c0746-119">Der Profil-Assistent wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c0746-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="c0746-120">Der Dienstanbieter sollten alle Bereinigung tun, wie Speicher Aufheben der Zuweisung von einem dynamisch zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c0746-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="c0746-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="c0746-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="c0746-122">Eines der Steuerelemente des Anbieters ausgewählt wurde, oder die **nächsten** oder **zurück** -Schaltfläche geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="c0746-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="c0746-123">Der Wert in der _wParam_ -Parameter gibt an, welches dieser Benutzerereignisse eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c0746-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="c0746-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="c0746-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="c0746-125">Der Benutzer wurde an eine andere Eigenschaftenseite verschoben, für die das Dialogfeld initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c0746-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="c0746-126">Der Anbieter sollte die Steuerelemente initialisieren, die der Profil-Assistent zum Dialogfeld hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="c0746-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="c0746-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="c0746-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="c0746-128">Der Profil-Assistent ist für die Anzahl der Seiten aufgefordert werden, die zum Anzeigen der Anbieter benötigt.</span><span class="sxs-lookup"><span data-stu-id="c0746-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="c0746-129">Der Anbieter sollte die Anzahl der Seiten anstelle von TRUE oder FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0746-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="c0746-130">Verwenden Sie beispielsweise die folgenden return-Anweisung um anzugeben, dass drei Seiten angezeigt werden soll:</span><span class="sxs-lookup"><span data-stu-id="c0746-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="c0746-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="c0746-131">_wParam_</span></span>
  
> <span data-ttu-id="c0746-132">[in] Ein 32-Bit-Parameter Fenster-Nachrichten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0746-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="c0746-133">Mögliche Werte hängen von der in der _wMsgID_ -Parameter angegebenen Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="c0746-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="c0746-134">Zusätzlich zu den Werten, die mit den normalen Fenster-Nachrichten für ein modales Dialogfeld erwartet können die folgenden Werte erhalten:</span><span class="sxs-lookup"><span data-stu-id="c0746-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="c0746-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="c0746-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="c0746-136">Wenn _wMsgID_ WM_COMMAND enthält, hat der Benutzer die Schaltfläche **Weiter** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="c0746-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="c0746-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="c0746-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="c0746-138">Wenn _wMsgID_ WM_COMMAND enthält, hat der Benutzer durch Klicken auf die Schaltfläche **zurück** .</span><span class="sxs-lookup"><span data-stu-id="c0746-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="c0746-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="c0746-139">_lParam_</span></span>
  
> <span data-ttu-id="c0746-140">[in] Ein 32-Bit-Parameter Fenster-Nachrichten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0746-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="c0746-141">Mögliche Werte hängen von der in der _wMsgID_ -Parameter angegebenen Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="c0746-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0746-142">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c0746-142">Return value</span></span>

<span data-ttu-id="c0746-143">Der von einer **SERVICEWIZARDDLGPROC** Basis-Funktion zurückgegebene Wert ist die empfangene Meldung Fenster abhängig.</span><span class="sxs-lookup"><span data-stu-id="c0746-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="c0746-144">Beachten Sie insbesondere, dass die außergewöhnliche Wert für die Nachricht WIZ_QUERYNUMPAGES zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c0746-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="c0746-145">Normale zurückgegebenen Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c0746-145">The normal return values are:</span></span> 
  
<span data-ttu-id="c0746-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0746-146">TRUE</span></span> 
  
> <span data-ttu-id="c0746-147">Der Dienstanbieter hat die empfangene Meldung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c0746-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="c0746-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0746-148">FALSE</span></span> 
  
> <span data-ttu-id="c0746-149">Der Dienstanbieter noch die empfangene Meldung nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c0746-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0746-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0746-150">Remarks</span></span>

<span data-ttu-id="c0746-151">Wenn der Benutzer eine Eigenschaft auf der Seite zu einer anderen bewegt wird, ist der Anbieter für die alte Seite Steuerelemente ein- und Ausblenden von den Steuerelementen zum nächsten oder vorherigen Seite verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="c0746-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="c0746-152">Wenn der Benutzer auf die Schaltfläche **Weiter** klickt, wird die **SERVICEWIZARDDLGPROC** Basis-Funktion mit der WM_COMMAND-Meldung und WIZ_NEXT im _wParam_ -Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c0746-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="c0746-153">Die folgenden Schritte beschreiben, was geschieht, zwischen dem Zeitpunkt der Benutzer **Weiter** klickt und Zeitpunkt, zu dem der erste Anbieter Konfigurationsseiten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="c0746-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="c0746-154">Der Profil-Assistent werden alle Steuerelemente, die auf das Fenster sind ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="c0746-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="c0746-155">Der Profil-Assistent hinzugefügt die Seite des Anbieters ausgeblendete Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c0746-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="c0746-156">Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**, senden die Nachricht WM_INITDIALOG, damit der Anbieter die Steuerelemente initialisieren kann.</span><span class="sxs-lookup"><span data-stu-id="c0746-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="c0746-157">Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**, die WIZ_QUERYNUMPAGES-Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="c0746-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="c0746-158">Der Anbieter gibt die Anzahl der Seiten, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0746-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="c0746-159">Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**, senden die WM_COMMAND-Meldung mit dem _wParam_ -Parameter auf WIZ_NEXT oder WIZ_PREV festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0746-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="c0746-160">Zu diesem Zeitpunkt der Anbieter entweder gibt FALSE {Fehler} zurück oder zeigt dessen Steuerelemente und gibt TRUE zurück {Erfolg}.</span><span class="sxs-lookup"><span data-stu-id="c0746-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="c0746-161">Wenn der Profil-Assistent ID_NEXT übergibt, wird die erste Seite des Anbieters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0746-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="c0746-162">Wenn ID_PREV übergeben wird, wird die letzte Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0746-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="c0746-163">Der Profil-Assistent ruft der Anbieter **SERVICEWIZARDDLGPROC** Funktion senden die WM_COMMAND-Meldung mit dem _wParam_ -Parameter auf WIZ_NEXT oder WIZ_PREV (je nachdem, auf welche Schaltfläche der Benutzer geklickt hat) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0746-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="c0746-164">Der Anbieter ist verantwortlich für ein- oder Ausblenden von dessen Steuerelemente, und Schreiben von Daten in die **IMAPIProp** an der Profil-Assistent schrittweise durchlaufen ihrer Sequenz von Seiten übergeben.</span><span class="sxs-lookup"><span data-stu-id="c0746-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="c0746-165">Der Anbieter sollte TRUE zurück, wenn die nächste oder der vorherige Seite wurde erfolgreich angezeigt werden soll, und FALSE, wenn weder der nächsten oder vorherigen Seite angezeigt werden konnten.</span><span class="sxs-lookup"><span data-stu-id="c0746-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="c0746-166">Der Anbieter muss beachten, wenn sie außerhalb der Reihenfolge von Seiten Einzelschritt ist, und durch Ausblenden von dessen Steuerelemente und Schreiben von Daten auf das Profil entsprechend reagieren.</span><span class="sxs-lookup"><span data-stu-id="c0746-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="c0746-167">Wenn der Benutzer außerhalb des Anbieters Seitenbereich Schritte, löscht den Anbieter ausgeblendete Steuerelemente im Dialogfeld der Profil-Assistent und ruft den nächsten Anbieter oder die nächste Seite angezeigt, wenn das letzte Anbieter war.</span><span class="sxs-lookup"><span data-stu-id="c0746-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

