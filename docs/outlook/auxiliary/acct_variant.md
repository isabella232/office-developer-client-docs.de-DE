---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp hat.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424399"
---
# <a name="acctvariant"></a><span data-ttu-id="e2d11-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="e2d11-103">ACCT_VARIANT</span></span>

<span data-ttu-id="e2d11-104">Eine Variable dieses Datentyps enthält den Wert einer Eigenschaft, die einen Variant-Datentyp hat.</span><span class="sxs-lookup"><span data-stu-id="e2d11-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e2d11-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e2d11-105">Quick info</span></span>

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a><span data-ttu-id="e2d11-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="e2d11-106">Members</span></span>

<span data-ttu-id="e2d11-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="e2d11-107">_dwType_</span></span>
  
> <span data-ttu-id="e2d11-108">Typ der Variante:</span><span class="sxs-lookup"><span data-stu-id="e2d11-108">Type of variant:</span></span>
    
    - <span data-ttu-id="e2d11-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e2d11-109">PT_LONG</span></span>
    
    - <span data-ttu-id="e2d11-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2d11-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="e2d11-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e2d11-111">PT_BINARY</span></span>
    
<span data-ttu-id="e2d11-112">_DW_</span><span class="sxs-lookup"><span data-stu-id="e2d11-112">_dw_</span></span>
  
> <span data-ttu-id="e2d11-113">DWORD-Wert von Variant.</span><span class="sxs-lookup"><span data-stu-id="e2d11-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="e2d11-114">_Pwsz_</span><span class="sxs-lookup"><span data-stu-id="e2d11-114">_pwsz_</span></span>
  
> <span data-ttu-id="e2d11-115">Zeichenfolgenwert von Variant.</span><span class="sxs-lookup"><span data-stu-id="e2d11-115">String value of variant.</span></span>
    
<span data-ttu-id="e2d11-116">_bin_</span><span class="sxs-lookup"><span data-stu-id="e2d11-116">_bin_</span></span>
  
> <span data-ttu-id="e2d11-117">Binärwert des Variant-Werts.</span><span class="sxs-lookup"><span data-stu-id="e2d11-117">Binary value of the variant.</span></span>
    

