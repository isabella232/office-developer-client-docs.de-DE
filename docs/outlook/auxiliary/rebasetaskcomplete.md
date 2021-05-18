---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Meldet den Abschluss der Neubasierung von Terminen.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328322"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="195ac-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="195ac-103">RebaseTaskComplete</span></span>

<span data-ttu-id="195ac-104">Meldet den Abschluss der Neubasierung von Terminen.</span><span class="sxs-lookup"><span data-stu-id="195ac-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="195ac-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="195ac-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="195ac-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="195ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="195ac-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="195ac-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="195ac-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="195ac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="195ac-109">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="195ac-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="195ac-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="195ac-110">Called by:</span></span>  <br/> |<span data-ttu-id="195ac-111">Outlook-Neubasierungsobjekt</span><span class="sxs-lookup"><span data-stu-id="195ac-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="195ac-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="195ac-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="195ac-113">**PFNREBASETASKCOMPLETE** gemäß definition in tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="195ac-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="195ac-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="195ac-114">Parameters</span></span>

<span data-ttu-id="195ac-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="195ac-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="195ac-116">[in] Die Zeile, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="195ac-116">[in] The row that was processed.</span></span> <span data-ttu-id="195ac-117">Dieser Index bezieht sich auf die **[SRowSet-Struktur,](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** die an [IOlkApptRebaser::BeginRebaseAppointments übergeben wird.](iolkapptrebaser-beginrebaseappointments.md)</span><span class="sxs-lookup"><span data-stu-id="195ac-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="195ac-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="195ac-118">_pRowCur_</span></span>
  
> <span data-ttu-id="195ac-119">in] Ein Zeiger auf eine **[SRow-Struktur,](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** die das verarbeitete Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="195ac-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="195ac-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="195ac-120">_hrResult_</span></span>
  
> <span data-ttu-id="195ac-121">[in] Ein **HRESULT,** das das Ergebnis des Neubasierungsvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="195ac-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="195ac-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="195ac-122">_fModified_</span></span>
  
> <span data-ttu-id="195ac-123">[in] Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="195ac-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="195ac-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="195ac-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="195ac-125">[in] Gibt an, ob eine Besprechungsaktualisierungsnachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="195ac-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="195ac-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="195ac-126">_pError_</span></span>
  
> <span data-ttu-id="195ac-127">[in] Ein Zeiger auf eine **MAPIERROR-Struktur** mit erweiterten Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="195ac-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="195ac-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="195ac-128">Return values</span></span>

<span data-ttu-id="195ac-129">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="195ac-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="195ac-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="195ac-130">Remarks</span></span>

<span data-ttu-id="195ac-131">MAPI-Clientanwendungen, die die [IOlkApptRebaser-Schnittstelle](iolkapptrebaser.md) verwenden, implementieren diese Funktion, um den Abschluss von Elementupdates nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="195ac-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="195ac-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="195ac-132">See also</span></span>

- [<span data-ttu-id="195ac-133">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="195ac-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

