---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791664"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="38a48-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="38a48-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="38a48-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38a48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38a48-105">Überprüft eine Sortierreihenfolge festlegen, indem Sie die Zuweisung von virtuellem Speicher überprüfen.</span><span class="sxs-lookup"><span data-stu-id="38a48-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38a48-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="38a48-106">Header file:</span></span>  <br/> |<span data-ttu-id="38a48-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="38a48-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="38a48-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="38a48-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38a48-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38a48-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38a48-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="38a48-110">Called by:</span></span>  <br/> |<span data-ttu-id="38a48-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="38a48-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="38a48-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="38a48-112">Parameters</span></span>

 <span data-ttu-id="38a48-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="38a48-113">_lpsos_</span></span>
  
> <span data-ttu-id="38a48-114">[in] Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierreihenfolge festlegen zu überprüfenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38a48-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38a48-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="38a48-115">Return value</span></span>

<span data-ttu-id="38a48-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="38a48-116">TRUE</span></span> 
  
> <span data-ttu-id="38a48-117">Die angegebene sortieren Reihenfolge Gruppe ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="38a48-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="38a48-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="38a48-118">FALSE</span></span> 
  
> <span data-ttu-id="38a48-119">Der angegebene sortieren Reihenfolge ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="38a48-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38a48-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38a48-120">Remarks</span></span>

<span data-ttu-id="38a48-121">Die **FBadSortOrderSet** -Funktion kann zur Vorbereitung eines Anrufs an eine Sortiermethode wie der [SortTable](imapitable-sorttable.md) -Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38a48-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

