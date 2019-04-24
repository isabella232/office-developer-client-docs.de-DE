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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340957"
---
# <a name="fbadrow"></a><span data-ttu-id="af3a5-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="af3a5-103">FBadRow</span></span>

  
  
<span data-ttu-id="af3a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af3a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af3a5-105">Überprüft eine Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="af3a5-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af3a5-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="af3a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="af3a5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="af3a5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="af3a5-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="af3a5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="af3a5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="af3a5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="af3a5-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="af3a5-110">Called by:</span></span>  <br/> |<span data-ttu-id="af3a5-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="af3a5-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="af3a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="af3a5-112">Parameters</span></span>

 <span data-ttu-id="af3a5-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="af3a5-113">_lprow_</span></span>
  
> <span data-ttu-id="af3a5-114">in Zeiger auf eine [SRow](srow.md) -Struktur, die die zu überprüfende Zeile identifiziert.</span><span class="sxs-lookup"><span data-stu-id="af3a5-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af3a5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af3a5-115">Return value</span></span>

<span data-ttu-id="af3a5-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="af3a5-116">TRUE</span></span> 
  
> <span data-ttu-id="af3a5-117">Die angegebene Zeile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="af3a5-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="af3a5-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="af3a5-118">FALSE</span></span> 
  
> <span data-ttu-id="af3a5-119">Die angegebene Zeile ist gültig.</span><span class="sxs-lookup"><span data-stu-id="af3a5-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af3a5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af3a5-120">See also</span></span>



[<span data-ttu-id="af3a5-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="af3a5-121">FBadRowSet</span></span>](fbadrowset.md)

