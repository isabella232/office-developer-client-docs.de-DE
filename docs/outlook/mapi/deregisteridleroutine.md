---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404561"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="0e895-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0e895-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="0e895-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e895-105">Entfernt eine [FNIDLE-basierte](fnidle.md) Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="0e895-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e895-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0e895-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e895-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0e895-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0e895-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0e895-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e895-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0e895-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0e895-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0e895-110">Called by:</span></span>  <br/> |<span data-ttu-id="0e895-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0e895-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="0e895-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e895-112">Parameters</span></span>

 <span data-ttu-id="0e895-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="0e895-113">_ftg_</span></span>
  
> <span data-ttu-id="0e895-114">[in] Funktionstag, das die zu entfernende Leerlaufroutine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e895-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e895-115">Return value</span><span class="sxs-lookup"><span data-stu-id="0e895-115">Return value</span></span>

<span data-ttu-id="0e895-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="0e895-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e895-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e895-117">Remarks</span></span>

<span data-ttu-id="0e895-118">Jede Aufgabe in einer Clientanwendung oder einem Dienstanbieter kann alle Leerlaufroutinen, für die sie über einen gültigen  _ftg-Parameter_ verfügt, abmelden.</span><span class="sxs-lookup"><span data-stu-id="0e895-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="0e895-119">Insbesondere kann sich eine Leerlaufroutine selbst abmelden.</span><span class="sxs-lookup"><span data-stu-id="0e895-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="0e895-120">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren:</span><span class="sxs-lookup"><span data-stu-id="0e895-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="0e895-121">**Routinefunktion im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="0e895-121">**Idle routine function**</span></span>|<span data-ttu-id="0e895-122">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="0e895-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e895-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0e895-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="0e895-124">Ändert die Merkmale einer registrierten Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="0e895-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="0e895-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="0e895-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="0e895-126">Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="0e895-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0e895-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0e895-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="0e895-128">Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0e895-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0e895-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0e895-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="0e895-130">Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e895-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="0e895-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="0e895-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="0e895-132">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0e895-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="0e895-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="0e895-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="0e895-134">Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0e895-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="0e895-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="0e895-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="0e895-136">Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e895-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="0e895-137">Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="0e895-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="0e895-138">Nachdem die Leerlaufroutine abgemeldet wurde, wird sie vom Leerlaufmodul nicht erneut aufruft.</span><span class="sxs-lookup"><span data-stu-id="0e895-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="0e895-139">Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke, an die Zeiger für das Leerlaufmodul übergeben werden, für den ursprünglichen Aufruf der **FtgRegisterIdleRoutine-Funktion** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e895-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

