---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Beginnt eine neue Aufgabe für neuen Termin Basisadressen anhand einer Liste von Terminen, die in der Regel von IOlkApptRebaser::EndEnumerateAppointmentsabgerufen.
ms.openlocfilehash: f0f2377f30de7688aaa4196e3a046c664c2128aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321910"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="63cd9-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="63cd9-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="63cd9-104">Beginnt eine neue Aufgabe für neuen Termin Basisadressen anhand einer Liste von Terminen, die in der Regel von [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63cd9-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="63cd9-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="63cd9-105">Quick info</span></span>

<span data-ttu-id="63cd9-106">Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="63cd9-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="63cd9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="63cd9-107">Parameters</span></span>

<span data-ttu-id="63cd9-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="63cd9-108">_pRows_</span></span>
  
> <span data-ttu-id="63cd9-p101">[in] Erforderlich. Ein Zeiger auf eine [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) -Struktur, die beschreibt, die Termine, die neuen Basisadressen. Diese Struktur wird in der Regel von einem vorherigen Aufruf von [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="63cd9-p101">[in] Required. A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="63cd9-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="63cd9-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="63cd9-p102">[in] Optional. Ein Zeiger auf ein Rebase-Funktion zum Fortschritt Task Status empfangen. **PFNREBASETASKPROGRESS** wird in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="63cd9-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="63cd9-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="63cd9-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="63cd9-p103">[out] Optional. Ein Zeiger auf eine Funktion Rebase Task Abschluss über Rebase Abschluss benachrichtigt. **PFNREBASETASKCOMPLETE** wird in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="63cd9-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="63cd9-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="63cd9-120">_ppContext_</span></span>
  
> <span data-ttu-id="63cd9-p104">[out] Erforderlich. Ein Zeiger auf einen Zeiger auf den zurückgegebenen Kontext. Dieser Kontext wird in der Regel an [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="63cd9-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="63cd9-124">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="63cd9-124">Return values</span></span>

<span data-ttu-id="63cd9-125">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="63cd9-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63cd9-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63cd9-126">Remarks</span></span>

<span data-ttu-id="63cd9-127">Diese Aufgabe wird in einem neuen Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63cd9-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63cd9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63cd9-128">See also</span></span>

- [<span data-ttu-id="63cd9-129">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="63cd9-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

