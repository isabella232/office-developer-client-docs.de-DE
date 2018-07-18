---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Berichte Abschluss zum Neuzuordnen von Terminen.
ms.openlocfilehash: 735d875b4151c86103a1ac0378bd33b84de64997
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791212"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="cef1b-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="cef1b-103">RebaseTaskComplete</span></span>

<span data-ttu-id="cef1b-104">Berichte Abschluss zum Neuzuordnen von Terminen.</span><span class="sxs-lookup"><span data-stu-id="cef1b-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cef1b-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cef1b-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cef1b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cef1b-106">Header file:</span></span>  <br/> |<span data-ttu-id="cef1b-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="cef1b-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="cef1b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="cef1b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cef1b-109">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="cef1b-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="cef1b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="cef1b-110">Called by:</span></span>  <br/> |<span data-ttu-id="cef1b-111">Basisadressen Outlook-Objekt</span><span class="sxs-lookup"><span data-stu-id="cef1b-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="cef1b-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="cef1b-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="cef1b-113">**PFNREBASETASKCOMPLETE** gemäß Definition im tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="cef1b-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="cef1b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cef1b-114">Parameters</span></span>

<span data-ttu-id="cef1b-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="cef1b-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="cef1b-116">[in] Die Zeile, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cef1b-116">[in] The row that was processed.</span></span> <span data-ttu-id="cef1b-117">Dieser Index bezieht sich auf die **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** Struktur [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="cef1b-117">This index refers to the **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="cef1b-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="cef1b-118">_pRowCur_</span></span>
  
> <span data-ttu-id="cef1b-119">[in] ein Zeiger auf eine **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** -Struktur, die Beschreibung des Artikels, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cef1b-119">in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="cef1b-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="cef1b-120">_hrResult_</span></span>
  
> <span data-ttu-id="cef1b-121">[in] Ein **HRESULT** zurück, der das Ergebnis des Vorgangs Basisadressen angibt.</span><span class="sxs-lookup"><span data-stu-id="cef1b-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="cef1b-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="cef1b-122">_fModified_</span></span>
  
> <span data-ttu-id="cef1b-123">[in] Gibt an, ob das Element geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cef1b-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="cef1b-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="cef1b-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="cef1b-125">[in] Gibt an, ob die Aktualisierung einer Besprechungsanfrage Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cef1b-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="cef1b-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="cef1b-126">_pError_</span></span>
  
> <span data-ttu-id="cef1b-127">[in] Ein Zeiger auf eine **MAPIERROR** -Struktur mit erweiterten Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="cef1b-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="cef1b-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cef1b-128">Return values</span></span>

<span data-ttu-id="cef1b-129">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cef1b-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cef1b-130">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="cef1b-130">Remarks</span></span>

<span data-ttu-id="cef1b-131">MAPI-Clientanwendungen, die verwenden die [IOlkApptRebaser](iolkapptrebaser.md) -Schnittstelle, implementieren Sie diese Funktion zum Abschluss des elementupdates nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="cef1b-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cef1b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cef1b-132">See also</span></span>

- [<span data-ttu-id="cef1b-133">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="cef1b-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

