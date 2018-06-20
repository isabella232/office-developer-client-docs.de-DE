---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8b7a93a9abb9a1c589ac7fdab3723c9c924eea0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795552"
---
# <a name="sizedsrowset"></a><span data-ttu-id="607d2-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="607d2-103">SizedSRowSet</span></span>

<span data-ttu-id="607d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="607d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="607d2-105">Erstellt eine benannte [SRowSet](srowset.md) -Struktur, die eine angegebene Anzahl von Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="607d2-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="607d2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="607d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="607d2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="607d2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="607d2-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="607d2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="607d2-109">**' Srowset '**</span><span class="sxs-lookup"><span data-stu-id="607d2-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="607d2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="607d2-110">Parameters</span></span>

<span data-ttu-id="607d2-111">__crow_</span><span class="sxs-lookup"><span data-stu-id="607d2-111">__crow_</span></span>
  
> <span data-ttu-id="607d2-112">Anzahl der Anzahl von Zeilen, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="607d2-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="607d2-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="607d2-113">__name_</span></span>
  
> <span data-ttu-id="607d2-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="607d2-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="607d2-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="607d2-115">Remarks</span></span>

<span data-ttu-id="607d2-116">Um die neue Struktur verwenden, die als Zeiger auf eine **SRowSet** -Struktur aus dem Makro **SizedSRowSet** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="607d2-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="607d2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="607d2-117">See also</span></span>

- [<span data-ttu-id="607d2-118">' Srowset '</span><span class="sxs-lookup"><span data-stu-id="607d2-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="607d2-119">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="607d2-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

