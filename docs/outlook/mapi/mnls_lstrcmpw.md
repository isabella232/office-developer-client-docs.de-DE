---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Zuletzt geändert: 18 Juni 2012'
ms.openlocfilehash: 36e22c60b32242425335b122b66c2c77e376848b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580117"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="6c4c1-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="6c4c1-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="6c4c1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c4c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c4c1-105">Vergleicht zwei Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="6c4c1-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="6c4c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c4c1-106">Parameters</span></span>

 <span data-ttu-id="6c4c1-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="6c4c1-107">_lpString1_</span></span>
  
> <span data-ttu-id="6c4c1-108">[in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6c4c1-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="6c4c1-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="6c4c1-109">_lpString2_</span></span>
  
> <span data-ttu-id="6c4c1-110">[in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6c4c1-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c4c1-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6c4c1-111">Return value</span></span>

<span data-ttu-id="6c4c1-112">Gibt die Werte für einen entsprechenden Aufruf **MNLS_CompareStringW** außer CSTR_EQUAL beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6c4c1-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6c4c1-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6c4c1-113">Remarks</span></span>

 <span data-ttu-id="6c4c1-114">_MNLS_lstrcmpW_ führt einen Vergleich durch Aufrufen von [MNLS_CompareStringW](mnls_comparestringw.md) mit der GetUserDefaultLCID, 0 für Flags, die ein Gebietsschema und-1 für cch1 und cch2.</span><span class="sxs-lookup"><span data-stu-id="6c4c1-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c4c1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c4c1-115">See also</span></span>



[<span data-ttu-id="6c4c1-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="6c4c1-116">GetUserDefaultLCID</span></span>](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

