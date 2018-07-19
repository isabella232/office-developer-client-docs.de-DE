---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791716"
---
# <a name="fnidle"></a><span data-ttu-id="3b864-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="3b864-103">FNIDLE</span></span>
 
<span data-ttu-id="3b864-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b864-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b864-105">Definiert eine im Leerlauf-Routine, die das im Leerlauf MAPI-Modul in regelmäßigen Abständen nach Priorität aufruft.</span><span class="sxs-lookup"><span data-stu-id="3b864-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b864-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3b864-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b864-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3b864-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3b864-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="3b864-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3b864-109">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3b864-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="3b864-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="3b864-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3b864-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="3b864-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="3b864-112">Zeigertyp des entsprechenden:</span><span class="sxs-lookup"><span data-stu-id="3b864-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="3b864-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="3b864-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="3b864-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b864-114">Parameters</span></span>

 <span data-ttu-id="3b864-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="3b864-115">_lpvContext_</span></span>
  
> <span data-ttu-id="3b864-116">[in] Zeiger auf einen Block von Arbeitsspeicher, dass MAPI an im Leerlauf Routine übergeben es Zeit wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3b864-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="3b864-117">Dieser Zeiger wird vom [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)an das im Leerlauf MAPI-Modul in der _PvIdleParam_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="3b864-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="3b864-118">Die Daten in den Arbeitsspeicher-Block können für den Anruf an die im Leerlauf Routine, beispielsweise zum Verarbeiten von, welches Objekt oder den aktuellen Status einer langen Operation Kontext bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b864-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b864-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b864-119">Return value</span></span>

<span data-ttu-id="3b864-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="3b864-120">FALSE</span></span> 
  
> <span data-ttu-id="3b864-121">Eine im Leerlauf Routine mit dem Prototyp **FNIDLE** sollte immer FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="3b864-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3b864-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b864-122">Remarks</span></span>

<span data-ttu-id="3b864-123">Die spezifische Funktionen der der im Leerlauf Routine wird durch die Implementierung bestimmt Clientanwendung oder den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3b864-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="3b864-124">Der Client oder Anbieter muss die Ausführungszeit der einzelnen Zustände einer im Leerlauf Routine einschränken.</span><span class="sxs-lookup"><span data-stu-id="3b864-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="3b864-125">Jeder Zustand sollte eine Mindest-Verarbeitung ausführen, in den Kontextdaten auf die _LpvContext_zeigt den aktuellen Status aktualisieren und zurück an die MAPI-Modul im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="3b864-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="3b864-126">Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor sie eine eigene im Leerlauf Routine mit einem Aufruf der Funktion [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) registrieren kann.</span><span class="sxs-lookup"><span data-stu-id="3b864-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="3b864-127">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den FNIDLE Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="3b864-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="3b864-128">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="3b864-128">**Idle routine function**</span></span>|<span data-ttu-id="3b864-129">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="3b864-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b864-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b864-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="3b864-131">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="3b864-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="3b864-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b864-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="3b864-133">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="3b864-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3b864-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b864-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="3b864-135">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="3b864-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3b864-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b864-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="3b864-137">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="3b864-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="3b864-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="3b864-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="3b864-139">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3b864-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="3b864-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="3b864-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="3b864-141">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3b864-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="3b864-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b864-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="3b864-143">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="3b864-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="3b864-144">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="3b864-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

