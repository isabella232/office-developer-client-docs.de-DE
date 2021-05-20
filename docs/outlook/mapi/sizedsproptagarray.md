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
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429348"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="22208-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="22208-103">SizedSPropTagArray</span></span>

<span data-ttu-id="22208-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22208-105">Erstellt eine benannte [SPropTagArray-Struktur,](sproptagarray.md) die eine angegebene Anzahl von Eigenschaftstags enthält.</span><span class="sxs-lookup"><span data-stu-id="22208-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22208-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="22208-106">Header file:</span></span>  <br/> |<span data-ttu-id="22208-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22208-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="22208-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="22208-108">Related structure:</span></span>  <br/> |<span data-ttu-id="22208-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="22208-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="22208-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22208-110">Parameters</span></span>

<span data-ttu-id="22208-111">_ _ctag_</span><span class="sxs-lookup"><span data-stu-id="22208-111">_ _ctag_</span></span>
  
> <span data-ttu-id="22208-112">Anzahl der Eigenschaftstags, die in der neuen Struktur enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="22208-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="22208-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="22208-113">_ _name_</span></span>
  
> <span data-ttu-id="22208-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="22208-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22208-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22208-115">Remarks</span></span>

<span data-ttu-id="22208-116">Verwenden Sie **das #A0 SizedSPropTagArray,** um ein Eigenschaftentagarray mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22208-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="22208-117">Führen Sie die folgende Gliederung aus, um die neue Struktur zu verwenden, die aus dem **#A0 als** Zeiger auf eine **SPropTagArray-Struktur** resultiert:</span><span class="sxs-lookup"><span data-stu-id="22208-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="22208-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22208-118">See also</span></span>

- [<span data-ttu-id="22208-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="22208-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="22208-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="22208-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

