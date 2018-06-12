---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Beginnt eine neue Aufgabe für neuen Termin Basisadressen anhand einer Liste von Terminen, die in der Regel von IOlkApptRebaser::EndEnumerateAppointmentsabgerufen.
ms.openlocfilehash: 2becb305eebe448e2adecf91c2a111f86d97fe50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791127"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="1d2df-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="1d2df-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="1d2df-104">Beginnt eine neue Aufgabe für neuen Termin Basisadressen anhand einer Liste von Terminen, die in der Regel von [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d2df-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1d2df-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1d2df-105">Quick info</span></span>

<span data-ttu-id="1d2df-106">Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="1d2df-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="1d2df-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d2df-107">Parameters</span></span>

<span data-ttu-id="1d2df-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="1d2df-108">_pRows_</span></span>
  
> <span data-ttu-id="1d2df-p101">[in] Erforderlich. Ein Zeiger auf eine [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) -Struktur, die beschreibt, die Termine, die neuen Basisadressen. Diese Struktur wird in der Regel von einem vorherigen Aufruf von [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d2df-p101">[in] Required. A pointer to an [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="1d2df-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="1d2df-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="1d2df-p102">[in] Optional. Ein Zeiger auf ein Rebase-Funktion zum Fortschritt Task Status empfangen. **PFNREBASETASKPROGRESS** wird in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="1d2df-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="1d2df-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="1d2df-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="1d2df-p103">[out] Optional. Ein Zeiger auf eine Funktion Rebase Task Abschluss über Rebase Abschluss benachrichtigt. **PFNREBASETASKCOMPLETE** wird in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="1d2df-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="1d2df-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="1d2df-120">_ppContext_</span></span>
  
> <span data-ttu-id="1d2df-p104">[out] Erforderlich. Ein Zeiger auf einen Zeiger auf den zurückgegebenen Kontext. Dieser Kontext wird in der Regel an [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1d2df-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1d2df-124">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1d2df-124">Return values</span></span>

<span data-ttu-id="1d2df-125">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1d2df-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d2df-126">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="1d2df-126">Remarks</span></span>

<span data-ttu-id="1d2df-127">Diese Aufgabe wird in einem neuen Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d2df-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d2df-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d2df-128">See also</span></span>

- [<span data-ttu-id="1d2df-129">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="1d2df-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

