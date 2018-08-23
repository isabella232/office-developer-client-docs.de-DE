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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565914"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="e1f50-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="e1f50-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="e1f50-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1f50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1f50-105">Überprüft alle Zeichenfolgen in einem Array von Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e1f50-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1f50-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e1f50-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1f50-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="e1f50-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="e1f50-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e1f50-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1f50-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1f50-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1f50-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e1f50-110">Called by:</span></span>  <br/> |<span data-ttu-id="e1f50-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e1f50-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="e1f50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1f50-112">Parameters</span></span>

 <span data-ttu-id="e1f50-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="e1f50-113">_lppszW_</span></span>
  
> <span data-ttu-id="e1f50-114">[in] Zeiger auf ein Array mit Null terminierte Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e1f50-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="e1f50-115">_CString_</span><span class="sxs-lookup"><span data-stu-id="e1f50-115">_cStrings_</span></span>
  
> <span data-ttu-id="e1f50-116">[in] Anzahl der Zeichenfolgen im Array auf den durch den Parameter _LppszW_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="e1f50-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e1f50-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e1f50-117">Return value</span></span>

<span data-ttu-id="e1f50-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="e1f50-118">TRUE</span></span> 
  
> <span data-ttu-id="e1f50-119">Eine oder mehrere der Zeichenfolgen in das angegebene Array ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e1f50-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="e1f50-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="e1f50-120">FALSE</span></span> 
  
> <span data-ttu-id="e1f50-121">Die Zeichenfolgen im angegebenen Array sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="e1f50-121">The strings in the specified array are valid.</span></span>
    

