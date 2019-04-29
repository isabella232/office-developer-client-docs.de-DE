---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428606"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="a22a1-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a22a1-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="a22a1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a22a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a22a1-105">Erstellt eine benannte [SSortOrderSet](ssortorderset.md) -Struktur, die eine angegebene Anzahl von Sortierreihenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="a22a1-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a22a1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a22a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="a22a1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a22a1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a22a1-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="a22a1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a22a1-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="a22a1-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="a22a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a22a1-110">Parameters</span></span>

<span data-ttu-id="a22a1-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="a22a1-111">__csort_</span></span>
  
> <span data-ttu-id="a22a1-112">Die Anzahl der Sortierreihenfolgen, die in die neue Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a22a1-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="a22a1-113">__Name_</span><span class="sxs-lookup"><span data-stu-id="a22a1-113">__name_</span></span>
  
> <span data-ttu-id="a22a1-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="a22a1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a22a1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a22a1-115">Remarks</span></span>

<span data-ttu-id="a22a1-116">Verwenden Sie das **SizedSSortOrderSet** -Makro, um eine Sortierreihenfolge mit expliziten Begrenzungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a22a1-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="a22a1-117">Um die neue Struktur zu verwenden, die aus dem **SizedSSortOrderSet** -Makro als Zeiger auf eine **SSortOrderSet** -Struktur resultiert, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a22a1-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="a22a1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a22a1-118">See also</span></span>

- [<span data-ttu-id="a22a1-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a22a1-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="a22a1-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="a22a1-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

