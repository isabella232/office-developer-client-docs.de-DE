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
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791690"
---
# <a name="fbadrowset"></a><span data-ttu-id="02693-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="02693-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="02693-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02693-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02693-105">Überprüft alle Tabellenzeilen in einer Tabellenzeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="02693-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02693-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="02693-106">Header file:</span></span>  <br/> |<span data-ttu-id="02693-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="02693-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="02693-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="02693-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="02693-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="02693-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="02693-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="02693-110">Called by:</span></span>  <br/> |<span data-ttu-id="02693-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="02693-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="02693-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="02693-112">Parameters</span></span>

 <span data-ttu-id="02693-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="02693-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="02693-114">[in] Zeiger auf eine [SRowSet](srowset.md) -Struktur, die den zu überprüfenden Rowset identifiziert.</span><span class="sxs-lookup"><span data-stu-id="02693-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="02693-115">Wenn der Zeiger NULL ist, ist die Struktur ungültig.</span><span class="sxs-lookup"><span data-stu-id="02693-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="02693-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02693-116">Return value</span></span>

<span data-ttu-id="02693-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="02693-117">TRUE</span></span> 
  
> <span data-ttu-id="02693-118">Eine Zeile mit der angegebenen Zeile Set ist ungültig, oder die Rowset selbst ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="02693-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="02693-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="02693-119">FALSE</span></span> 
  
> <span data-ttu-id="02693-120">Die Zeilen der angegebenen Zeile Menge und die Zeile selbst festgelegt sind gültig.</span><span class="sxs-lookup"><span data-stu-id="02693-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02693-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02693-121">See also</span></span>



[<span data-ttu-id="02693-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="02693-122">FBadRow</span></span>](fbadrow.md)

