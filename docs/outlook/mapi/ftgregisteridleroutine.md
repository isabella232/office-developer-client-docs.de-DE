---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418521"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="5a122-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5a122-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="5a122-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a122-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a122-105">Fügt dem MAPI-System eine funktionsbasierte Leerlaufroutine für [FNIDLE](fnidle.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="5a122-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a122-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5a122-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a122-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5a122-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5a122-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5a122-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a122-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5a122-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5a122-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5a122-110">Called by:</span></span>  <br/> |<span data-ttu-id="5a122-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5a122-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="5a122-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a122-112">Parameters</span></span>

<span data-ttu-id="5a122-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="5a122-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="5a122-114">[in] Ein Zeiger auf die Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="5a122-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="5a122-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="5a122-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="5a122-116">[in] Ein Zeiger auf einen Speicherblock, den das Leerlaufmodul als Parameter an die Leerlaufroutine übergeben soll, wenn es es aufruft.</span><span class="sxs-lookup"><span data-stu-id="5a122-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="5a122-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="5a122-117">_priIdle_</span></span>
  
> <span data-ttu-id="5a122-118">[in] Die anfängliche Priorität für die Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="5a122-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="5a122-119">Mögliche Prioritäten für implementierungsdefinierte Routinen sind größer oder kleiner als Null, aber nicht Null.</span><span class="sxs-lookup"><span data-stu-id="5a122-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="5a122-120">Die Nullpriorität ist für ein Benutzerereignis wie z. B. einen Mausklick oder eine WM_PAINT reserviert.</span><span class="sxs-lookup"><span data-stu-id="5a122-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="5a122-121">Prioritäten, die größer als Null sind, stellen Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der standardmäßigen Nachrichtenumpumpschleife Windows werden.</span><span class="sxs-lookup"><span data-stu-id="5a122-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="5a122-122">Prioritäten kleiner als Null stellen Leerlaufaufgaben dar, die nur während der Leerlaufzeit der Nachrichtenumpumpung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5a122-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="5a122-123">Beispiele für Prioritäten sind: 1 für die Vordergrundübermittlung, 2 für das Einfügen von Power-Edit-Zeichen und 3 für das Herunterladen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="5a122-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="5a122-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="5a122-124">_csecIdle_</span></span>
  
> <span data-ttu-id="5a122-125">[in] Der anfängliche Zeitwert in Hundertstel sekunden, der bei der Angabe von Routineparametern im Leerlauf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a122-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="5a122-126">Die Bedeutung des Anfänglichen Zeitwerts variiert, je nachdem, was im  _iroIdle-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="5a122-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="5a122-127">Die Bedeutung kann eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="5a122-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="5a122-128">Der Minimale Zeitraum der Untätigkeit des Benutzers, der verstreichen muss, bevor das MAPI-Leerlaufmodul die Leerlaufroutine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in  _iroIdle_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5a122-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="5a122-129">Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5a122-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="5a122-130">Das Mindestintervall zwischen Aufrufen der Leerlaufroutine, wenn das FIROINTERVAL-Flag in _iroIdle festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="5a122-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="5a122-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="5a122-131">_iroIdle_</span></span>
  
> <span data-ttu-id="5a122-132">[in] Die Bitmaske der Flags, mit der erste Optionen für die Leerlaufroutine festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a122-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="5a122-133">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5a122-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="5a122-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="5a122-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="5a122-135">Verwenden Sie dieses Flag, um anzugeben, dass der Leerlaufroutinentimer nicht für den Ruhezustand oder die Fortsetzung angepasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a122-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="5a122-136">Das Standardverhalten ohne dieses Flag ist, dass die Ruhezeit beim Berechnen der verstrichenen Zeit ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5a122-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="5a122-137">Wenn FIRONOADJUSTMENT übergeben wird, wird die Ruhezeit bei der Berechnung der verstrichenen Zeit einbezogen.</span><span class="sxs-lookup"><span data-stu-id="5a122-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="5a122-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="5a122-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="5a122-139">Die Leerlaufroutine sollte bei der Registrierung deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5a122-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="5a122-140">Die Standardaktion besteht in der Aktivierung der Leerlaufroutine, wenn **FtgRegisterIdleRoutine** sie registriert.</span><span class="sxs-lookup"><span data-stu-id="5a122-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="5a122-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="5a122-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="5a122-142">Die durch den  _csecIdle-Parameter_ angegebene Zeit ist das Mindestintervall zwischen aufeinander folgenden Aufrufen der Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="5a122-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="5a122-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="5a122-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="5a122-p107">Veraltet. Nicht verwenden. </span><span class="sxs-lookup"><span data-stu-id="5a122-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="5a122-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="5a122-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="5a122-p108">Veraltet. Nicht verwenden. </span><span class="sxs-lookup"><span data-stu-id="5a122-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="5a122-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="5a122-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="5a122-150">Die durch den  _csecIdle-Parameter_ angegebene Zeit ist der minimale Zeitraum der Untätigkeit des Benutzers, der verstreichen muss, bevor das #A0 die Leerlaufroutine zum ersten Mal aufruft.</span><span class="sxs-lookup"><span data-stu-id="5a122-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="5a122-151">Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5a122-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5a122-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a122-152">Return value</span></span>

<span data-ttu-id="5a122-153">Die **FtgRegisterIdleRoutine-Funktion** gibt ein Funktionstag zurück, das die Leerlaufroutine identifiziert, die dem MAPI-System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a122-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="5a122-154">Wenn **FtgRegisterIdleRoutine** die Leerlaufroutine für die Clientanwendung oder den Dienstanbieter nicht registrieren kann, z. B. aufgrund von Speicherproblemen, gibt es NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="5a122-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5a122-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a122-155">Remarks</span></span>

<span data-ttu-id="5a122-156">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren.</span><span class="sxs-lookup"><span data-stu-id="5a122-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="5a122-157">**Routinefunktion im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="5a122-157">**Idle routine function**</span></span>|<span data-ttu-id="5a122-158">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="5a122-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a122-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5a122-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="5a122-160">Ändert die Merkmale einer registrierten Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="5a122-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="5a122-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5a122-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="5a122-162">Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="5a122-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5a122-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5a122-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="5a122-164">Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5a122-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="5a122-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="5a122-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="5a122-166">Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="5a122-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="5a122-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="5a122-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="5a122-168">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5a122-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="5a122-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="5a122-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="5a122-170">Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5a122-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="5a122-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="5a122-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="5a122-172">Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a122-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="5a122-173">Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="5a122-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="5a122-174">Im Folgenden sehen Sie ein Beispiel für die Verwendung des FIRONOADJUSTMENT-Flag im _iroIdle-Parameter._</span><span class="sxs-lookup"><span data-stu-id="5a122-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="5a122-175">Registrieren Sie eine Leerlaufroutine mit einer Verzögerung von 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="5a122-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="5a122-176">Ruhezustand/Ruhezustand des Computers nach 1 Minute (4 Minuten im Timer).</span><span class="sxs-lookup"><span data-stu-id="5a122-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="5a122-177">Setzen Sie den Computer 10 Minuten später fort.</span><span class="sxs-lookup"><span data-stu-id="5a122-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="5a122-178">Das Standardverhalten ohne FIRONOADJUSTMENT ist, dass Sie noch 4 Minuten warten müssen, bis Ihre Routine ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a122-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="5a122-179">Das heißt, Der Timer wurde angepasst, um zu ermöglichen, wie lange der Computer geschlafen hat.</span><span class="sxs-lookup"><span data-stu-id="5a122-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="5a122-180">Wenn Sie FIRONOADJUSTMENT jedoch bestehen, wird Ihre Leerlaufroutine sofort ausgeführt, da mehr als 5 Minuten Echtzeit verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="5a122-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

