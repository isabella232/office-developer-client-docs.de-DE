---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Zuletzt geändert: 20 Februar 2012'
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793274"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="c1e95-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="c1e95-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="c1e95-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1e95-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1e95-105">Überprüft, ob ein Zeiger auf eine Breite Zeichenfolge gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c1e95-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="c1e95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1e95-106">Parameters</span></span>

 <span data-ttu-id="c1e95-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="c1e95-107">_lpsz_</span></span>
  
> <span data-ttu-id="c1e95-108">[in] Ein Zeiger auf die Breite Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c1e95-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="c1e95-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="c1e95-109">_ucchMax_</span></span>
  
> <span data-ttu-id="c1e95-110">[in] Die maximale Länge der Zeichenfolge in Zeichen einschließlich.</span><span class="sxs-lookup"><span data-stu-id="c1e95-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1e95-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c1e95-111">Return value</span></span>

<span data-ttu-id="c1e95-112">Gibt einen booleschen Wert, der True, wenn die Zeichenfolge beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="c1e95-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1e95-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1e95-113">Remarks</span></span>

<span data-ttu-id="c1e95-114">Diese Funktion umschließt [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1e95-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="c1e95-115">Weitere Informationen finden Sie unter [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1e95-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

