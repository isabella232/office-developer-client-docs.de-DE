---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407270"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="1a99c-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="1a99c-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="1a99c-104">Beginnt eine Aufgabe für die Enumeration der Termin im Kalenderordner Termine zu finden, die neuen Basisadressen benötigen.</span><span class="sxs-lookup"><span data-stu-id="1a99c-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1a99c-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1a99c-105">Quick info</span></span>

<span data-ttu-id="1a99c-106">Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="1a99c-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="1a99c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a99c-107">Parameters</span></span>

<span data-ttu-id="1a99c-108">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="1a99c-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="1a99c-p101">[in] Optional. Ein Zeiger auf ein Rebase-Funktion zum Fortschritt Task Status empfangen. **PFNREBASETASKPROGRESS** wird in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="1a99c-p101">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="1a99c-112">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="1a99c-112">_ppContext_</span></span>
  
> <span data-ttu-id="1a99c-p102">[out] Erforderlich. Ein Zeiger auf einen Zeiger auf den zurückgegebenen Kontext. Dieser Kontext wird an [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1a99c-p102">[out] Required. A pointer to a pointer to the returned context. This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1a99c-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1a99c-116">Return values</span></span>

<span data-ttu-id="1a99c-117">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1a99c-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a99c-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a99c-118">Remarks</span></span>

<span data-ttu-id="1a99c-119">Diese Aufgabe wird in einem neuen Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a99c-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a99c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a99c-120">See also</span></span>

- [<span data-ttu-id="1a99c-121">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="1a99c-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

