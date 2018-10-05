---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Zuletzt geändert: 18 Juni 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382708"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="07872-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="07872-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="07872-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07872-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07872-105">Kopiert eine Zeichenfolge in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="07872-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="07872-106">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="07872-106">Do not use.</span></span> <span data-ttu-id="07872-107">Erwägen Sie [StringCchCopy hin](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="07872-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="07872-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="07872-108">Parameters</span></span>

<span data-ttu-id="07872-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="07872-109">lpString1</span></span>
  
> <span data-ttu-id="07872-110">[out] Durch den Parameter lpString2 auf ein Puffer den Inhalt der Zeichenfolge empfängt das.</span><span class="sxs-lookup"><span data-stu-id="07872-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="07872-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="07872-111">lpString2</span></span>
  
> <span data-ttu-id="07872-112">[in] Die Null endende Zeichenfolge kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07872-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07872-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07872-113">Return value</span></span>

<span data-ttu-id="07872-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.</span><span class="sxs-lookup"><span data-stu-id="07872-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="07872-115">Wenn die Funktion fehlschlägt, wird NULL zurückgegeben und lpString1 möglicherweise nicht Null endende.</span><span class="sxs-lookup"><span data-stu-id="07872-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="07872-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="07872-116">Remarks</span></span>

<span data-ttu-id="07872-117">Diese Funktion umschließt die **Lstrcpy** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="07872-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="07872-118">Weitere Informationen finden Sie unter [Lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="07872-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="07872-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07872-119">See also</span></span>



[<span data-ttu-id="07872-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="07872-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

