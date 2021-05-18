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
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412380"
---
# <a name="fnidle"></a><span data-ttu-id="cc75f-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="cc75f-103">FNIDLE</span></span>
 
<span data-ttu-id="cc75f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc75f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc75f-105">Definiert eine Leerlaufroutine, die das MAPI-Leerlaufmodul regelmäßig nach Priorität aufruft.</span><span class="sxs-lookup"><span data-stu-id="cc75f-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc75f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cc75f-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc75f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cc75f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cc75f-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="cc75f-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="cc75f-109">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="cc75f-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="cc75f-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="cc75f-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="cc75f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc75f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc75f-112">Entsprechender Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="cc75f-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="cc75f-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="cc75f-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="cc75f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc75f-114">Parameters</span></span>

 <span data-ttu-id="cc75f-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="cc75f-115">_lpvContext_</span></span>
  
> <span data-ttu-id="cc75f-116">[in] Zeiger auf einen Speicherblock, den MAPI bei jedem Aufruf an die Leerlaufroutine übergibt.</span><span class="sxs-lookup"><span data-stu-id="cc75f-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="cc75f-117">Dieser Zeiger wird von [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)an das MAPI-Leerlaufmodul im _parameter pvIdleParam_ übergeben.</span><span class="sxs-lookup"><span data-stu-id="cc75f-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="cc75f-118">Die Daten im Speicherblock können Kontext für den Aufruf der Leerlaufroutine bereitstellen, z. B. für das zu verwendende Objekt oder den aktuellen Status eines langwierigen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cc75f-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc75f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc75f-119">Return value</span></span>

<span data-ttu-id="cc75f-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="cc75f-120">FALSE</span></span> 
  
> <span data-ttu-id="cc75f-121">Eine Leerlaufroutine mit dem **FNIDLE-Prototyp** sollte immer FALSE zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc75f-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cc75f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc75f-122">Remarks</span></span>

<span data-ttu-id="cc75f-123">Die spezifische Funktionalität der Leerlaufroutine wird durch die implementierende Clientanwendung oder den Dienstanbieter bestimmt.</span><span class="sxs-lookup"><span data-stu-id="cc75f-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="cc75f-124">Der Client oder Anbieter muss die Ausführungszeit jedes Zustands einer Leerlaufroutine begrenzen.</span><span class="sxs-lookup"><span data-stu-id="cc75f-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="cc75f-125">Jeder Zustand sollte eine minimale Verarbeitungsmenge ausführen, den aktuellen Status in den Kontextdaten aktualisieren, auf die  _von lpvContext_ verwiesen wird, und zum MAPI-Leerlaufmodul zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="cc75f-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="cc75f-126">Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor er seine eigene Leerlaufroutine mit einem Aufruf der [FtgRegisterIdleRoutine-Funktion registrieren](ftgregisteridleroutine.md) kann.</span><span class="sxs-lookup"><span data-stu-id="cc75f-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="cc75f-127">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der FNIDLE-Funktion basieren:</span><span class="sxs-lookup"><span data-stu-id="cc75f-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="cc75f-128">**Routinefunktion im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="cc75f-128">**Idle routine function**</span></span>|<span data-ttu-id="cc75f-129">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="cc75f-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc75f-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="cc75f-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="cc75f-131">Ändert die Merkmale einer registrierten Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="cc75f-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="cc75f-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="cc75f-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="cc75f-133">Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="cc75f-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="cc75f-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="cc75f-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="cc75f-135">Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="cc75f-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="cc75f-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="cc75f-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="cc75f-137">Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc75f-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="cc75f-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="cc75f-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="cc75f-139">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cc75f-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="cc75f-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="cc75f-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="cc75f-141">Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cc75f-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="cc75f-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="cc75f-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="cc75f-143">Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc75f-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="cc75f-144">Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="cc75f-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

