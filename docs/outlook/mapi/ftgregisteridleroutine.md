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
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791762"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="d6917-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6917-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="d6917-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6917-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6917-105">Das MAPI-System hinzugefügt eine [FNIDLE](fnidle.md) funktionsbasierte im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d6917-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6917-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d6917-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6917-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d6917-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d6917-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d6917-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6917-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d6917-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d6917-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d6917-110">Called by:</span></span>  <br/> |<span data-ttu-id="d6917-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d6917-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="d6917-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6917-112">Parameters</span></span>

<span data-ttu-id="d6917-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="d6917-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="d6917-114">[in] Ein Zeiger auf die im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d6917-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="d6917-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="d6917-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="d6917-116">[in] Ein Zeiger auf einen Block von Arbeitsspeicher, die das Modul im Leerlauf sollte als Parameter für die im Leerlauf Routine beim übergeben es aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d6917-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="d6917-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="d6917-117">_priIdle_</span></span>
  
> <span data-ttu-id="d6917-118">[in] Die erste Priorität für die im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d6917-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="d6917-119">Mögliche Prioritäten für die Implementierung definierten Routinen sind größer oder kleiner als 0 (null), aber nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d6917-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="d6917-120">Die Priorität 0 (null) ist für eine Benutzerereignis wie klicken mit der Maus oder eine Nachricht WM_PAINT reserviert.</span><span class="sxs-lookup"><span data-stu-id="d6917-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="d6917-121">Größer als 0 (null) Prioritäten darstellen Hintergrundaufgaben, die eine höhere Priorität als Veranstaltungen und werden im Rahmen der standardmäßigen Windows-Nachricht Pumpe Schleife verteilt.</span><span class="sxs-lookup"><span data-stu-id="d6917-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="d6917-122">Prioritäten kleiner als 0 (null) darstellen im Leerlauf Aufgaben, die nur während der Nachricht Pumpe Leerlaufzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6917-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="d6917-123">Beispiele für Prioritäten sind wie folgt: 1 für die Übermittlung von Vordergrund, für das Einfügen von Power bearbeiten Zeichen 2 und 3 für das Herunterladen von neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d6917-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="d6917-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="d6917-124">_csecIdle_</span></span>
  
> <span data-ttu-id="d6917-125">[in] Der Wert der anfänglichen Uhrzeit im Hundertstelsekunden, bei der Angabe im Leerlauf routinemäßige-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6917-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="d6917-126">Die Bedeutung des ursprünglichen Zeitwerts hängt davon ab, was im _IroIdle_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6917-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="d6917-127">Die Bedeutung kann eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="d6917-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="d6917-128">Der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor die MAPI ruft im Leerlauf Modul die im Leerlauf Routine zum ersten Mal, wenn das Flag FIROWAIT in _IroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6917-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="d6917-129">Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d6917-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="d6917-130">Das kürzeste Intervall zwischen Aufrufen der im Leerlauf Routine, wenn das Flag FIROINTERVAL in _IroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6917-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="d6917-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="d6917-131">_iroIdle_</span></span>
  
> <span data-ttu-id="d6917-132">[in] Die Bitmaske Flags verwendet, um die anfängliche Optionen für die im Leerlauf Routine festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d6917-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="d6917-133">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d6917-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="d6917-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="d6917-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="d6917-135">Verwenden Sie dieses Flag angegeben wird, dass der im Leerlauf routinemäßige Zeitgeber Standbymodus nicht angepasst werden sollten oder fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d6917-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="d6917-136">Das Standardverhalten ohne dieses Flag ist, dass beim Berechnen der verstrichenen Zeit Zeit für Ruhezustand ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d6917-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="d6917-137">Wenn FIRONOADJUSTMENT übergeben wird, werden die Zeit für Ruhezustand eingeschlossen beim Berechnen der verstrichenen Zeit.</span><span class="sxs-lookup"><span data-stu-id="d6917-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="d6917-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="d6917-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="d6917-139">Die im Leerlauf Routine sollte deaktiviert werden, wenn registriert.</span><span class="sxs-lookup"><span data-stu-id="d6917-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="d6917-140">Die Standardaktion besteht, die im Leerlauf Routine aktivieren, wenn **FtgRegisterIdleRoutine** registriert.</span><span class="sxs-lookup"><span data-stu-id="d6917-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="d6917-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="d6917-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="d6917-142">Die durch den _CsecIdle_ -Parameter angegebenen Zeit ist das kürzeste Intervall zwischen aufeinander folgenden Aufrufen der Routine im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="d6917-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="d6917-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="d6917-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="d6917-p107">Veraltet. Nicht verwenden. </span><span class="sxs-lookup"><span data-stu-id="d6917-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="d6917-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="d6917-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="d6917-p108">Veraltet. Nicht verwenden. </span><span class="sxs-lookup"><span data-stu-id="d6917-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="d6917-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="d6917-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="d6917-150">Die durch den _CsecIdle_ -Parameter angegebenen Zeit ist der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor das im Leerlauf MAPI-Modul die im Leerlauf Routine zum ersten Mal aufruft.</span><span class="sxs-lookup"><span data-stu-id="d6917-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="d6917-151">Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d6917-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6917-152">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d6917-152">Return value</span></span>

<span data-ttu-id="d6917-153">Die **FtgRegisterIdleRoutine** -Funktion gibt eine Function-Tag, identifiziert der im Leerlauf Routine, die die MAPI-System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6917-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="d6917-154">Wenn **FtgRegisterIdleRoutine** nicht im Leerlauf Routine für die Clientanwendung oder Dienstanbieter registrieren können, beispielsweise aufgrund Speicherprobleme, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6917-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d6917-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6917-155">Remarks</span></span>

<span data-ttu-id="d6917-156">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp.</span><span class="sxs-lookup"><span data-stu-id="d6917-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="d6917-157">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="d6917-157">**Idle routine function**</span></span>|<span data-ttu-id="d6917-158">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="d6917-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6917-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6917-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="d6917-160">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d6917-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="d6917-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6917-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="d6917-162">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="d6917-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d6917-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6917-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d6917-164">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d6917-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="d6917-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="d6917-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="d6917-166">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d6917-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="d6917-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d6917-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="d6917-168">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d6917-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="d6917-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d6917-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="d6917-170">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d6917-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="d6917-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6917-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="d6917-172">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="d6917-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d6917-173">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="d6917-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="d6917-174">Es folgt ein Beispiel für das Flag FIRONOADJUSTMENT im _IroIdle_ -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6917-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="d6917-175">Registrieren einer Routine im Leerlauf mit einer Verzögerung von 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="d6917-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="d6917-176">Ruhezustand/Standbymodus den Computer nach einer Minute (4 Minuten auf den Timer).</span><span class="sxs-lookup"><span data-stu-id="d6917-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="d6917-177">Setzen Sie den Computer später 10 Minuten fort.</span><span class="sxs-lookup"><span data-stu-id="d6917-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="d6917-178">Das Standardverhalten, ohne FIRONOADJUSTMENT, ist, dass Sie warten, bis 4 Minuten für eine Routine noch ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6917-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="d6917-179">D. h., wurde Zeitgebers angepasst, um zuzulassen, für wie lange der Computer im Standbymodus war.</span><span class="sxs-lookup"><span data-stu-id="d6917-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="d6917-180">Wenn Sie FIRONOADJUSTMENT übergeben wird jedoch eine Routine im Leerlauf sofort ausgeführt, da Echtzeit von mehr als 5 Minuten verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="d6917-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

