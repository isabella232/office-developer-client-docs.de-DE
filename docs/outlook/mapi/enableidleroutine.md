---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339396"
---
# <a name="enableidleroutine"></a><span data-ttu-id="853eb-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="853eb-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="853eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="853eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="853eb-105">Aktiviert oder deaktiviert eine [FNIDLE](fnidle.md) -basierte Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="853eb-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="853eb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="853eb-106">Header file:</span></span>  <br/> |<span data-ttu-id="853eb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="853eb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="853eb-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="853eb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="853eb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="853eb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="853eb-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="853eb-110">Called by:</span></span>  <br/> |<span data-ttu-id="853eb-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="853eb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="853eb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="853eb-112">Parameters</span></span>

 <span data-ttu-id="853eb-113">_FTG_</span><span class="sxs-lookup"><span data-stu-id="853eb-113">_ftg_</span></span>
  
> <span data-ttu-id="853eb-114">in Function-Tag, das die zu aktivierende oder zu deaktivierende Leerlauf Routine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="853eb-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="853eb-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="853eb-115">_fEnable_</span></span>
  
> <span data-ttu-id="853eb-116">in Enthält TRUE, wenn das Leerlauf Modul die Leerlauf Routine aktivieren soll, oder FALSE, wenn es deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="853eb-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="853eb-117">Return value</span><span class="sxs-lookup"><span data-stu-id="853eb-117">Return value</span></span>

<span data-ttu-id="853eb-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="853eb-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="853eb-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="853eb-119">Remarks</span></span>

<span data-ttu-id="853eb-120">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren:</span><span class="sxs-lookup"><span data-stu-id="853eb-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="853eb-121">**Leerlauf Routine Funktion**</span><span class="sxs-lookup"><span data-stu-id="853eb-121">**Idle routine function**</span></span>|<span data-ttu-id="853eb-122">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="853eb-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="853eb-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="853eb-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="853eb-124">Ändert die Eigenschaften einer registrierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="853eb-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="853eb-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="853eb-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="853eb-126">Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="853eb-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="853eb-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="853eb-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="853eb-128">Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="853eb-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="853eb-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="853eb-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="853eb-130">Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="853eb-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="853eb-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="853eb-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="853eb-132">Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="853eb-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="853eb-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="853eb-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="853eb-134">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="853eb-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="853eb-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="853eb-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="853eb-136">Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="853eb-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="853eb-137">Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="853eb-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

