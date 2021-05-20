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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428459"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="ba273-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ba273-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="ba273-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba273-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba273-105">Überprüft eine Sortierreihenfolge, indem die Speicherzuordnung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="ba273-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba273-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="ba273-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba273-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ba273-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ba273-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ba273-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba273-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba273-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ba273-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ba273-110">Called by:</span></span>  <br/> |<span data-ttu-id="ba273-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="ba273-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="ba273-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba273-112">Parameters</span></span>

 <span data-ttu-id="ba273-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="ba273-113">_lpsos_</span></span>
  
> <span data-ttu-id="ba273-114">[in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die zu überprüfende Sortierreihenfolge identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba273-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ba273-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba273-115">Return value</span></span>

<span data-ttu-id="ba273-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="ba273-116">TRUE</span></span> 
  
> <span data-ttu-id="ba273-117">Der angegebene Sortierreihenfolgensatz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba273-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="ba273-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="ba273-118">FALSE</span></span> 
  
> <span data-ttu-id="ba273-119">Der angegebene Sortierreihenfolgensatz ist gültig.</span><span class="sxs-lookup"><span data-stu-id="ba273-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba273-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba273-120">Remarks</span></span>

<span data-ttu-id="ba273-121">Die **FBadSortOrderSet-Funktion** kann verwendet werden, um einen Aufruf einer Sortiermethode wie der [IMAPITable::SortTable-Methode vorzubereiten.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="ba273-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

