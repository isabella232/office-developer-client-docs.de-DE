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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793280"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="5a141-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="5a141-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="5a141-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a141-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a141-105">Kopiert eine Zeichenfolge in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="5a141-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="5a141-106">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a141-106">Do not use.</span></span> <span data-ttu-id="5a141-107">Erwägen Sie [StringCchCopy hin](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5a141-107">Consider using [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="5a141-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a141-108">Parameters</span></span>

<span data-ttu-id="5a141-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="5a141-109">lpString1</span></span>
  
> <span data-ttu-id="5a141-110">[out] Durch den Parameter lpString2 auf ein Puffer den Inhalt der Zeichenfolge empfängt das.</span><span class="sxs-lookup"><span data-stu-id="5a141-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="5a141-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="5a141-111">lpString2</span></span>
  
> <span data-ttu-id="5a141-112">[in] Die Null endende Zeichenfolge kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a141-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a141-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5a141-113">Return value</span></span>

<span data-ttu-id="5a141-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Puffer.</span><span class="sxs-lookup"><span data-stu-id="5a141-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="5a141-115">Wenn die Funktion fehlschlägt, wird NULL zurückgegeben und lpString1 möglicherweise nicht Null endende.</span><span class="sxs-lookup"><span data-stu-id="5a141-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a141-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a141-116">Remarks</span></span>

<span data-ttu-id="5a141-117">Diese Funktion umschließt die **Lstrcpy** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5a141-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="5a141-118">Weitere Informationen finden Sie unter [Lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a141-118">For more information, see [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a141-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a141-119">See also</span></span>



[<span data-ttu-id="5a141-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="5a141-120">lstrcpy</span></span>](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

