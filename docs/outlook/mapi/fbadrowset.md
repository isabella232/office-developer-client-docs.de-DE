---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411792"
---
# <a name="fbadrowset"></a><span data-ttu-id="1c414-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="1c414-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="1c414-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c414-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c414-105">Überprüft alle Tabellenzeilen, die in einem Satz von Tabellenzeilen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1c414-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c414-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="1c414-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c414-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1c414-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1c414-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1c414-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c414-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c414-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1c414-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1c414-110">Called by:</span></span>  <br/> |<span data-ttu-id="1c414-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1c414-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="1c414-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c414-112">Parameters</span></span>

 <span data-ttu-id="1c414-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="1c414-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="1c414-114">in Zeiger auf eine [SRowSet](srowset.md) -Struktur, die den zu überprüfenden Zeilensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1c414-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="1c414-115">Wenn der Zeiger NULL ist, ist die Struktur ungültig.</span><span class="sxs-lookup"><span data-stu-id="1c414-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1c414-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c414-116">Return value</span></span>

<span data-ttu-id="1c414-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="1c414-117">TRUE</span></span> 
  
> <span data-ttu-id="1c414-118">Eine Zeile des angegebenen Zeilen Satzes ist ungültig, oder der Zeilensatz selbst ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1c414-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="1c414-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="1c414-119">FALSE</span></span> 
  
> <span data-ttu-id="1c414-120">Die Zeilen des angegebenen Zeilen Satzes und des Zeilen Satzes selbst sind gültig.</span><span class="sxs-lookup"><span data-stu-id="1c414-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c414-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c414-121">See also</span></span>



[<span data-ttu-id="1c414-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="1c414-122">FBadRow</span></span>](fbadrow.md)

