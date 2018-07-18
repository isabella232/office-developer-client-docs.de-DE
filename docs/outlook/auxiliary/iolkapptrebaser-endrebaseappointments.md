---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791123"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="7a1a7-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="7a1a7-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="7a1a7-104">Führen Sie neuen Basisadressen Termin wartet, und ruft die Ergebnisse ab.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7a1a7-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7a1a7-105">Quick info</span></span>

<span data-ttu-id="7a1a7-106">Finden Sie unter [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="7a1a7-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="7a1a7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a1a7-107">Parameters</span></span>

<span data-ttu-id="7a1a7-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="7a1a7-108">_pContext_</span></span>
  
> <span data-ttu-id="7a1a7-p101">[in] Erforderlich. Ein Zeiger auf den Kontext von einem Aufruf von [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="7a1a7-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="7a1a7-111">_phResult_</span></span>
  
> <span data-ttu-id="7a1a7-p102">[out] Erforderlich. Ein Zeiger auf ein **HRESULT** zum Abrufen des Ergebnisses des Vorgangs Basisadressen.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7a1a7-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7a1a7-114">Return values</span></span>

<span data-ttu-id="7a1a7-115">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7a1a7-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a1a7-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a1a7-116">See also</span></span>

- [<span data-ttu-id="7a1a7-117">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="7a1a7-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

