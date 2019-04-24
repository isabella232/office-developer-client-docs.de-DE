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
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282698"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="5d9ad-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5d9ad-103">SizedSPropTagArray</span></span>

<span data-ttu-id="5d9ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d9ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d9ad-105">Erstellt eine benannte [SPropTagArray](sproptagarray.md) -Struktur, die eine angegebene Anzahl von Property-Tags enthält.</span><span class="sxs-lookup"><span data-stu-id="5d9ad-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d9ad-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5d9ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d9ad-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5d9ad-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5d9ad-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="5d9ad-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5d9ad-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="5d9ad-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="5d9ad-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d9ad-110">Parameters</span></span>

<span data-ttu-id="5d9ad-111">__CTAG_</span><span class="sxs-lookup"><span data-stu-id="5d9ad-111">__ctag_</span></span>
  
> <span data-ttu-id="5d9ad-112">Die Anzahl der Eigenschaftstags, die in die neue Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5d9ad-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="5d9ad-113">__Name_</span><span class="sxs-lookup"><span data-stu-id="5d9ad-113">__name_</span></span>
  
> <span data-ttu-id="5d9ad-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d9ad-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d9ad-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d9ad-115">Remarks</span></span>

<span data-ttu-id="5d9ad-116">Verwenden Sie das **SizedSPropTagArray** -Makro, um ein Property-Tag-Array mit expliziten Begrenzungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5d9ad-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="5d9ad-117">Um die neue Struktur zu verwenden, die aus dem **SizedSPropTagArray** -Makro als Zeiger auf eine **SPropTagArray** -Struktur resultiert, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="5d9ad-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="5d9ad-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d9ad-118">See also</span></span>

- [<span data-ttu-id="5d9ad-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5d9ad-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="5d9ad-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="5d9ad-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

