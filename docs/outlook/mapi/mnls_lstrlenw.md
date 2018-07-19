---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793297"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="4577b-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="4577b-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="4577b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4577b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4577b-105">Bestimmt die Länge der angegebenen Unicode-Zeichenfolge, ausgenommen abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4577b-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="4577b-106">Erwägen Sie [StringCchLength](http://msdn.microsoft.com/de-de/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4577b-106">Consider using [StringCchLength](http://msdn.microsoft.com/de-de/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="4577b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4577b-107">Parameters</span></span>

 <span data-ttu-id="4577b-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="4577b-108">_lpsz_</span></span>
  
> <span data-ttu-id="4577b-109">[in] Die Null terminierte Unicode-Zeichenfolge überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="4577b-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4577b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4577b-110">Return value</span></span>

<span data-ttu-id="4577b-111">Die Funktion gibt eine ganze Zahl mit der Länge der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="4577b-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="4577b-112">Es ist die Anzahl der Zeichen in der Zeichenfolge, ausgenommen abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4577b-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="4577b-113">Wenn _Lpsz_ NULL ist, gibt die Funktion 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4577b-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4577b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4577b-114">Remarks</span></span>

<span data-ttu-id="4577b-115">Diese Funktion umschließt die **Lstrlen** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4577b-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="4577b-116">Weitere Informationen finden Sie unter [Lstrlen](http://msdn.microsoft.com/de-de/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4577b-116">For more information, see [lstrlen](http://msdn.microsoft.com/de-de/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4577b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4577b-117">See also</span></span>



[<span data-ttu-id="4577b-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="4577b-118">lstrlen</span></span>](http://msdn.microsoft.com/de-de/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="4577b-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="4577b-119">StringCchLength</span></span>](http://msdn.microsoft.com/de-de/library/ms647539%28VS.85%29.aspx)

