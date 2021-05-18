---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Termin-Enumeration in einem Kalenderordner Abschluss wartet, und gibt einer Liste von Terminen, müssen neuen Basisadressen.
ms.openlocfilehash: 5be6fd9ce33374725b36429cd0fbc717776c9ab9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321903"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="9dfd1-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="9dfd1-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="9dfd1-104">Termin-Enumeration in einem Kalenderordner Abschluss wartet, und gibt einer Liste von Terminen, müssen neuen Basisadressen.</span><span class="sxs-lookup"><span data-stu-id="9dfd1-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9dfd1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9dfd1-105">Quick info</span></span>

<span data-ttu-id="9dfd1-106">Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="9dfd1-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="9dfd1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dfd1-107">Parameters</span></span>

<span data-ttu-id="9dfd1-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="9dfd1-108">_pContext_</span></span>
  
> <span data-ttu-id="9dfd1-p101">[in] Erforderlich. Ein Zeiger auf den Kontext von einem vorherigen Aufruf von [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9dfd1-p101">[in] Required. A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="9dfd1-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="9dfd1-111">_phResult_</span></span>
  
> <span data-ttu-id="9dfd1-p102">[out] Erforderlich. Ein Zeiger auf ein **HRESULT** zum Abrufen der Ergebnisse der Enumeration-Operation.</span><span class="sxs-lookup"><span data-stu-id="9dfd1-p102">[out] Required. A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="9dfd1-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="9dfd1-114">_ppError_</span></span>
  
> <span data-ttu-id="9dfd1-p103">[out] Optional. Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, um erweiterte Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9dfd1-p103">[out] Optional. A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="9dfd1-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="9dfd1-117">_ppRows_</span></span>
  
> <span data-ttu-id="9dfd1-p104">[out] Erforderlich. Ein Zeiger auf einen Zeiger auf eine [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) -Struktur, die beschreibt, die Termine, die neuen Basisadressen. Diese Struktur wird in der Regel an [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9dfd1-p104">[out] Required. A pointer to a pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9dfd1-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9dfd1-121">Return values</span></span>

<span data-ttu-id="9dfd1-122">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9dfd1-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9dfd1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dfd1-123">See also</span></span>

- [<span data-ttu-id="9dfd1-124">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="9dfd1-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

