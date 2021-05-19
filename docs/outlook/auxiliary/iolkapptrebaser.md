---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Unterstützt das Neubasieren von Terminen in einem Kalenderordner.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410070"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="7e5d1-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="7e5d1-103">IOlkApptRebaser</span></span>

<span data-ttu-id="7e5d1-104">Unterstützt das Neubasieren von Terminen in einem Kalenderordner.</span><span class="sxs-lookup"><span data-stu-id="7e5d1-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7e5d1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7e5d1-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e5d1-106">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="7e5d1-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="7e5d1-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="7e5d1-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="7e5d1-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7e5d1-108">Header file:</span></span>  <br/> |<span data-ttu-id="7e5d1-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="7e5d1-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="7e5d1-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7e5d1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e5d1-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="7e5d1-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="7e5d1-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7e5d1-112">Called by:</span></span>  <br/> |<span data-ttu-id="7e5d1-113">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="7e5d1-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="7e5d1-114">Verfügbar gemacht für:</span><span class="sxs-lookup"><span data-stu-id="7e5d1-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="7e5d1-115">Outlook-Neubasierungsobjekt</span><span class="sxs-lookup"><span data-stu-id="7e5d1-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7e5d1-116">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="7e5d1-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e5d1-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="7e5d1-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="7e5d1-118">Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.</span><span class="sxs-lookup"><span data-stu-id="7e5d1-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="7e5d1-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="7e5d1-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="7e5d1-120">Termin-Enumeration in einem Kalenderordner Abschluss wartet, und gibt einer Liste von Terminen, müssen neuen Basisadressen.</span><span class="sxs-lookup"><span data-stu-id="7e5d1-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="7e5d1-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="7e5d1-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="7e5d1-122">Beginnt eine Aufgabe für die Terminumbasierung mit einer Liste von Terminen, die in der Regel von **EndEnumerateAppointments erhalten werden.**</span><span class="sxs-lookup"><span data-stu-id="7e5d1-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="7e5d1-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="7e5d1-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="7e5d1-124">Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.</span><span class="sxs-lookup"><span data-stu-id="7e5d1-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e5d1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e5d1-125">See also</span></span>

- [<span data-ttu-id="7e5d1-126">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="7e5d1-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

