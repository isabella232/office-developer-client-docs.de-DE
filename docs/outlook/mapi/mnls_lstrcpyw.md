---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Letzte Änderung: 18. Juni 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341727"
---
# <a name="mnls_lstrcpyw"></a><span data-ttu-id="ffe50-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="ffe50-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="ffe50-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffe50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffe50-105">Kopiert eine Zeichenfolge in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="ffe50-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="ffe50-106">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ffe50-106">Do not use.</span></span> <span data-ttu-id="ffe50-107">Erwägen Sie stattdessen die Verwendung [von StringCchCopy.](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffe50-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="ffe50-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffe50-108">Parameters</span></span>

<span data-ttu-id="ffe50-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="ffe50-109">lpString1</span></span>
  
> <span data-ttu-id="ffe50-110">[out] Ein Puffer zum Empfangen des Inhalts der Zeichenfolge, auf die der lpString2-Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="ffe50-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="ffe50-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="ffe50-111">lpString2</span></span>
  
> <span data-ttu-id="ffe50-112">[in] Die zu kopierende Zeichenfolge mit Nullenend.</span><span class="sxs-lookup"><span data-stu-id="ffe50-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ffe50-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffe50-113">Return value</span></span>

<span data-ttu-id="ffe50-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.</span><span class="sxs-lookup"><span data-stu-id="ffe50-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="ffe50-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert NULL, und lpString1 ist möglicherweise nicht null-terminated.</span><span class="sxs-lookup"><span data-stu-id="ffe50-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffe50-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffe50-116">Remarks</span></span>

<span data-ttu-id="ffe50-117">Diese Funktion umschließt die **lstrcpy-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="ffe50-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="ffe50-118">Weitere Informationen finden Sie unter [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ffe50-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ffe50-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffe50-119">See also</span></span>



[<span data-ttu-id="ffe50-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="ffe50-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

