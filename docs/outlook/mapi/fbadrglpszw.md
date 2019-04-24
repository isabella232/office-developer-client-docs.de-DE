---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341055"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="92c74-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="92c74-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="92c74-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92c74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92c74-105">Überprüft alle Zeichenfolgen in einem Array von Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="92c74-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92c74-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="92c74-106">Header file:</span></span>  <br/> |<span data-ttu-id="92c74-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="92c74-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="92c74-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="92c74-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="92c74-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="92c74-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="92c74-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="92c74-110">Called by:</span></span>  <br/> |<span data-ttu-id="92c74-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="92c74-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="92c74-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="92c74-112">Parameters</span></span>

 <span data-ttu-id="92c74-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="92c74-113">_lppszW_</span></span>
  
> <span data-ttu-id="92c74-114">in Zeiger auf ein Array von null-terminierten Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="92c74-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="92c74-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="92c74-115">_cStrings_</span></span>
  
> <span data-ttu-id="92c74-116">in Anzahl der Zeichenfolgen im Array, auf die durch den _lppszW_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="92c74-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="92c74-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92c74-117">Return value</span></span>

<span data-ttu-id="92c74-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="92c74-118">TRUE</span></span> 
  
> <span data-ttu-id="92c74-119">Mindestens eine der Zeichenfolgen im angegebenen Array ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="92c74-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="92c74-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="92c74-120">FALSE</span></span> 
  
> <span data-ttu-id="92c74-121">Die Zeichenfolgen im angegebenen Array sind gültig.</span><span class="sxs-lookup"><span data-stu-id="92c74-121">The strings in the specified array are valid.</span></span>
    

