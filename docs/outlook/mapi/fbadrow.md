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
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590162"
---
# <a name="fbadrow"></a><span data-ttu-id="1efb8-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="1efb8-103">FBadRow</span></span>

  
  
<span data-ttu-id="1efb8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1efb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1efb8-105">Überprüft eine Zeile in einer Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="1efb8-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1efb8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1efb8-106">Header file:</span></span>  <br/> |<span data-ttu-id="1efb8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1efb8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1efb8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1efb8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1efb8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1efb8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1efb8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1efb8-110">Called by:</span></span>  <br/> |<span data-ttu-id="1efb8-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1efb8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="1efb8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1efb8-112">Parameters</span></span>

 <span data-ttu-id="1efb8-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="1efb8-113">_lprow_</span></span>
  
> <span data-ttu-id="1efb8-114">[in] Zeiger auf eine [SRow](srow.md) -Struktur, die die Zeile zu überprüfenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1efb8-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1efb8-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1efb8-115">Return value</span></span>

<span data-ttu-id="1efb8-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="1efb8-116">TRUE</span></span> 
  
> <span data-ttu-id="1efb8-117">Die angegebene Zeile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1efb8-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="1efb8-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="1efb8-118">FALSE</span></span> 
  
> <span data-ttu-id="1efb8-119">Die angegebene Zeile ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1efb8-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1efb8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1efb8-120">See also</span></span>



[<span data-ttu-id="1efb8-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="1efb8-121">FBadRowSet</span></span>](fbadrowset.md)

