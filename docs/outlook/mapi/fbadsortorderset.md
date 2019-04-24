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
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336974"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="104a8-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="104a8-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="104a8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="104a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="104a8-105">Überprüft eine Sortierreihenfolge, die durch Überprüfen der Speicherbelegung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="104a8-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="104a8-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="104a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="104a8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="104a8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="104a8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="104a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="104a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="104a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="104a8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="104a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="104a8-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="104a8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="104a8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="104a8-112">Parameters</span></span>

 <span data-ttu-id="104a8-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="104a8-113">_lpsos_</span></span>
  
> <span data-ttu-id="104a8-114">in Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die zu validierende Sortierreihenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="104a8-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="104a8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="104a8-115">Return value</span></span>

<span data-ttu-id="104a8-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="104a8-116">TRUE</span></span> 
  
> <span data-ttu-id="104a8-117">Die angegebene Sortierreihenfolge ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="104a8-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="104a8-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="104a8-118">FALSE</span></span> 
  
> <span data-ttu-id="104a8-119">Der angegebene Sortierreihenfolge-Satz ist gültig.</span><span class="sxs-lookup"><span data-stu-id="104a8-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="104a8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="104a8-120">Remarks</span></span>

<span data-ttu-id="104a8-121">Die **FBadSortOrderSet** -Funktion kann verwendet werden, um einen Aufruf einer Sort-Methode wie der [IMAPITable:: sortable](imapitable-sorttable.md) -Methode vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="104a8-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

