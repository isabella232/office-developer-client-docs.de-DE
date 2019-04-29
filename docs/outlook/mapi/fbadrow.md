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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420619"
---
# <a name="fbadrow"></a><span data-ttu-id="a6b09-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="a6b09-103">FBadRow</span></span>

  
  
<span data-ttu-id="a6b09-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6b09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6b09-105">Überprüft eine Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a6b09-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6b09-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="a6b09-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6b09-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a6b09-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a6b09-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a6b09-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6b09-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a6b09-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a6b09-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a6b09-110">Called by:</span></span>  <br/> |<span data-ttu-id="a6b09-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a6b09-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="a6b09-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6b09-112">Parameters</span></span>

 <span data-ttu-id="a6b09-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="a6b09-113">_lprow_</span></span>
  
> <span data-ttu-id="a6b09-114">in Zeiger auf eine [SRow](srow.md) -Struktur, die die zu überprüfende Zeile identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a6b09-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6b09-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6b09-115">Return value</span></span>

<span data-ttu-id="a6b09-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="a6b09-116">TRUE</span></span> 
  
> <span data-ttu-id="a6b09-117">Die angegebene Zeile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a6b09-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="a6b09-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="a6b09-118">FALSE</span></span> 
  
> <span data-ttu-id="a6b09-119">Die angegebene Zeile ist gültig.</span><span class="sxs-lookup"><span data-stu-id="a6b09-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6b09-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6b09-120">See also</span></span>



[<span data-ttu-id="a6b09-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="a6b09-121">FBadRowSet</span></span>](fbadrowset.md)

