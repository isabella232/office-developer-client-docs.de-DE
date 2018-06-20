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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795553"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="e122f-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e122f-103">SizedSPropTagArray</span></span>

<span data-ttu-id="e122f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e122f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e122f-105">Erstellt eine benannte [SPropTagArray](sproptagarray.md) -Struktur, die eine angegebene Anzahl von Eigenschaftentags enthält.</span><span class="sxs-lookup"><span data-stu-id="e122f-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e122f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e122f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e122f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e122f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e122f-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="e122f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e122f-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="e122f-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="e122f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e122f-110">Parameters</span></span>

<span data-ttu-id="e122f-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="e122f-111">__ctag_</span></span>
  
> <span data-ttu-id="e122f-112">Anzahl der Eigenschaftentags in die neue Struktur enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="e122f-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="e122f-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="e122f-113">__name_</span></span>
  
> <span data-ttu-id="e122f-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="e122f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e122f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e122f-115">Remarks</span></span>

<span data-ttu-id="e122f-116">Verwenden Sie das Makro **SizedSPropTagArray** , um ein Array Tag-Eigenschaft mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e122f-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="e122f-117">Um die neue Struktur verwenden, die als Zeiger auf eine **SPropTagArray** -Struktur aus dem Makro **SizedSPropTagArray** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="e122f-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="e122f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e122f-118">See also</span></span>

- [<span data-ttu-id="e122f-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e122f-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="e122f-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="e122f-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

