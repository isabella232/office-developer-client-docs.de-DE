---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334433"
---
# <a name="changeidleroutine"></a><span data-ttu-id="375ed-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="375ed-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="375ed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="375ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="375ed-105">Ändert einige oder alle Merkmale einer [FNIDLE](fnidle.md) -basierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="375ed-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="375ed-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="375ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="375ed-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="375ed-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="375ed-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="375ed-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="375ed-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="375ed-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="375ed-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="375ed-110">Called by:</span></span>  <br/> |<span data-ttu-id="375ed-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="375ed-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a><span data-ttu-id="375ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="375ed-112">Parameters</span></span>

<span data-ttu-id="375ed-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="375ed-113">_ftg_</span></span>
  
> <span data-ttu-id="375ed-114">in Funktionstag, das die Leerlauf Routine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="375ed-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="375ed-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="375ed-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="375ed-116">in Zeiger auf die Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="375ed-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="375ed-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="375ed-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="375ed-118">in Zeiger auf einen neuen Speicherblock, den die aufrufende Implementierung für die Leerlauf Routine reserviert.</span><span class="sxs-lookup"><span data-stu-id="375ed-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="375ed-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="375ed-119">_priIdle_</span></span>
  
> <span data-ttu-id="375ed-120">in Wert, der eine neue Priorität für die Leerlauf Routine darstellt.</span><span class="sxs-lookup"><span data-stu-id="375ed-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="375ed-121">Mögliche Prioritäten für Implementierungs definierte Routinen sind größer oder kleiner als 0 (null), jedoch nicht NULL.</span><span class="sxs-lookup"><span data-stu-id="375ed-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="375ed-122">Der Wert 0 (null) ist für ein Benutzerereignis wie ein Mausklick oder eine WM_PAINT-Nachricht reserviert.</span><span class="sxs-lookup"><span data-stu-id="375ed-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="375ed-123">Werte, die größer als NULL sind, stellen Prioritäten für Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der standardmäßigen Windows-Nachrichten Pumpen Schleife gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="375ed-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="375ed-124">Werte, die kleiner als 0 (null) sind, stellen Prioritäten für Leerlauf Vorgänge dar, die nur während der Nachrichten Pumpen Leerlaufzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="375ed-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="375ed-125">Beispiele für Prioritäten sind: 1 für die Vordergrund Übermittlung, 1 für das Einfügen von Power-Edit-Zeichen und 3 zum Herunterladen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="375ed-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="375ed-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="375ed-126">_csecIdle_</span></span>
  
> <span data-ttu-id="375ed-127">in Eine neue Zeit in Hundertstel Sekunden, die auf die Leerlauf Routine angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="375ed-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="375ed-128">Die Bedeutung des anfänglichen Time-Werts variiert je nachdem, was im _iroIdle_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="375ed-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="375ed-129">Es kann Folgendes sein:</span><span class="sxs-lookup"><span data-stu-id="375ed-129">It can be:</span></span> 
    
  - <span data-ttu-id="375ed-130">Der minimale Zeitraum der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in _iroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="375ed-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="375ed-131">Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="375ed-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="375ed-132">Das minimale Intervall zwischen Aufrufen der Leerlauf Routine, wenn das FIROINTERVAL-Flag in _iroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="375ed-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="375ed-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="375ed-133">_iroIdle_</span></span>
  
> <span data-ttu-id="375ed-134">in Bitmaske von Flags, die neue Optionen für das Aufrufen der Leerlauf Routine angeben.</span><span class="sxs-lookup"><span data-stu-id="375ed-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="375ed-135">Es muss genau eines der folgenden Flags festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="375ed-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="375ed-136">FIROINTERVAL: die vom _csecIdle_ -Parameter angegebene Zeit ist das Mindestintervall zwischen aufeinanderfolgenden Aufrufen der Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="375ed-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="375ed-137">FIROONCEONLY: veraltet.</span><span class="sxs-lookup"><span data-stu-id="375ed-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="375ed-138">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="375ed-138">Do not use.</span></span> 
      
  - <span data-ttu-id="375ed-139">FIROPERBLOCK: veraltet.</span><span class="sxs-lookup"><span data-stu-id="375ed-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="375ed-140">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="375ed-140">Do not use.</span></span> 
      
  - <span data-ttu-id="375ed-141">FIROWAIT: die vom _csecIdle_ -Parameter angegebene Zeit ist die Mindestdauer der Benutzer Untätigkeit, die verstreichen muss, bevor das MAPI-Leerlauf Modul die Leerlauf Routine zum ersten Mal aufruft.</span><span class="sxs-lookup"><span data-stu-id="375ed-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="375ed-142">Nach diesem Zeitpunkt kann das Leerlauf Modul die Leerlauf Routine so oft aufrufen, wie es erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="375ed-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="375ed-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="375ed-143">_ircIdle_</span></span>
  
> <span data-ttu-id="375ed-144">in Bitmaske der Flags, die zum Anzeigen der Änderungen an der Leerlauf Routine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="375ed-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="375ed-145">Die folgenden Flags können in einer beliebigen Kombination festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="375ed-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="375ed-146">FIRCCSEC: eine Änderung der Zeit, die der Leerlauf Routine zugeordnet ist, also einer Änderung, die durch den im _csecIdle_ -Parameter übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="375ed-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="375ed-147">FIRCIRO: eine Änderung der Optionen für die Leerlauf Routine, also eine Änderung, die durch den im _iroIdle_ -Parameter übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="375ed-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="375ed-148">FIRCPFN: eine Änderung am Zeiger für die Leerlauf Routine, das heißt eine Änderung, die durch den im _pfnIdle_ -Parameter übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="375ed-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="375ed-149">FIRCPRI: eine Änderung der Priorität der Leerlauf Routine, also einer Änderung, die durch den im _priIdle_ -Parameter übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="375ed-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="375ed-150">FIRCPV: eine Änderung des Speicherblocks der Leerlauf Routine, also einer Änderung, die durch den im _pvIdleParam_ -Parameter übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="375ed-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="375ed-151">Return value</span><span class="sxs-lookup"><span data-stu-id="375ed-151">Return value</span></span>

<span data-ttu-id="375ed-152">Keine.</span><span class="sxs-lookup"><span data-stu-id="375ed-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="375ed-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="375ed-153">Remarks</span></span>

<span data-ttu-id="375ed-154">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren:</span><span class="sxs-lookup"><span data-stu-id="375ed-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="375ed-155">**Leerlauf Routine Funktion**</span><span class="sxs-lookup"><span data-stu-id="375ed-155">**Idle routine function**</span></span>|<span data-ttu-id="375ed-156">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="375ed-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="375ed-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="375ed-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="375ed-158">Ändert die Eigenschaften einer registrierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="375ed-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="375ed-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="375ed-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="375ed-160">Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="375ed-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="375ed-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="375ed-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="375ed-162">Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="375ed-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="375ed-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="375ed-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="375ed-164">Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="375ed-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="375ed-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="375ed-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="375ed-166">Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="375ed-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="375ed-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="375ed-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="375ed-168">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="375ed-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="375ed-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="375ed-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="375ed-170">Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="375ed-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="375ed-171">Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="375ed-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

