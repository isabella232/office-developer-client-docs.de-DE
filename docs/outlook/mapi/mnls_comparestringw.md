---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Zuletzt geändert: 20 Februar 2012'
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793265"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="aabb4-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="aabb4-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="aabb4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aabb4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aabb4-105">Vergleicht zwei Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="aabb4-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="aabb4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aabb4-106">Parameters</span></span>

 <span data-ttu-id="aabb4-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="aabb4-107">_lcid_</span></span>
  
> <span data-ttu-id="aabb4-108">[in] Gebietsschema-ID.</span><span class="sxs-lookup"><span data-stu-id="aabb4-108">[in] Locale identifier.</span></span> <span data-ttu-id="aabb4-109">Ausführliche Definitionen finden Sie unter der Parameter _Locale_ der [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aabb4-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="aabb4-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="aabb4-110">_dwFlags_</span></span>
  
> <span data-ttu-id="aabb4-111">[in] Kennzeichen, die Groß-/Kleinschreibung und diakritische Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="aabb4-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="aabb4-112">Ausführliche Definitionen finden Sie unter den _DwCmpFlags_ -Parameter der [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aabb4-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="aabb4-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="aabb4-113">_pstr1_</span></span>
  
> <span data-ttu-id="aabb4-114">[in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="aabb4-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="aabb4-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="aabb4-115">_cch1_</span></span>
  
> <span data-ttu-id="aabb4-116">[in] Länge in Zeichen der ersten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="aabb4-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="aabb4-117">Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist.</span><span class="sxs-lookup"><span data-stu-id="aabb4-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="aabb4-118">In diesem Fall bestimmt die **MNLS_CompareStringW** -Funktion die Länge automatisch.</span><span class="sxs-lookup"><span data-stu-id="aabb4-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="aabb4-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="aabb4-119">_pstr2_</span></span>
  
> <span data-ttu-id="aabb4-120">[in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="aabb4-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="aabb4-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="aabb4-121">_cch2_</span></span>
  
> <span data-ttu-id="aabb4-122">[in] Die Länge des zweiten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="aabb4-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="aabb4-123">Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist.</span><span class="sxs-lookup"><span data-stu-id="aabb4-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="aabb4-124">In diesem Fall bestimmt die Funktion die Länge automatisch.</span><span class="sxs-lookup"><span data-stu-id="aabb4-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aabb4-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="aabb4-125">Return value</span></span>

<span data-ttu-id="aabb4-126">Gibt die Werte für [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aabb4-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aabb4-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aabb4-127">Remarks</span></span>

<span data-ttu-id="aabb4-128">Diese Funktion umschließt [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aabb4-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="aabb4-129">**MNLS_CompareStringW** weist die gleichen Parameter und hat die gleiche Wirkung wie [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aabb4-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aabb4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aabb4-130">See also</span></span>



[<span data-ttu-id="aabb4-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="aabb4-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="aabb4-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="aabb4-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

