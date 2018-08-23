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
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589567"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="4f464-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="4f464-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="4f464-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f464-105">Überprüft, ob ein Zeiger auf eine Breite Zeichenfolge gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4f464-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="4f464-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f464-106">Parameters</span></span>

 <span data-ttu-id="4f464-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="4f464-107">_lpsz_</span></span>
  
> <span data-ttu-id="4f464-108">[in] Ein Zeiger auf die Breite Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4f464-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="4f464-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="4f464-109">_ucchMax_</span></span>
  
> <span data-ttu-id="4f464-110">[in] Die maximale Länge der Zeichenfolge in Zeichen einschließlich.</span><span class="sxs-lookup"><span data-stu-id="4f464-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f464-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4f464-111">Return value</span></span>

<span data-ttu-id="4f464-112">Gibt einen booleschen Wert, der True, wenn die Zeichenfolge beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="4f464-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f464-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4f464-113">Remarks</span></span>

<span data-ttu-id="4f464-114">Diese Funktion umschließt [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f464-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="4f464-115">Weitere Informationen finden Sie unter [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f464-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

