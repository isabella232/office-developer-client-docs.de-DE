---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Zuletzt geändert: 20, 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356854"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="a692e-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="a692e-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="a692e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a692e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a692e-105">Überprüft, ob ein Zeiger auf eine Breite Zeichenfolge gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a692e-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="a692e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a692e-106">Parameters</span></span>

 <span data-ttu-id="a692e-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a692e-107">_lpsz_</span></span>
  
> <span data-ttu-id="a692e-108">in Ein Zeiger auf die Breitzeichen-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a692e-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="a692e-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="a692e-109">_ucchMax_</span></span>
  
> <span data-ttu-id="a692e-110">in Die maximale Länge der Zeichenfolge in Zeichen, einschließlich Terminator.</span><span class="sxs-lookup"><span data-stu-id="a692e-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a692e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a692e-111">Return value</span></span>

<span data-ttu-id="a692e-112">Gibt einen Wert vom Typ Boolean zurück, der true ist, wenn die Zeichenfolge ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="a692e-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a692e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a692e-113">Remarks</span></span>

<span data-ttu-id="a692e-114">Diese Funktion umschließt [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a692e-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="a692e-115">Weitere Informationen finden Sie unter [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a692e-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

