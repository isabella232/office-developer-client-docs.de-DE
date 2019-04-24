---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Fortschritt für die Aufzählung und die Begründung von Terminen.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326453"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="15754-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="15754-103">RebaseTaskProgress</span></span>

<span data-ttu-id="15754-104">Meldet den Fortschritt für die Aufzählung und die Begründung von Terminen.</span><span class="sxs-lookup"><span data-stu-id="15754-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="15754-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="15754-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15754-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="15754-106">Header file:</span></span>  <br/> |<span data-ttu-id="15754-107">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="15754-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="15754-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="15754-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="15754-109">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="15754-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="15754-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="15754-110">Called by:</span></span>  <br/> |<span data-ttu-id="15754-111">Outlook-Objekt wird erneut basiert</span><span class="sxs-lookup"><span data-stu-id="15754-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="15754-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="15754-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="15754-113">**PFNREBASETASKPROGRESS** wie in tzmovelib. h definiert</span><span class="sxs-lookup"><span data-stu-id="15754-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="15754-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="15754-114">Parameters</span></span>

<span data-ttu-id="15754-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="15754-115">_ulMin_</span></span>
  
> <span data-ttu-id="15754-116">in Das untere Ende des Bereiches der zu verarbeitenden Termine.</span><span class="sxs-lookup"><span data-stu-id="15754-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="15754-117">Es ist normalerweise Null.</span><span class="sxs-lookup"><span data-stu-id="15754-117">It is usually zero.</span></span>
    
<span data-ttu-id="15754-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="15754-118">_ulMax_</span></span>
  
> <span data-ttu-id="15754-119">in Das obere Ende des Bereiches der zu verarbeitenden Termine.</span><span class="sxs-lookup"><span data-stu-id="15754-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="15754-120">In der Regel wird die Anzahl der Elemente im Kalenderordner verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="15754-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="15754-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="15754-121">_ulCur_</span></span>
  
> <span data-ttu-id="15754-122">in Das aktuelle Element, das verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="15754-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="15754-123">_State_</span><span class="sxs-lookup"><span data-stu-id="15754-123">_State_</span></span>
  
> <span data-ttu-id="15754-124">in Ein Wert, der den Status des zu verarbeitenden Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="15754-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="15754-125">Die Aufzählung **REBASE_APPT_STATE** ist in tzmovelib. h definiert.</span><span class="sxs-lookup"><span data-stu-id="15754-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="15754-126">_State_ hat einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="15754-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="15754-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** – überprüfen und untersuchen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="15754-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="15754-128">**REBASE_APPT_STATE_SCANNING_FOUND** – ein Element wird gescannt und gefunden.</span><span class="sxs-lookup"><span data-stu-id="15754-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="15754-129">**REBASE_APPT_STATE_BEGIN** – fixieren und Starten eines Elements.</span><span class="sxs-lookup"><span data-stu-id="15754-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="15754-130">**REBASE_APPT_STATE_REBASING** – Behebung und Anpassung eines Elements.</span><span class="sxs-lookup"><span data-stu-id="15754-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="15754-131">**REBASE_APPT_STATE_SENDING** – Behebung und Senden eines Besprechungs Updates.</span><span class="sxs-lookup"><span data-stu-id="15754-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="15754-132">**REBASE_APPT_STATE_DONE** – Behebung und fertig mit einem Element.</span><span class="sxs-lookup"><span data-stu-id="15754-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="15754-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="15754-133">_pRowCur_</span></span>
  
> <span data-ttu-id="15754-134">in Ein Zeiger auf eine **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die das Element beschreibt, das überprüft oder korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="15754-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="15754-135">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="15754-135">Return values</span></span>

<span data-ttu-id="15754-136">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="15754-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15754-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15754-137">Remarks</span></span>

<span data-ttu-id="15754-138">MAPI-Clientanwendungen, die die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle verwenden, implementieren diese Funktion, um die Elementverarbeitung nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="15754-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15754-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15754-139">See also</span></span>

- [<span data-ttu-id="15754-140">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="15754-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

