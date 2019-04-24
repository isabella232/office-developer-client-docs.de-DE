---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346655"
---
# <a name="mapiinitidle"></a><span data-ttu-id="920c5-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="920c5-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="920c5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="920c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="920c5-105">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="920c5-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="920c5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="920c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="920c5-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="920c5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="920c5-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="920c5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="920c5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="920c5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="920c5-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="920c5-110">Called by:</span></span>  <br/> |<span data-ttu-id="920c5-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="920c5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="920c5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="920c5-112">Parameters</span></span>

 <span data-ttu-id="920c5-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="920c5-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="920c5-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="920c5-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="920c5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="920c5-115">Return value</span></span>

<span data-ttu-id="920c5-116">Die **MAPIInitIdle** -Funktion gibt NULL zurück, wenn die Initialisierung erfolgreich ist, und 1 andernfalls.</span><span class="sxs-lookup"><span data-stu-id="920c5-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="920c5-117">Wenn **MAPIInitIdle** mehrmals aufgerufen wird, werden alle zusätzlichen Aufrufe erfolgreich ausgeführt, werden jedoch ignoriert, außer um den Verweiszähler zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="920c5-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="920c5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="920c5-118">Remarks</span></span>

<span data-ttu-id="920c5-119">Eine Clientanwendung oder ein Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor eine andere Leerlauf Funktion des Moduls aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="920c5-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="920c5-120">Jeder Aufruf von **MAPIInitIdle** muss durch einen nachfolgenden Aufruf von [MAPIDeInitIdle](mapideinitidle.md)oder das Leerlauf Modul für die aufrufende Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="920c5-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="920c5-121">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren:</span><span class="sxs-lookup"><span data-stu-id="920c5-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="920c5-122">**Leerlauf Routine Funktion**</span><span class="sxs-lookup"><span data-stu-id="920c5-122">**Idle routine function**</span></span>|<span data-ttu-id="920c5-123">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="920c5-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="920c5-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="920c5-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="920c5-125">Ändert die Eigenschaften einer registrierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="920c5-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="920c5-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="920c5-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="920c5-127">Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="920c5-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="920c5-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="920c5-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="920c5-129">Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="920c5-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="920c5-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="920c5-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="920c5-131">Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="920c5-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="920c5-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="920c5-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="920c5-133">Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="920c5-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="920c5-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="920c5-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="920c5-135">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="920c5-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="920c5-136">Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="920c5-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="920c5-137">Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="920c5-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

