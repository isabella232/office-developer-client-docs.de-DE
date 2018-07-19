---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791683"
---
# <a name="fbadrow"></a><span data-ttu-id="f17b1-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="f17b1-103">FBadRow</span></span>

  
  
<span data-ttu-id="f17b1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f17b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f17b1-105">Überprüft eine Zeile in einer Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="f17b1-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f17b1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f17b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="f17b1-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f17b1-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f17b1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f17b1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f17b1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f17b1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f17b1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f17b1-110">Called by:</span></span>  <br/> |<span data-ttu-id="f17b1-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f17b1-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="f17b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f17b1-112">Parameters</span></span>

 <span data-ttu-id="f17b1-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="f17b1-113">_lprow_</span></span>
  
> <span data-ttu-id="f17b1-114">[in] Zeiger auf eine [SRow](srow.md) -Struktur, die die Zeile zu überprüfenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f17b1-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f17b1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f17b1-115">Return value</span></span>

<span data-ttu-id="f17b1-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="f17b1-116">TRUE</span></span> 
  
> <span data-ttu-id="f17b1-117">Die angegebene Zeile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f17b1-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="f17b1-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="f17b1-118">FALSE</span></span> 
  
> <span data-ttu-id="f17b1-119">Die angegebene Zeile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f17b1-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f17b1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f17b1-120">See also</span></span>



[<span data-ttu-id="f17b1-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="f17b1-121">FBadRowSet</span></span>](fbadrowset.md)

