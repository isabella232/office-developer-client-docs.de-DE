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
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386348"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="1999e-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="1999e-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="1999e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1999e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1999e-105">Vergleicht zwei Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="1999e-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="1999e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1999e-106">Parameters</span></span>

 <span data-ttu-id="1999e-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="1999e-107">_lpString1_</span></span>
  
> <span data-ttu-id="1999e-108">[in] Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1999e-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="1999e-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="1999e-109">_lpString2_</span></span>
  
> <span data-ttu-id="1999e-110">[in] Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1999e-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1999e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1999e-111">Return value</span></span>

<span data-ttu-id="1999e-112">Gibt die Werte für einen entsprechenden Aufruf **MNLS_CompareStringW** außer CSTR_EQUAL beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1999e-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1999e-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1999e-113">Remarks</span></span>

 <span data-ttu-id="1999e-114">_MNLS_lstrcmpW_ führt einen Vergleich durch Aufrufen von [MNLS_CompareStringW](mnls_comparestringw.md) mit der GetUserDefaultLCID, 0 für Flags, die ein Gebietsschema und-1 für cch1 und cch2.</span><span class="sxs-lookup"><span data-stu-id="1999e-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1999e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1999e-115">See also</span></span>



[<span data-ttu-id="1999e-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="1999e-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

