---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412380"
---
# <a name="fnidle"></a><span data-ttu-id="8f9aa-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="8f9aa-103">FNIDLE</span></span>
 
<span data-ttu-id="8f9aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f9aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f9aa-105">Definiert eine Leerlauf Routine, die vom MAPI-Leerlauf Modul regelmäßig gemäß der Priorität aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f9aa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8f9aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="8f9aa-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8f9aa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8f9aa-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8f9aa-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="8f9aa-109">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8f9aa-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="8f9aa-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8f9aa-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="8f9aa-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8f9aa-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="8f9aa-112">EntSprechender Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="8f9aa-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="8f9aa-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="8f9aa-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="8f9aa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f9aa-114">Parameters</span></span>

 <span data-ttu-id="8f9aa-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="8f9aa-115">_lpvContext_</span></span>
  
> <span data-ttu-id="8f9aa-116">in Zeiger auf einen Speicherblock, der von MAPI bei jedem Aufruf an die Leerlauf Routine übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="8f9aa-117">Dieser Zeiger wird im _pvIdleParam_ -Parameter von [FTGREGISTERIDLEROUTINE](ftgregisteridleroutine.md)an das MAPI-Leerlauf Modul übergeben.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="8f9aa-118">Die Daten im Speicherblock können Kontext für den Aufruf der Leerlauf Routine bereitstellen, beispielsweise das zu verwendende Objekt oder den aktuellen Status eines langwierigen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f9aa-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f9aa-119">Return value</span></span>

<span data-ttu-id="8f9aa-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="8f9aa-120">FALSE</span></span> 
  
> <span data-ttu-id="8f9aa-121">Eine Leerlauf Routine mit dem **FNIDLE** -Prototyp sollte immer false zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8f9aa-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f9aa-122">Remarks</span></span>

<span data-ttu-id="8f9aa-123">Die spezifische Funktionalität der Leerlauf Routine wird von der implementierenden Clientanwendung oder dem Dienstanbieter bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="8f9aa-124">Der Client oder Anbieter muss die Ausführungszeit der einzelnen Zustände einer Leerlauf Routine einschränken.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="8f9aa-125">Jeder Status sollte eine minimale Verarbeitung durchführen, den aktuellen Status in den Kontextdaten aktualisieren, auf die von _lpvContext_verwiesen wird, und zum MAPI-Leerlauf Modul zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="8f9aa-126">Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor er seine eigene Leerlauf Routine mit einem Aufruf der [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) -Funktion registrieren kann.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="8f9aa-127">Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem FNIDLE-Funktionsprototyp basieren:</span><span class="sxs-lookup"><span data-stu-id="8f9aa-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="8f9aa-128">**Leerlauf Routine Funktion**</span><span class="sxs-lookup"><span data-stu-id="8f9aa-128">**Idle routine function**</span></span>|<span data-ttu-id="8f9aa-129">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="8f9aa-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f9aa-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="8f9aa-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="8f9aa-131">Ändert die Eigenschaften einer registrierten Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="8f9aa-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="8f9aa-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="8f9aa-133">Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="8f9aa-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="8f9aa-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="8f9aa-135">Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="8f9aa-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="8f9aa-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="8f9aa-137">Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="8f9aa-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="8f9aa-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="8f9aa-139">Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="8f9aa-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="8f9aa-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="8f9aa-141">Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="8f9aa-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="8f9aa-143">Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="8f9aa-144">Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

