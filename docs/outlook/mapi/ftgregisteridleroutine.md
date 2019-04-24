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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327993"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="9c2f7-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9c2f7-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="9c2f7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c2f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c2f7-105">Fügt dem MAPI-System eine [FNIDLE](fnidle.md) -funktionsbasierte Leerlauf Routine hinzu.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c2f7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9c2f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c2f7-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="9c2f7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9c2f7-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9c2f7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9c2f7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9c2f7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9c2f7-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9c2f7-110">Called by:</span></span>  <br/> |<span data-ttu-id="9c2f7-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9c2f7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="9c2f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c2f7-112">Parameters</span></span>

<span data-ttu-id="9c2f7-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="9c2f7-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="9c2f7-114">in Ein Zeiger auf die Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="9c2f7-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="9c2f7-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="9c2f7-116">in Ein Zeiger auf einen Speicherblock, der vom Leerlauf Modul als Parameter an die Leerlauf Routine übergeben werden soll, wenn diese aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="9c2f7-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="9c2f7-117">_priIdle_</span></span>
  
> <span data-ttu-id="9c2f7-118">in Die anfängliche Priorität für die Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="9c2f7-119">Mögliche Prioritäten für Implementierungs definierte Routinen sind größer oder kleiner als 0 (null), jedoch nicht NULL.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="9c2f7-120">Die NULL-Priorität ist für ein Benutzerereignis wie einen Mausklick oder eine WM_PAINT-Nachricht reserviert.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="9c2f7-121">Prioritäten, die größer als NULL sind, stellen Hintergrundvorgänge dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der standardmäßigen Windows-Nachrichten Pumpen Schleife gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="9c2f7-122">Prioritäten unter Null stellen Leerlauf Vorgänge dar, die nur während der Nachrichten Pumpen-Leerlaufzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="9c2f7-123">Es folgen Beispiele für Prioritäten: 1 für die Vordergrund Übermittlung, 2 für das Einfügen von Power-Edit-Zeichen und 3 zum Herunterladen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="9c2f7-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="9c2f7-124">_csecIdle_</span></span>
  
> <span data-ttu-id="9c2f7-125">in Der anfängliche Zeitwert in Hundertstel Sekunden, der bei der Angabe von Leerlauf Routine Parametern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="9c2f7-126">Die Bedeutung des anfänglichen Time-Werts variiert je nachdem, was im _iroIdle_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="9c2f7-127">Die Bedeutung kann eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="9c2f7-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="9c2f7-128">Der minimale Zeitraum der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in _iroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="9c2f7-129">Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="9c2f7-130">Das minimale Intervall zwischen Aufrufen der Leerlauf Routine, wenn das FIROINTERVAL-Flag in _iroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="9c2f7-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="9c2f7-131">_iroIdle_</span></span>
  
> <span data-ttu-id="9c2f7-132">in Die Bitmaske der Flags, die zum Festlegen der anfänglichen Optionen für die Leerlauf Routine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="9c2f7-133">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9c2f7-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="9c2f7-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="9c2f7-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="9c2f7-135">Verwenden Sie dieses Flag, um anzugeben, dass der Zeitgeber für die Leerlauf Routine nicht für den Standbymodus oder den Lebenslauf angepasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="9c2f7-136">Das Standardverhalten ohne dieses Flag besteht darin, dass die Sleep-Zeit beim Berechnen der verstrichenen Zeit ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="9c2f7-137">Wenn FIRONOADJUSTMENT übergeben wird, wird die Zeit beim Berechnen der verstrichenen Zeit berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="9c2f7-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="9c2f7-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="9c2f7-139">Die Leerlauf Routine sollte bei der Registrierung deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="9c2f7-140">Die Standardaktion besteht darin, die Leerlauf Routine zu aktivieren, wenn Sie von **FtgRegisterIdleRoutine** registriert wird.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="9c2f7-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="9c2f7-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="9c2f7-142">Die vom _csecIdle_ -Parameter angegebene Zeit ist das Mindestintervall zwischen aufeinanderfolgenden Aufrufen der Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="9c2f7-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="9c2f7-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="9c2f7-144">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-144">Obsolete.</span></span> <span data-ttu-id="9c2f7-145">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-145">Do not use.</span></span> 
      
  <span data-ttu-id="9c2f7-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="9c2f7-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="9c2f7-147">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-147">Obsolete.</span></span> <span data-ttu-id="9c2f7-148">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-148">Do not use.</span></span> 
      
  <span data-ttu-id="9c2f7-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="9c2f7-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="9c2f7-150">Die vom _csecIdle_ -Parameter angegebene Zeit ist die Mindestdauer der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="9c2f7-151">Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9c2f7-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c2f7-152">Return value</span></span>

<span data-ttu-id="9c2f7-153">Die **FtgRegisterIdleRoutine** -Funktion gibt ein function-Tag zurück, das die Leerlauf Routine identifiziert, die dem MAPI-System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="9c2f7-154">Wenn **FtgRegisterIdleRoutine** die Leerlauf Routine für die Clientanwendung oder den Dienstanbieter, beispielsweise aufgrund von Speicherproblemen, nicht registrieren kann, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c2f7-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c2f7-155">Remarks</span></span>

<span data-ttu-id="9c2f7-156">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="9c2f7-157">**Leerlauf Routine Funktion**</span><span class="sxs-lookup"><span data-stu-id="9c2f7-157">**Idle routine function**</span></span>|<span data-ttu-id="9c2f7-158">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="9c2f7-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c2f7-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9c2f7-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="9c2f7-160">Ändert die Eigenschaften einer registrierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="9c2f7-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9c2f7-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="9c2f7-162">Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9c2f7-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9c2f7-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="9c2f7-164">Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="9c2f7-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="9c2f7-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="9c2f7-166">Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="9c2f7-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="9c2f7-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="9c2f7-168">Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="9c2f7-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="9c2f7-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="9c2f7-170">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="9c2f7-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="9c2f7-172">Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="9c2f7-173">Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="9c2f7-174">Es folgt ein Beispiel für die Verwendung des FIRONOADJUSTMENT-Flags im _iroIdle_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="9c2f7-175">Registrieren Sie eine Leerlauf Routine mit einer Verzögerung von 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="9c2f7-176">Hibernate/Sleep the Computer after 1 Minute (4 Minuten Links auf dem Timer).</span><span class="sxs-lookup"><span data-stu-id="9c2f7-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="9c2f7-177">Setzen Sie den Computer 10 Minuten später fort.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="9c2f7-178">Das Standardverhalten ohne FIRONOADJUSTMENT ist, dass Sie noch 4 Minuten warten müssen, bis Ihre Routine ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="9c2f7-179">Das heißt, der Timer wurde angepasst, um zu ermöglichen, wie lange der Computer eingeschlafen ist.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="9c2f7-180">Wenn Sie jedoch FIRONOADJUSTMENT, wird die Leerlauf Routine sofort ausgeführt, da mehr als 5 Minuten in Echtzeit vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="9c2f7-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

