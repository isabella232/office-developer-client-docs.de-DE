---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Meldet den Status Enumeration und Neuzuordnen von Terminen.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384353"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="59bcb-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="59bcb-103">RebaseTaskProgress</span></span>

<span data-ttu-id="59bcb-104">Meldet den Status Enumeration und Neuzuordnen von Terminen.</span><span class="sxs-lookup"><span data-stu-id="59bcb-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="59bcb-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="59bcb-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59bcb-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="59bcb-106">Header file:</span></span>  <br/> |<span data-ttu-id="59bcb-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="59bcb-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="59bcb-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="59bcb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="59bcb-109">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="59bcb-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="59bcb-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="59bcb-110">Called by:</span></span>  <br/> |<span data-ttu-id="59bcb-111">Basisadressen Outlook-Objekt</span><span class="sxs-lookup"><span data-stu-id="59bcb-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="59bcb-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="59bcb-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="59bcb-113">**PFNREBASETASKPROGRESS** gemäß Definition im tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="59bcb-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="59bcb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="59bcb-114">Parameters</span></span>

<span data-ttu-id="59bcb-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="59bcb-115">_ulMin_</span></span>
  
> <span data-ttu-id="59bcb-116">[in] Niedrige Ende des Bereichs von Terminen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="59bcb-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="59bcb-117">Es ist normalerweise 0 (null).</span><span class="sxs-lookup"><span data-stu-id="59bcb-117">It is usually zero.</span></span>
    
<span data-ttu-id="59bcb-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="59bcb-118">_ulMax_</span></span>
  
> <span data-ttu-id="59bcb-119">[in] Hohe Ende des Bereichs von Terminen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="59bcb-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="59bcb-120">Es ist in der Regel die Anzahl der Elemente im Ordner "Kalender" verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="59bcb-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="59bcb-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="59bcb-121">_ulCur_</span></span>
  
> <span data-ttu-id="59bcb-122">[in] Das aktuelle Element verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="59bcb-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="59bcb-123">_State_</span><span class="sxs-lookup"><span data-stu-id="59bcb-123">_State_</span></span>
  
> <span data-ttu-id="59bcb-124">[in] Ein Wert, der den Status der das verarbeitete Element angibt.</span><span class="sxs-lookup"><span data-stu-id="59bcb-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="59bcb-125">Die **REBASE_APPT_STATE** -Enumeration wird in tzmovelib.h definiert.</span><span class="sxs-lookup"><span data-stu-id="59bcb-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="59bcb-126">_Zustand_ hat einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="59bcb-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="59bcb-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** – Scannen und Untersuchen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="59bcb-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="59bcb-128">**REBASE_APPT_STATE_SCANNING_FOUND** – Überprüfung und ein Element gefunden.</span><span class="sxs-lookup"><span data-stu-id="59bcb-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="59bcb-129">**REBASE_APPT_STATE_BEGIN** – behoben und Starten eines Elements.</span><span class="sxs-lookup"><span data-stu-id="59bcb-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="59bcb-130">**REBASE_APPT_STATE_REBASING** – behoben und Anpassen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="59bcb-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="59bcb-131">**REBASE_APPT_STATE_SENDING** – behoben und Senden einer Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="59bcb-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="59bcb-132">**REBASE_APPT_STATE_DONE** – korrigieren und mit einem Artikel fertig.</span><span class="sxs-lookup"><span data-stu-id="59bcb-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="59bcb-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="59bcb-133">_pRowCur_</span></span>
  
> <span data-ttu-id="59bcb-134">[in] Ein Zeiger auf eine **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die das Element überprüften oder feste beschreibt.</span><span class="sxs-lookup"><span data-stu-id="59bcb-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="59bcb-135">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="59bcb-135">Return values</span></span>

<span data-ttu-id="59bcb-136">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="59bcb-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59bcb-137">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="59bcb-137">Remarks</span></span>

<span data-ttu-id="59bcb-138">MAPI-Clientanwendungen, die verwenden die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle, implementieren Sie diese Funktion, um die Verarbeitung des Elements zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="59bcb-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59bcb-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59bcb-139">See also</span></span>

- [<span data-ttu-id="59bcb-140">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="59bcb-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

