---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Eine Variable dieses Typs Daten enthält den Wert einer Eigenschaft, die einen variant-Datentyp ist.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790926"
---
# <a name="acctvariant"></a><span data-ttu-id="2bca2-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="2bca2-103">ACCT_VARIANT</span></span>

<span data-ttu-id="2bca2-104">Eine Variable dieses Typs Daten enthält den Wert einer Eigenschaft, die einen variant-Datentyp ist.</span><span class="sxs-lookup"><span data-stu-id="2bca2-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2bca2-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2bca2-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="2bca2-106">Members</span><span class="sxs-lookup"><span data-stu-id="2bca2-106">Members</span></span>

<span data-ttu-id="2bca2-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="2bca2-107">_dwType_</span></span>
  
> <span data-ttu-id="2bca2-108">Typ Variante:</span><span class="sxs-lookup"><span data-stu-id="2bca2-108">Type of variant:</span></span>
    
    - <span data-ttu-id="2bca2-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2bca2-109">PT_LONG</span></span>
    
    - <span data-ttu-id="2bca2-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2bca2-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="2bca2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2bca2-111">PT_BINARY</span></span>
    
<span data-ttu-id="2bca2-112">_dw_</span><span class="sxs-lookup"><span data-stu-id="2bca2-112">_dw_</span></span>
  
> <span data-ttu-id="2bca2-113">DWORD-Wert von Variant-Wert.</span><span class="sxs-lookup"><span data-stu-id="2bca2-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="2bca2-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="2bca2-114">_pwsz_</span></span>
  
> <span data-ttu-id="2bca2-115">String-Wert von Variant-Wert.</span><span class="sxs-lookup"><span data-stu-id="2bca2-115">String value of variant.</span></span>
    
<span data-ttu-id="2bca2-116">_Papierkorb_</span><span class="sxs-lookup"><span data-stu-id="2bca2-116">_bin_</span></span>
  
> <span data-ttu-id="2bca2-117">Binärer Wert der Variante.</span><span class="sxs-lookup"><span data-stu-id="2bca2-117">Binary value of the variant.</span></span>
    

