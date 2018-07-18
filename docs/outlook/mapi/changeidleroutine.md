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
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791432"
---
# <a name="changeidleroutine"></a><span data-ttu-id="d026b-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d026b-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="d026b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d026b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d026b-105">Ändert einige oder alle Merkmale eine im Leerlauf Routine [FNIDLE](fnidle.md) basiert.</span><span class="sxs-lookup"><span data-stu-id="d026b-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d026b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d026b-106">Header file:</span></span>  <br/> |<span data-ttu-id="d026b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d026b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d026b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d026b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d026b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d026b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d026b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d026b-110">Called by:</span></span>  <br/> |<span data-ttu-id="d026b-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d026b-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d026b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d026b-112">Parameters</span></span>

<span data-ttu-id="d026b-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="d026b-113">_ftg_</span></span>
  
> <span data-ttu-id="d026b-114">[in] Funktion-Tag, die im Leerlauf Routine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d026b-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="d026b-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="d026b-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="d026b-116">[in] Zeiger auf die im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d026b-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="d026b-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="d026b-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="d026b-118">[in] Zeiger auf einen neuen Block Arbeitsspeicher, der die aufrufende Implementierung für die im Leerlauf Routine zuweist.</span><span class="sxs-lookup"><span data-stu-id="d026b-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="d026b-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="d026b-119">_priIdle_</span></span>
  
> <span data-ttu-id="d026b-120">[in] Wert, der eine neue Priorität für die im Leerlauf Routine darstellt.</span><span class="sxs-lookup"><span data-stu-id="d026b-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="d026b-121">Mögliche Prioritäten für die Implementierung definierten Routinen sind größer oder kleiner als 0 (null), aber nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d026b-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="d026b-122">Der Wert 0 (null) ist für eine Benutzerereignis wie klicken mit der Maus oder eine Nachricht WM_PAINT reserviert.</span><span class="sxs-lookup"><span data-stu-id="d026b-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="d026b-123">Werte, die größer als 0 (null) darstellen Prioritäten für Hintergrund-Vorgänge, die eine höhere Priorität als Veranstaltungen und werden im Rahmen der standardmäßigen Windows-Nachricht Pumpe Schleife verteilt.</span><span class="sxs-lookup"><span data-stu-id="d026b-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="d026b-124">Werte kleiner als 0 (null) darstellen Prioritäten für im Leerlauf Vorgänge, die nur während der Leerlaufzeit Nachrichtensystem ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d026b-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="d026b-125">Beispiele für Prioritäten sind: 1 für die Übermittlung von Vordergrund, für das Einfügen von Power bearbeiten Zeichen 1 und 3 für das Herunterladen von neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d026b-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="d026b-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="d026b-126">_csecIdle_</span></span>
  
> <span data-ttu-id="d026b-127">[in] Eine neue Zeit in Hundertstelsekunden, der im Leerlauf Routine zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d026b-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="d026b-128">Die Bedeutung des ursprünglichen Zeitwerts hängt davon ab, was im _IroIdle_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d026b-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="d026b-129">Es kann sein:</span><span class="sxs-lookup"><span data-stu-id="d026b-129">It can be:</span></span> 
    
  - <span data-ttu-id="d026b-130">Der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor die MAPI ruft im Leerlauf Modul die im Leerlauf Routine zum ersten Mal, wenn das Flag FIROWAIT in _IroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d026b-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="d026b-131">Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d026b-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="d026b-132">Das kürzeste Intervall zwischen Aufrufen der im Leerlauf Routine, wenn das Flag FIROINTERVAL in _IroIdle_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d026b-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="d026b-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="d026b-133">_iroIdle_</span></span>
  
> <span data-ttu-id="d026b-134">[in] Bitmaske aus Flags, die neue Optionen zum Aufrufen der im Leerlauf Routine angibt.</span><span class="sxs-lookup"><span data-stu-id="d026b-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="d026b-135">Genau einem der folgenden Flags muss festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d026b-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="d026b-136">FIROINTERVAL: Die Zeit, die durch den Parameter _CsecIdle_ angegeben ist das kürzeste Intervall zwischen aufeinander folgenden Aufrufen der Routine im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="d026b-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="d026b-137">FIROONCEONLY: veraltet.</span><span class="sxs-lookup"><span data-stu-id="d026b-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="d026b-138">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d026b-138">Do not use.</span></span> 
      
  - <span data-ttu-id="d026b-139">FIROPERBLOCK: veraltet.</span><span class="sxs-lookup"><span data-stu-id="d026b-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="d026b-140">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d026b-140">Do not use.</span></span> 
      
  - <span data-ttu-id="d026b-141">FIROWAIT: Die Zeit, die durch den Parameter _CsecIdle_ angegeben ist der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor das im Leerlauf MAPI-Modul die im Leerlauf Routine zum ersten Mal aufruft.</span><span class="sxs-lookup"><span data-stu-id="d026b-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="d026b-142">Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d026b-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="d026b-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="d026b-143">_ircIdle_</span></span>
  
> <span data-ttu-id="d026b-144">[in] Bitmaske der Flags verwendet, um die Änderungen anzugeben, der im Leerlauf Routine vorgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d026b-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="d026b-145">Die folgenden Kennzeichen können eine beliebige Kombination festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d026b-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="d026b-146">FIRCCSEC: Eine Änderung an den Zeitaufwand für die im Leerlauf Routine, d. h., eine Änderung von der in der _CsecIdle_ -Parameter übergebene Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="d026b-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="d026b-147">FIRCIRO: Eine Änderung der Optionen für die Routine im Leerlauf, d. h., eine Änderung angegeben durch den Wert im _IroIdle_ Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d026b-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="d026b-148">FIRCPFN: Eine Änderung der im Leerlauf routinemäßige Zeiger, d. h., eine Änderung angegeben durch den Wert im _PfnIdle_ Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d026b-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="d026b-149">FIRCPRI: Eine Änderung der Priorität von der Routine im Leerlauf, d. h., eine Änderung angegeben durch den Wert im _PriIdle_ Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d026b-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="d026b-150">FIRCPV: Eine Änderung an den Arbeitsspeicher Block mit der Routine im Leerlauf, d. h., eine Änderung angegeben durch den Wert im _PvIdleParam_ Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d026b-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d026b-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d026b-151">Return value</span></span>

<span data-ttu-id="d026b-152">None.</span><span class="sxs-lookup"><span data-stu-id="d026b-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d026b-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d026b-153">Remarks</span></span>

<span data-ttu-id="d026b-154">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="d026b-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="d026b-155">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="d026b-155">**Idle routine function**</span></span>|<span data-ttu-id="d026b-156">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="d026b-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d026b-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="d026b-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="d026b-158">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d026b-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="d026b-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d026b-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="d026b-160">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="d026b-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d026b-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d026b-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d026b-162">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="d026b-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d026b-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d026b-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="d026b-164">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="d026b-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="d026b-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d026b-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="d026b-166">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d026b-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="d026b-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d026b-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="d026b-168">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d026b-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="d026b-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d026b-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="d026b-170">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="d026b-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d026b-171">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="d026b-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

