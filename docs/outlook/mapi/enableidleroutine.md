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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410221"
---
# <a name="enableidleroutine"></a><span data-ttu-id="81156-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="81156-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="81156-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81156-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81156-105">Aktiviert oder deaktiviert eine [FNIDLE-basierte](fnidle.md) Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="81156-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81156-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="81156-106">Header file:</span></span>  <br/> |<span data-ttu-id="81156-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="81156-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="81156-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="81156-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="81156-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="81156-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="81156-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="81156-110">Called by:</span></span>  <br/> |<span data-ttu-id="81156-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="81156-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="81156-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="81156-112">Parameters</span></span>

 <span data-ttu-id="81156-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="81156-113">_ftg_</span></span>
  
> <span data-ttu-id="81156-114">[in] Funktionstag, das die zu aktivierende oder deaktivierte Leerlaufroutine identifiziert.</span><span class="sxs-lookup"><span data-stu-id="81156-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="81156-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="81156-115">_fEnable_</span></span>
  
> <span data-ttu-id="81156-116">[in] Enthält TRUE, wenn das Leerlaufmodul die Leerlaufroutine aktivieren soll, oder FALSE, wenn es es deaktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="81156-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81156-117">Return value</span><span class="sxs-lookup"><span data-stu-id="81156-117">Return value</span></span>

<span data-ttu-id="81156-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="81156-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81156-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81156-119">Remarks</span></span>

<span data-ttu-id="81156-120">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren:</span><span class="sxs-lookup"><span data-stu-id="81156-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="81156-121">**Routinefunktion im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="81156-121">**Idle routine function**</span></span>|<span data-ttu-id="81156-122">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="81156-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81156-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="81156-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="81156-124">Ändert die Merkmale einer registrierten Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="81156-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="81156-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="81156-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="81156-126">Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="81156-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="81156-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="81156-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="81156-128">Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="81156-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="81156-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="81156-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="81156-130">Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="81156-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="81156-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="81156-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="81156-132">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="81156-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="81156-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="81156-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="81156-134">Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="81156-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="81156-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="81156-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="81156-136">Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="81156-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="81156-137">Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="81156-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

