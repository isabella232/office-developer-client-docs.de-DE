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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418267"
---
# <a name="changeidleroutine"></a><span data-ttu-id="eb235-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="eb235-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="eb235-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb235-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb235-105">Ändert einige oder alle Merkmale einer [FNIDLE-basierten](fnidle.md) Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="eb235-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb235-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="eb235-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb235-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="eb235-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="eb235-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="eb235-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb235-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eb235-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eb235-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="eb235-110">Called by:</span></span>  <br/> |<span data-ttu-id="eb235-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="eb235-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="eb235-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb235-112">Parameters</span></span>

<span data-ttu-id="eb235-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="eb235-113">_ftg_</span></span>
  
> <span data-ttu-id="eb235-114">[in] Funktionstag, das die Leerlaufroutine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="eb235-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="eb235-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="eb235-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="eb235-116">[in] Zeiger auf die Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="eb235-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="eb235-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="eb235-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="eb235-118">[in] Zeiger auf einen neuen Speicherblock, der von der aufrufenden Implementierung für die Leerlaufroutine zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="eb235-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="eb235-119">_priIdle_</span></span>
  
> <span data-ttu-id="eb235-120">[in] Wert, der eine neue Priorität für die Leerlaufroutine darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb235-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="eb235-121">Mögliche Prioritäten für implementierungsdefinierte Routinen sind größer oder kleiner als Null, aber nicht Null.</span><span class="sxs-lookup"><span data-stu-id="eb235-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="eb235-122">Ein Wert von Null ist für ein Benutzerereignis reserviert, z. B. einen Mausklick oder eine WM_PAINT Nachricht.</span><span class="sxs-lookup"><span data-stu-id="eb235-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="eb235-123">Werte, die größer als Null sind, stellen Prioritäten für Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und im Rahmen der standardmäßigen nachrichtenumpumpschleife Windows werden.</span><span class="sxs-lookup"><span data-stu-id="eb235-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="eb235-124">Werte, die kleiner als Null sind, stellen Prioritäten für Leerlaufaufgaben dar, die nur während der Leerlaufzeit von Nachrichtenpumps ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eb235-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="eb235-125">Beispiele für Prioritäten sind: 1 für die Vordergrundübermittlung, 1 für das Einfügen von Power-Edit-Zeichen und 3 für das Herunterladen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="eb235-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="eb235-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="eb235-126">_csecIdle_</span></span>
  
> <span data-ttu-id="eb235-127">[in] Eine neue Zeit in Hundertstel sekunden, um auf die Leerlaufroutine anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="eb235-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="eb235-128">Die Bedeutung des Anfänglichen Zeitwerts variiert, je nachdem, was im  _iroIdle-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="eb235-129">Dies kann:</span><span class="sxs-lookup"><span data-stu-id="eb235-129">It can be:</span></span> 
    
  - <span data-ttu-id="eb235-130">Der Minimale Zeitraum der Untätigkeit des Benutzers, der verstreichen muss, bevor das MAPI-Leerlaufmodul die Leerlaufroutine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in  _iroIdle_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eb235-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="eb235-131">Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eb235-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="eb235-132">Das Mindestintervall zwischen Aufrufen der Leerlaufroutine, wenn das FIROINTERVAL-Flag in _iroIdle festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="eb235-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="eb235-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="eb235-133">_iroIdle_</span></span>
  
> <span data-ttu-id="eb235-134">[in] Bitmaske mit Flags, die neue Optionen zum Aufrufen der Leerlaufroutine angeben.</span><span class="sxs-lookup"><span data-stu-id="eb235-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="eb235-135">Genau eines der folgenden Kennzeichen muss festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="eb235-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="eb235-136">FIROINTERVAL: Die durch den  _csecIdle-Parameter_ angegebene Zeit ist das Mindestintervall zwischen aufeinander folgenden Aufrufen der Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="eb235-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="eb235-137">FIROONCEONLY: Veraltet.</span><span class="sxs-lookup"><span data-stu-id="eb235-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="eb235-138">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb235-138">Do not use.</span></span> 
      
  - <span data-ttu-id="eb235-139">FIROPERBLOCK: Veraltet.</span><span class="sxs-lookup"><span data-stu-id="eb235-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="eb235-140">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb235-140">Do not use.</span></span> 
      
  - <span data-ttu-id="eb235-141">FIROWAIT: Die durch den  _csecIdle-Parameter_ angegebene Zeit ist die minimale Dauer der Untätigkeit des Benutzers, die verstreichen muss, bevor das #A0 die Leerlaufroutine zum ersten Mal aufruft.</span><span class="sxs-lookup"><span data-stu-id="eb235-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="eb235-142">Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eb235-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="eb235-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="eb235-143">_ircIdle_</span></span>
  
> <span data-ttu-id="eb235-144">[in] Bitmaske von Flags, die verwendet werden, um die Änderungen an der Leerlaufroutine anzugeben.</span><span class="sxs-lookup"><span data-stu-id="eb235-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="eb235-145">Die folgenden Flags können in beliebiger Kombination festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="eb235-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="eb235-146">FIRCCSEC: Eine Änderung der Zeit, die der Leerlaufroutine zugeordnet ist, d. h. eine Änderung, die durch den im  _csecIdle-Parameter_ übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="eb235-147">FIRCIRO: Eine Änderung der Optionen für die Leerlaufroutine, d. h. eine Änderung, die durch den im  _iroIdle-Parameter_ übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="eb235-148">FIRCPFN: Eine Änderung am Leerlaufroutinenzeiger, d. h. eine Änderung, die durch den im  _pfnIdle-Parameter übergebenen_ Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="eb235-149">FIRCPRI: Eine Änderung an der Priorität der Leerlaufroutine, d. h. eine Änderung, die durch den im  _priIdle-Parameter_ übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="eb235-150">FIRCPV: Eine Änderung am Speicherblock der Leerlaufroutine, d. h. eine Änderung, die durch den im  _pvIdleParam-Parameter_ übergebenen Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb235-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb235-151">Return value</span><span class="sxs-lookup"><span data-stu-id="eb235-151">Return value</span></span>

<span data-ttu-id="eb235-152">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb235-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb235-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb235-153">Remarks</span></span>

<span data-ttu-id="eb235-154">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren:</span><span class="sxs-lookup"><span data-stu-id="eb235-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="eb235-155">**Routinefunktion im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="eb235-155">**Idle routine function**</span></span>|<span data-ttu-id="eb235-156">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="eb235-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb235-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="eb235-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="eb235-158">Ändert die Merkmale einer registrierten Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="eb235-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="eb235-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="eb235-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="eb235-160">Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="eb235-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="eb235-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="eb235-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="eb235-162">Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="eb235-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="eb235-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="eb235-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="eb235-164">Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb235-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="eb235-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="eb235-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="eb235-166">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="eb235-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="eb235-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="eb235-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="eb235-168">Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="eb235-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="eb235-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="eb235-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="eb235-170">Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb235-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="eb235-171">Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="eb235-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

