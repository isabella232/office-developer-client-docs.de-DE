---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418113"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="d30bd-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d30bd-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="d30bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d30bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d30bd-105">Erstellt eine benannte [SPropProblemArray-Struktur,](spropproblemarray.md) die eine angegebene Anzahl von [SPropProblem-Strukturen](spropproblem.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="d30bd-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d30bd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d30bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="d30bd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d30bd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d30bd-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="d30bd-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d30bd-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="d30bd-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="d30bd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d30bd-110">Parameters</span></span>

<span data-ttu-id="d30bd-111">_ _cprob_</span><span class="sxs-lookup"><span data-stu-id="d30bd-111">_ _cprob_</span></span>
  
> <span data-ttu-id="d30bd-112">Anzahl der **SPropProblem-Strukturen,** die in die neue Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d30bd-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="d30bd-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="d30bd-113">_ _name_</span></span>
  
> <span data-ttu-id="d30bd-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="d30bd-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d30bd-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d30bd-115">Remarks</span></span>

<span data-ttu-id="d30bd-116">Verwenden Sie **das SizeSPropProblemArray-Makro,** um ein Eigenschaftenproblemarray mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d30bd-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="d30bd-117">Führen Sie die folgende Gliederung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedSPropProblemArray** als Zeiger auf eine **SPropProblemArray-Struktur** resultiert:</span><span class="sxs-lookup"><span data-stu-id="d30bd-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="d30bd-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d30bd-118">See also</span></span>

- [<span data-ttu-id="d30bd-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d30bd-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="d30bd-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="d30bd-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="d30bd-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="d30bd-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

