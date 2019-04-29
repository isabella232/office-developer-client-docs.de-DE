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
# <a name="deregisteridleroutine"></a><span data-ttu-id="e7e70-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7e70-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="e7e70-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7e70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7e70-105">Entfernt eine [FNIDLE](fnidle.md) -basierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="e7e70-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7e70-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e7e70-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7e70-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e7e70-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7e70-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e7e70-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7e70-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7e70-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7e70-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e7e70-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7e70-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e7e70-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="e7e70-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7e70-112">Parameters</span></span>

 <span data-ttu-id="e7e70-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="e7e70-113">_ftg_</span></span>
  
> <span data-ttu-id="e7e70-114">in Funktionstag, das die zu entfernende Leerlauf Routine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7e70-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7e70-115">Return value</span><span class="sxs-lookup"><span data-stu-id="e7e70-115">Return value</span></span>

<span data-ttu-id="e7e70-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7e70-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7e70-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7e70-117">Remarks</span></span>

<span data-ttu-id="e7e70-118">Jede Aufgabe in einer Clientanwendung oder einem Dienstanbieter kann jede Leerlauf Routine, für die Sie einen gültigen _FTG_ -Parameter aufweist, aufheben.</span><span class="sxs-lookup"><span data-stu-id="e7e70-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="e7e70-119">Insbesondere eine Leerlauf Routine kann sich selbst aufheben.</span><span class="sxs-lookup"><span data-stu-id="e7e70-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="e7e70-120">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren:</span><span class="sxs-lookup"><span data-stu-id="e7e70-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="e7e70-121">**Leerlauf Routine Funktion**</span><span class="sxs-lookup"><span data-stu-id="e7e70-121">**Idle routine function**</span></span>|<span data-ttu-id="e7e70-122">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="e7e70-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7e70-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7e70-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="e7e70-124">Ändert die Eigenschaften einer registrierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="e7e70-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="e7e70-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="e7e70-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="e7e70-126">Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="e7e70-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e7e70-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7e70-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="e7e70-128">Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e7e70-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e7e70-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7e70-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="e7e70-130">Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e7e70-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="e7e70-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e7e70-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="e7e70-132">Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="e7e70-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="e7e70-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e7e70-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="e7e70-134">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e7e70-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="e7e70-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="e7e70-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="e7e70-136">Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="e7e70-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="e7e70-137">Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="e7e70-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="e7e70-138">Nachdem die Leerlauf Routine deregistriert wurde, wird Sie vom Leerlauf Modul nicht erneut aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e7e70-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="e7e70-139">Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke freigeben, an die Sie Zeiger für das Leerlauf Modul übergeben hat, die im ursprünglichen Aufruf der **FtgRegisterIdleRoutine** -Funktion verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7e70-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

