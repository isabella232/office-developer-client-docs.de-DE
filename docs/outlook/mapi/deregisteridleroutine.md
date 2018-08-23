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
ms.openlocfilehash: 78d499dabe60a8051c6a2a77abad4b7d6f2ed159
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591954"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="40a46-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="40a46-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="40a46-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40a46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40a46-105">Entfernt eine [FNIDLE](fnidle.md) basierend im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="40a46-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40a46-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="40a46-106">Header file:</span></span>  <br/> |<span data-ttu-id="40a46-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="40a46-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="40a46-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="40a46-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="40a46-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="40a46-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="40a46-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="40a46-110">Called by:</span></span>  <br/> |<span data-ttu-id="40a46-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="40a46-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="40a46-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="40a46-112">Parameters</span></span>

 <span data-ttu-id="40a46-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="40a46-113">_ftg_</span></span>
  
> <span data-ttu-id="40a46-114">[in] Funktion-Tag zur Identifizierung der im Leerlauf Routine entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40a46-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40a46-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40a46-115">Return value</span></span>

<span data-ttu-id="40a46-116">None.</span><span class="sxs-lookup"><span data-stu-id="40a46-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40a46-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="40a46-117">Remarks</span></span>

<span data-ttu-id="40a46-118">Jede Aufgabe in einer Clientanwendung oder Dienstanbieter kann eine beliebige im Leerlauf Routine Aufheben der Registrierung für den sie einen gültigen _Ftg_ Parameter verfügt.</span><span class="sxs-lookup"><span data-stu-id="40a46-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="40a46-119">Insbesondere kann eine im Leerlauf Routine selbst Aufheben der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="40a46-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="40a46-120">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="40a46-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="40a46-121">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="40a46-121">**Idle routine function**</span></span>|<span data-ttu-id="40a46-122">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="40a46-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40a46-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="40a46-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="40a46-124">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="40a46-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="40a46-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="40a46-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="40a46-126">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="40a46-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="40a46-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="40a46-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="40a46-128">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="40a46-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="40a46-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="40a46-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="40a46-130">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="40a46-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="40a46-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="40a46-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="40a46-132">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="40a46-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="40a46-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="40a46-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="40a46-134">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="40a46-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="40a46-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40a46-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="40a46-136">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="40a46-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="40a46-137">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="40a46-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="40a46-138">Nachdem die im Leerlauf Routine aufgehoben wird, wird das Modul im Leerlauf nicht erneut aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="40a46-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="40a46-139">Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke freigeben an die dieser Zeiger in seiner ursprünglichen Aufruf der Funktion **FtgRegisterIdleRoutine** verwenden, die im Leerlauf Engine übergeben.</span><span class="sxs-lookup"><span data-stu-id="40a46-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

