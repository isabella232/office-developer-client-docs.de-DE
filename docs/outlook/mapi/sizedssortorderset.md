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
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572564"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="65bdc-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="65bdc-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="65bdc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65bdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65bdc-105">Erstellt eine benannte [SSortOrderSet](ssortorderset.md) -Struktur, die eine angegebene Anzahl von Sortierreihenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="65bdc-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65bdc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="65bdc-106">Header file:</span></span>  <br/> |<span data-ttu-id="65bdc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65bdc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="65bdc-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="65bdc-108">Related structure:</span></span>  <br/> |<span data-ttu-id="65bdc-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="65bdc-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="65bdc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65bdc-110">Parameters</span></span>

<span data-ttu-id="65bdc-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="65bdc-111">__csort_</span></span>
  
> <span data-ttu-id="65bdc-112">Anzahl der Sortierreihenfolgen, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="65bdc-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="65bdc-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="65bdc-113">__name_</span></span>
  
> <span data-ttu-id="65bdc-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="65bdc-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65bdc-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="65bdc-115">Remarks</span></span>

<span data-ttu-id="65bdc-116">Verwenden Sie das Makro **SizedSSortOrderSet** , erstellen Sie eine Sortierreihenfolge mit expliziten Grenzen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="65bdc-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="65bdc-117">Um die neue Struktur verwenden, die als Zeiger auf eine **SSortOrderSet** -Struktur aus dem Makro **SizedSSortOrderSet** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="65bdc-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="65bdc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65bdc-118">See also</span></span>

- [<span data-ttu-id="65bdc-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="65bdc-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="65bdc-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="65bdc-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

