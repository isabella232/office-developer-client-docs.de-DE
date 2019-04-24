---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Zuletzt geändert: 20, 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356847"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="4a110-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="4a110-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="4a110-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a110-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a110-105">Vergleicht zwei Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="4a110-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="4a110-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a110-106">Parameters</span></span>

 <span data-ttu-id="4a110-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="4a110-107">_lcid_</span></span>
  
> <span data-ttu-id="4a110-108">in Gebietsschemabezeichner.</span><span class="sxs-lookup"><span data-stu-id="4a110-108">[in] Locale identifier.</span></span> <span data-ttu-id="4a110-109">Ausführliche Definitionen finden Sie unter _locale_ -Parameter von [comparecollection](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a110-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="4a110-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4a110-110">_dwFlags_</span></span>
  
> <span data-ttu-id="4a110-111">in Flags zum Ignorieren von Groß-/Kleinschreibung und diakritischen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4a110-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="4a110-112">Ausführliche Definitionen finden Sie im _dwCmpFlags_ -Parameter von [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a110-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="4a110-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="4a110-113">_pstr1_</span></span>
  
> <span data-ttu-id="4a110-114">in Zeiger auf die erste Unicode-Zeichenfolge, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a110-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="4a110-115">_Kmk1_</span><span class="sxs-lookup"><span data-stu-id="4a110-115">_cch1_</span></span>
  
> <span data-ttu-id="4a110-116">in Länge in Zeichen der ersten Unicode-Zeichenfolge, ohne das abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4a110-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="4a110-117">Die Anwendung kann einen negativen Wert angeben, wenn die Zeichenfolge NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="4a110-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="4a110-118">In diesem Fall bestimmt die **MNLS_CompareStringW** -Funktion die Länge automatisch.</span><span class="sxs-lookup"><span data-stu-id="4a110-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="4a110-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="4a110-119">_pstr2_</span></span>
  
> <span data-ttu-id="4a110-120">in Zeiger auf die zweite Unicode-Zeichenfolge, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a110-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="4a110-121">_Kmk2_</span><span class="sxs-lookup"><span data-stu-id="4a110-121">_cch2_</span></span>
  
> <span data-ttu-id="4a110-122">in Länge in Zeichen der zweiten Unicode-Zeichenfolge, ohne das abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4a110-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="4a110-123">Die Anwendung kann einen negativen Wert angeben, wenn die Zeichenfolge NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="4a110-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="4a110-124">In diesem Fall bestimmt die Funktion die Länge automatisch.</span><span class="sxs-lookup"><span data-stu-id="4a110-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a110-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a110-125">Return value</span></span>

<span data-ttu-id="4a110-126">Gibt die für [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)beschriebenen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4a110-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a110-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a110-127">Remarks</span></span>

<span data-ttu-id="4a110-128">Diese Funktion umschließt [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a110-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="4a110-129">**MNLS_CompareStringW** verwendet die gleichen Parameter und hat dasselbe Verhalten wie [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a110-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a110-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a110-130">See also</span></span>



[<span data-ttu-id="4a110-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="4a110-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="4a110-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="4a110-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

