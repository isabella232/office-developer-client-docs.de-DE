---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573621"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="293b1-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="293b1-103">SizedSPropTagArray</span></span>

<span data-ttu-id="293b1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="293b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="293b1-105">Erstellt eine benannte [SPropTagArray](sproptagarray.md) -Struktur, die eine angegebene Anzahl von Eigenschaftentags enthält.</span><span class="sxs-lookup"><span data-stu-id="293b1-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="293b1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="293b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="293b1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="293b1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="293b1-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="293b1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="293b1-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="293b1-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="293b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="293b1-110">Parameters</span></span>

<span data-ttu-id="293b1-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="293b1-111">__ctag_</span></span>
  
> <span data-ttu-id="293b1-112">Anzahl der Eigenschaftentags in die neue Struktur enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="293b1-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="293b1-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="293b1-113">__name_</span></span>
  
> <span data-ttu-id="293b1-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="293b1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="293b1-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="293b1-115">Remarks</span></span>

<span data-ttu-id="293b1-116">Verwenden Sie das Makro **SizedSPropTagArray** , um ein Array Tag-Eigenschaft mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="293b1-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="293b1-117">Um die neue Struktur verwenden, die als Zeiger auf eine **SPropTagArray** -Struktur aus dem Makro **SizedSPropTagArray** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="293b1-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="293b1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="293b1-118">See also</span></span>

- [<span data-ttu-id="293b1-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="293b1-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="293b1-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="293b1-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

