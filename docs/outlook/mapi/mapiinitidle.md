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
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793124"
---
# <a name="mapiinitidle"></a><span data-ttu-id="ab74c-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="ab74c-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="ab74c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab74c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab74c-105">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ab74c-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab74c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ab74c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab74c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ab74c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ab74c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ab74c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab74c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab74c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab74c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ab74c-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab74c-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ab74c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="ab74c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab74c-112">Parameters</span></span>

 <span data-ttu-id="ab74c-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="ab74c-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="ab74c-114">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="ab74c-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab74c-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ab74c-115">Return value</span></span>

<span data-ttu-id="ab74c-116">Die **MAPIInitIdle** -Funktion gibt NULL zurück, falls die Initialisierung erfolgreich ist, und 1 ist.</span><span class="sxs-lookup"><span data-stu-id="ab74c-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="ab74c-117">Wenn **MAPIInitIdle** mehrere Male aufgerufen wird, alle zusätzlichen Anrufe fehlerfrei ausgeführt werden, jedoch werden ignoriert, außer wenn erhöht den Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="ab74c-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ab74c-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab74c-118">Remarks</span></span>

<span data-ttu-id="ab74c-119">Eine Clientanwendung oder Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor alle anderen im Leerlauf Engine-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab74c-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="ab74c-120">Jedem Aufruf von **MAPIInitIdle** muss durch einen nachfolgenden Aufruf von [MAPIDeInitIdle](mapideinitidle.md)abgeglichen werden, oder das Modul im Leerlauf verläuft von Links für die aufrufende Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab74c-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="ab74c-121">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="ab74c-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="ab74c-122">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="ab74c-122">**Idle routine function**</span></span>|<span data-ttu-id="ab74c-123">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="ab74c-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab74c-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ab74c-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="ab74c-125">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="ab74c-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="ab74c-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ab74c-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="ab74c-127">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="ab74c-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="ab74c-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ab74c-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="ab74c-129">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="ab74c-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="ab74c-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ab74c-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="ab74c-131">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="ab74c-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="ab74c-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="ab74c-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="ab74c-133">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ab74c-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="ab74c-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="ab74c-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="ab74c-135">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ab74c-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="ab74c-136">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="ab74c-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="ab74c-137">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="ab74c-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

