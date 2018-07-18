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
ms.openlocfilehash: 00b5c123e588636654fb4287cc7b45500d47d89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791624"
---
# <a name="enableidleroutine"></a><span data-ttu-id="9fe82-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fe82-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="9fe82-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9fe82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9fe82-105">Aktiviert oder deaktiviert eine im Leerlauf Routine [FNIDLE](fnidle.md) basiert.</span><span class="sxs-lookup"><span data-stu-id="9fe82-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fe82-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9fe82-106">Header file:</span></span>  <br/> |<span data-ttu-id="9fe82-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9fe82-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9fe82-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9fe82-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9fe82-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9fe82-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9fe82-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9fe82-110">Called by:</span></span>  <br/> |<span data-ttu-id="9fe82-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9fe82-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="9fe82-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe82-112">Parameters</span></span>

 <span data-ttu-id="9fe82-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="9fe82-113">_ftg_</span></span>
  
> <span data-ttu-id="9fe82-114">[in] Funktion-Tag zur Identifizierung der im Leerlauf Routine aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fe82-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="9fe82-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="9fe82-115">_fEnable_</span></span>
  
> <span data-ttu-id="9fe82-116">[in] Enthält True, wenn das Modul im Leerlauf sollten die im Leerlauf Routine oder FALSE aktivieren, falls es deaktiviert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9fe82-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fe82-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fe82-117">Return value</span></span>

<span data-ttu-id="9fe82-118">None.</span><span class="sxs-lookup"><span data-stu-id="9fe82-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fe82-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fe82-119">Remarks</span></span>

<span data-ttu-id="9fe82-120">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="9fe82-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="9fe82-121">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="9fe82-121">**Idle routine function**</span></span>|<span data-ttu-id="9fe82-122">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="9fe82-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fe82-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fe82-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="9fe82-124">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="9fe82-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="9fe82-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fe82-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="9fe82-126">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="9fe82-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="9fe82-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="9fe82-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="9fe82-128">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="9fe82-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9fe82-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fe82-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="9fe82-130">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="9fe82-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="9fe82-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="9fe82-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="9fe82-132">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9fe82-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="9fe82-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="9fe82-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="9fe82-134">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9fe82-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="9fe82-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9fe82-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="9fe82-136">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="9fe82-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="9fe82-137">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="9fe82-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

