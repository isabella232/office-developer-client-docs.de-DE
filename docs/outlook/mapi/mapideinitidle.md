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
ms.openlocfilehash: 4eaeb3338c95196ff346c5098e5d06371b00bc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793114"
---
# <a name="mapideinitidle"></a><span data-ttu-id="00c60-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="00c60-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="00c60-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00c60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00c60-105">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="00c60-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00c60-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="00c60-106">Header file:</span></span>  <br/> |<span data-ttu-id="00c60-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="00c60-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="00c60-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="00c60-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="00c60-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="00c60-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="00c60-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="00c60-110">Called by:</span></span>  <br/> |<span data-ttu-id="00c60-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="00c60-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="00c60-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00c60-112">Parameters</span></span>

<span data-ttu-id="00c60-113">None.</span><span class="sxs-lookup"><span data-stu-id="00c60-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="00c60-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00c60-114">Return value</span></span>

<span data-ttu-id="00c60-115">None.</span><span class="sxs-lookup"><span data-stu-id="00c60-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00c60-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00c60-116">Remarks</span></span>

<span data-ttu-id="00c60-117">Eine Clientanwendung oder Dienstanbieter sollte **MAPIDeInitIdle** aufrufen, wenn er nicht mehr das Modul im Leerlauf, beispielsweise benötigt bei Beenden der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="00c60-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="00c60-118">Jedem Aufruf von [MAPIInitIdle](mapiinitidle.md) muss durch einen nachfolgenden Aufruf von **MAPIDeInitIdle**abgeglichen werden, oder das Modul im Leerlauf verläuft von Links für die aufrufende Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00c60-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="00c60-119">Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp:</span><span class="sxs-lookup"><span data-stu-id="00c60-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="00c60-120">**Im Leerlauf routinemäßige-Funktion**</span><span class="sxs-lookup"><span data-stu-id="00c60-120">**Idle routine function**</span></span>|<span data-ttu-id="00c60-121">**Nutzung**</span><span class="sxs-lookup"><span data-stu-id="00c60-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00c60-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="00c60-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="00c60-123">Ändert die Eigenschaften einer registrierten im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="00c60-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="00c60-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="00c60-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="00c60-125">Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.</span><span class="sxs-lookup"><span data-stu-id="00c60-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="00c60-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="00c60-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="00c60-127">Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.</span><span class="sxs-lookup"><span data-stu-id="00c60-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="00c60-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="00c60-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="00c60-129">Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.</span><span class="sxs-lookup"><span data-stu-id="00c60-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="00c60-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="00c60-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="00c60-131">Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="00c60-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="00c60-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="00c60-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="00c60-133">Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.</span><span class="sxs-lookup"><span data-stu-id="00c60-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="00c60-134">Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="00c60-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="00c60-135">Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität.</span><span class="sxs-lookup"><span data-stu-id="00c60-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

