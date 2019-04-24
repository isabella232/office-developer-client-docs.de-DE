---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Zuletzt geändert: 18, 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356840"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="46185-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="46185-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="46185-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46185-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46185-105">Vergleicht zwei Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="46185-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="46185-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46185-106">Parameters</span></span>

 <span data-ttu-id="46185-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="46185-107">_lpString1_</span></span>
  
> <span data-ttu-id="46185-108">in Zeiger auf die erste Unicode-Zeichenfolge, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="46185-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="46185-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="46185-109">_lpString2_</span></span>
  
> <span data-ttu-id="46185-110">in Zeiger auf die zweite Unicode-Zeichenfolge, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="46185-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46185-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46185-111">Return value</span></span>

<span data-ttu-id="46185-112">Gibt die für einen äquivalenten Aufruf von **MNLS_CompareStringW** mit Ausnahme von CSTR_EQUAL beschriebenen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="46185-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="46185-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46185-113">Remarks</span></span>

 <span data-ttu-id="46185-114">_MNLS_lstrcmpW_ führt einen Vergleich durch Aufrufen von [MNLS_CompareStringW](mnls_comparestringw.md) mit einem Gebietsschema von GetUserDefaultLCID, 0 für Flags und-1 für Kmk1 und Kmk2 aus.</span><span class="sxs-lookup"><span data-stu-id="46185-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46185-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46185-115">See also</span></span>



[<span data-ttu-id="46185-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="46185-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

