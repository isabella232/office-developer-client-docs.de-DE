---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Fortschritt für die Aufzählung und Neubasierung von Terminen.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326453"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="a1902-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="a1902-103">RebaseTaskProgress</span></span>

<span data-ttu-id="a1902-104">Meldet den Fortschritt für die Aufzählung und Neubasierung von Terminen.</span><span class="sxs-lookup"><span data-stu-id="a1902-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a1902-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a1902-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1902-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a1902-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1902-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="a1902-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="a1902-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a1902-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1902-109">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="a1902-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="a1902-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a1902-110">Called by:</span></span>  <br/> |<span data-ttu-id="a1902-111">Outlook-Neubasierungsobjekt</span><span class="sxs-lookup"><span data-stu-id="a1902-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="a1902-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="a1902-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="a1902-113">**PFNREBASETASKPROGRESS** gemäß definition in tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="a1902-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="a1902-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1902-114">Parameters</span></span>

<span data-ttu-id="a1902-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="a1902-115">_ulMin_</span></span>
  
> <span data-ttu-id="a1902-116">[in] Das niedrige Ende des zu verarbeitenden Terminbereichs.</span><span class="sxs-lookup"><span data-stu-id="a1902-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="a1902-117">In der Regel ist es null.</span><span class="sxs-lookup"><span data-stu-id="a1902-117">It is usually zero.</span></span>
    
<span data-ttu-id="a1902-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="a1902-118">_ulMax_</span></span>
  
> <span data-ttu-id="a1902-119">[in] Das hohe Ende des zu verarbeitenden Terminbereichs.</span><span class="sxs-lookup"><span data-stu-id="a1902-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="a1902-120">Dies ist in der Regel die Anzahl der Elemente im zu verarbeitende Kalenderordner.</span><span class="sxs-lookup"><span data-stu-id="a1902-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="a1902-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="a1902-121">_ulCur_</span></span>
  
> <span data-ttu-id="a1902-122">[in] Das aktuelle Element, das verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a1902-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="a1902-123">_State_</span><span class="sxs-lookup"><span data-stu-id="a1902-123">_State_</span></span>
  
> <span data-ttu-id="a1902-124">[in] Ein Wert, der den Status des verarbeiteten Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="a1902-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="a1902-125">Die Enumeration **REBASE_APPT_STATE** in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="a1902-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="a1902-126">_State_ hat einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="a1902-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="a1902-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** – Scannen und Untersuchen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="a1902-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="a1902-128">**REBASE_APPT_STATE_SCANNING_FOUND** – Ein Element wurde gescannt und gefunden.</span><span class="sxs-lookup"><span data-stu-id="a1902-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="a1902-129">**REBASE_APPT_STATE_BEGIN** – Fixieren und Starten eines Elements.</span><span class="sxs-lookup"><span data-stu-id="a1902-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="a1902-130">**REBASE_APPT_STATE_REBASING** – Fixieren und Anpassen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="a1902-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="a1902-131">**REBASE_APPT_STATE_SENDING** – Beheben und Senden eines Besprechungsupdates.</span><span class="sxs-lookup"><span data-stu-id="a1902-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="a1902-132">**REBASE_APPT_STATE_DONE** – Fixieren und Fertig mit einem Element.</span><span class="sxs-lookup"><span data-stu-id="a1902-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="a1902-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="a1902-133">_pRowCur_</span></span>
  
> <span data-ttu-id="a1902-134">[in] Ein Zeiger auf eine **[SRow-Struktur,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** die das gescannte oder feste Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a1902-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a1902-135">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a1902-135">Return values</span></span>

<span data-ttu-id="a1902-136">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a1902-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1902-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1902-137">Remarks</span></span>

<span data-ttu-id="a1902-138">MAPI-Clientanwendungen, die die [IOlkApptRebaser-Schnittstelle](iolkapptrebaser.md) verwenden, implementieren diese Funktion, um die Elementverarbeitung nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="a1902-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1902-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1902-139">See also</span></span>

- [<span data-ttu-id="a1902-140">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="a1902-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

