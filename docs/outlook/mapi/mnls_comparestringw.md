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
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396211"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="306a4-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="306a4-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="306a4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="306a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="306a4-105">Vergleicht zwei Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="306a4-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="306a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="306a4-106">Parameters</span></span>

 <span data-ttu-id="306a4-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="306a4-107">_lcid_</span></span>
  
> <span data-ttu-id="306a4-108">[in] Gebietsschema-ID.</span><span class="sxs-lookup"><span data-stu-id="306a4-108">[in] Locale identifier.</span></span> <span data-ttu-id="306a4-109">Ausführliche Definitionen finden Sie unter der Parameter _Locale_ der [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="306a4-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="306a4-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="306a4-110">_dwFlags_</span></span>
  
> <span data-ttu-id="306a4-111">[in] Kennzeichen, die Groß-/Kleinschreibung und diakritische Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="306a4-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="306a4-112">Ausführliche Definitionen finden Sie unter den _DwCmpFlags_ -Parameter der [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="306a4-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="306a4-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="306a4-113">_pstr1_</span></span>
  
> <span data-ttu-id="306a4-114">[in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="306a4-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="306a4-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="306a4-115">_cch1_</span></span>
  
> <span data-ttu-id="306a4-116">[in] Länge in Zeichen der ersten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="306a4-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="306a4-117">Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist.</span><span class="sxs-lookup"><span data-stu-id="306a4-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="306a4-118">In diesem Fall bestimmt die **MNLS_CompareStringW** -Funktion die Länge automatisch.</span><span class="sxs-lookup"><span data-stu-id="306a4-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="306a4-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="306a4-119">_pstr2_</span></span>
  
> <span data-ttu-id="306a4-120">[in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="306a4-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="306a4-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="306a4-121">_cch2_</span></span>
  
> <span data-ttu-id="306a4-122">[in] Die Länge des zweiten Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="306a4-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="306a4-123">Die Anwendung kann einen negativen Wert bereitstellen, wenn die Zeichenfolge Null endende ist.</span><span class="sxs-lookup"><span data-stu-id="306a4-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="306a4-124">In diesem Fall bestimmt die Funktion die Länge automatisch.</span><span class="sxs-lookup"><span data-stu-id="306a4-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="306a4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="306a4-125">Return value</span></span>

<span data-ttu-id="306a4-126">Gibt die Werte für [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="306a4-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="306a4-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="306a4-127">Remarks</span></span>

<span data-ttu-id="306a4-128">Diese Funktion umschließt [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="306a4-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="306a4-129">**MNLS_CompareStringW** weist die gleichen Parameter und hat die gleiche Wirkung wie [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="306a4-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="306a4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="306a4-130">See also</span></span>



[<span data-ttu-id="306a4-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="306a4-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="306a4-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="306a4-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

