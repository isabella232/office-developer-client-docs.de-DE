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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fd9a91b089bb06e6dfe34a1a144245d404adb270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569225"
---
# <a name="mapiinitidle"></a><span data-ttu-id="6ef62-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="6ef62-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="6ef62-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ef62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ef62-105">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ef62-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ef62-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6ef62-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ef62-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6ef62-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6ef62-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6ef62-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ef62-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ef62-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6ef62-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6ef62-110">Called by:</span></span>  <br/> |<span data-ttu-id="6ef62-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6ef62-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="6ef62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ef62-112">Parameters</span></span>

 <span data-ttu-id="6ef62-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="6ef62-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="6ef62-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6ef62-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ef62-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6ef62-115">Return value</span></span>

<span data-ttu-id="6ef62-116">Die **MAPIInitIdle** -Funktion gibt NULL zurück, falls die Initialisierung erfolgreich ist, und 1 ist.</span><span class="sxs-lookup"><span data-stu-id="6ef62-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="6ef62-117">Wenn **MAPIInitIdle** mehrere Male aufgerufen wird, alle zusätzlichen Anrufe fehlerfrei ausgeführt werden, jedoch werden ignoriert, außer wenn erhöht den Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="6ef62-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6ef62-118">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6ef62-118">Remarks</span></span>

<span data-ttu-id="6ef62-119">Eine Clientanwendung oder Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor alle anderen im Leerlauf Engine-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ef62-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="6ef62-120">Jedem Aufruf von **MAPIInitIdle** muss durch einen nachfolgenden Aufruf von [MAPIDeInitIdle](mapideinitidle.md)abgeglichen werden, oder das Modul im Leerlauf verläuft von Links für die aufrufende Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ef62-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="6ef62-121">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="6ef62-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="6ef62-122">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="6ef62-122">**Idle routine function**</span></span>|<span data-ttu-id="6ef62-123">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="6ef62-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ef62-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6ef62-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="6ef62-125">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="6ef62-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="6ef62-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6ef62-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="6ef62-127">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="6ef62-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="6ef62-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6ef62-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="6ef62-129">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="6ef62-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="6ef62-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="6ef62-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="6ef62-131">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="6ef62-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="6ef62-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="6ef62-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="6ef62-133">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6ef62-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="6ef62-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="6ef62-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="6ef62-135">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ef62-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="6ef62-136">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="6ef62-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="6ef62-137">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="6ef62-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

