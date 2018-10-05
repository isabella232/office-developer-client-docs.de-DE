---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Berichte Abschluss zum Neuzuordnen von Terminen.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388917"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="f0d9d-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="f0d9d-103">RebaseTaskComplete</span></span>

<span data-ttu-id="f0d9d-104">Berichte Abschluss zum Neuzuordnen von Terminen.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f0d9d-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f0d9d-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0d9d-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="f0d9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0d9d-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="f0d9d-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="f0d9d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f0d9d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f0d9d-109">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="f0d9d-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="f0d9d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f0d9d-110">Called by:</span></span>  <br/> |<span data-ttu-id="f0d9d-111">Basisadressen Outlook-Objekt</span><span class="sxs-lookup"><span data-stu-id="f0d9d-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="f0d9d-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="f0d9d-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="f0d9d-113">**PFNREBASETASKCOMPLETE** gemäß Definition im tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="f0d9d-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="f0d9d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0d9d-114">Parameters</span></span>

<span data-ttu-id="f0d9d-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="f0d9d-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="f0d9d-116">[in] Die Zeile, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-116">[in] The row that was processed.</span></span> <span data-ttu-id="f0d9d-117">Dieser Index bezieht sich auf die **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** Struktur [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="f0d9d-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="f0d9d-118">_pRowCur_</span></span>
  
> <span data-ttu-id="f0d9d-119">[in] ein Zeiger auf eine **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die Beschreibung des Artikels, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="f0d9d-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="f0d9d-120">_hrResult_</span></span>
  
> <span data-ttu-id="f0d9d-121">[in] Ein **HRESULT** zurück, der das Ergebnis des Vorgangs Basisadressen angibt.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="f0d9d-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="f0d9d-122">_fModified_</span></span>
  
> <span data-ttu-id="f0d9d-123">[in] Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="f0d9d-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="f0d9d-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="f0d9d-125">[in] Gibt an, ob die Aktualisierung einer Besprechungsanfrage Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="f0d9d-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="f0d9d-126">_pError_</span></span>
  
> <span data-ttu-id="f0d9d-127">[in] Ein Zeiger auf eine **MAPIERROR** -Struktur mit erweiterten Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f0d9d-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f0d9d-128">Return values</span></span>

<span data-ttu-id="f0d9d-129">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0d9d-130">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="f0d9d-130">Remarks</span></span>

<span data-ttu-id="f0d9d-131">MAPI-Clientanwendungen, die verwenden die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle, implementieren Sie diese Funktion zum Abschluss des elementupdates nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="f0d9d-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0d9d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0d9d-132">See also</span></span>

- [<span data-ttu-id="f0d9d-133">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="f0d9d-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

