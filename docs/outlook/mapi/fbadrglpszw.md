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
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791659"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="6e8fc-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="6e8fc-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="6e8fc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e8fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e8fc-105">Überprüft alle Zeichenfolgen in einem Array von Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6e8fc-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e8fc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6e8fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e8fc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6e8fc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6e8fc-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6e8fc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6e8fc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6e8fc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6e8fc-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6e8fc-110">Called by:</span></span>  <br/> |<span data-ttu-id="6e8fc-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6e8fc-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="6e8fc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e8fc-112">Parameters</span></span>

 <span data-ttu-id="6e8fc-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="6e8fc-113">_lppszW_</span></span>
  
> <span data-ttu-id="6e8fc-114">[in] Zeiger auf ein Array mit Null terminierte Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6e8fc-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="6e8fc-115">_CString_</span><span class="sxs-lookup"><span data-stu-id="6e8fc-115">_cStrings_</span></span>
  
> <span data-ttu-id="6e8fc-116">[in] Anzahl der Zeichenfolgen im Array auf den durch den Parameter _LppszW_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="6e8fc-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6e8fc-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6e8fc-117">Return value</span></span>

<span data-ttu-id="6e8fc-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="6e8fc-118">TRUE</span></span> 
  
> <span data-ttu-id="6e8fc-119">Eine oder mehrere der Zeichenfolgen in das angegebene Array ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6e8fc-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="6e8fc-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="6e8fc-120">FALSE</span></span> 
  
> <span data-ttu-id="6e8fc-121">Die Zeichenfolgen im angegebenen Array sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="6e8fc-121">The strings in the specified array are valid.</span></span>
    

