---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408208"
---
# <a name="mapideinitidle"></a><span data-ttu-id="d2ed0-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d2ed0-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="d2ed0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2ed0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2ed0-105">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2ed0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d2ed0-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2ed0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d2ed0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d2ed0-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d2ed0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2ed0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ed0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2ed0-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d2ed0-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2ed0-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d2ed0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="d2ed0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2ed0-112">Parameters</span></span>

<span data-ttu-id="d2ed0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d2ed0-114">Return value</span><span class="sxs-lookup"><span data-stu-id="d2ed0-114">Return value</span></span>

<span data-ttu-id="d2ed0-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2ed0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2ed0-116">Remarks</span></span>

<span data-ttu-id="d2ed0-117">Eine Clientanwendung oder ein Dienstanbieter sollte **MAPIDeInitIdle** aufrufen, wenn das Leerlaufmodul nicht mehr benötigt wird, z. B. wenn die Verarbeitung beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="d2ed0-118">Jedem Aufruf von [MAPIInitIdle](mapiinitidle.md) muss ein nachfolgender Aufruf von **MAPIDeInitIdle** entsprechen, oder das Leerlaufmodul wird für die aufrufende Anwendung noch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="d2ed0-119">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren:</span><span class="sxs-lookup"><span data-stu-id="d2ed0-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="d2ed0-120">**Routinefunktion im Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="d2ed0-120">**Idle routine function**</span></span>|<span data-ttu-id="d2ed0-121">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="d2ed0-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2ed0-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2ed0-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="d2ed0-123">Ändert die Merkmale einer registrierten Leerlaufroutine.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="d2ed0-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2ed0-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="d2ed0-125">Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d2ed0-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2ed0-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d2ed0-127">Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d2ed0-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2ed0-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="d2ed0-129">Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="d2ed0-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="d2ed0-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="d2ed0-131">Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="d2ed0-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d2ed0-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="d2ed0-133">Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="d2ed0-134">Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d2ed0-135">Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

