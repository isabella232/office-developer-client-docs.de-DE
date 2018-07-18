---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Neuzuordnen von Terminen in einem Kalenderordner unterstützt.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791115"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="8e824-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="8e824-103">IOlkApptRebaser</span></span>

<span data-ttu-id="8e824-104">Neuzuordnen von Terminen in einem Kalenderordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e824-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8e824-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8e824-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e824-106">Erbt:</span><span class="sxs-lookup"><span data-stu-id="8e824-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="8e824-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="8e824-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="8e824-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8e824-108">Header file:</span></span>  <br/> |<span data-ttu-id="8e824-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="8e824-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="8e824-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8e824-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8e824-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="8e824-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="8e824-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8e824-112">Called by:</span></span>  <br/> |<span data-ttu-id="8e824-113">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="8e824-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="8e824-114">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="8e824-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="8e824-115">Basisadressen Outlook-Objekt</span><span class="sxs-lookup"><span data-stu-id="8e824-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8e824-116">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8e824-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e824-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="8e824-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="8e824-118">Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.</span><span class="sxs-lookup"><span data-stu-id="8e824-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="8e824-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="8e824-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="8e824-120">Termin-Enumeration in einem Kalenderordner Abschluss wartet, und gibt einer Liste von Terminen, müssen neuen Basisadressen.</span><span class="sxs-lookup"><span data-stu-id="8e824-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="8e824-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="8e824-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="8e824-122">Beginnt mit einer Aufgabe zum Termin Neuzuordnen anhand einer Liste von Terminen, in der Regel von **EndEnumerateAppointments**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8e824-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="8e824-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="8e824-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="8e824-124">Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.</span><span class="sxs-lookup"><span data-stu-id="8e824-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e824-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e824-125">See also</span></span>

- [<span data-ttu-id="8e824-126">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="8e824-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

