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
# <a name="sizedssortorderset"></a><span data-ttu-id="0dd14-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0dd14-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="0dd14-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd14-105">Erstellt eine benannte [SSortOrderSet-Struktur,](ssortorderset.md) die eine angegebene Anzahl von Sortierreihenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="0dd14-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dd14-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0dd14-106">Header file:</span></span>  <br/> |<span data-ttu-id="0dd14-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dd14-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0dd14-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="0dd14-108">Related structure:</span></span>  <br/> |<span data-ttu-id="0dd14-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="0dd14-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="0dd14-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dd14-110">Parameters</span></span>

<span data-ttu-id="0dd14-111">_ _csort_</span><span class="sxs-lookup"><span data-stu-id="0dd14-111">_ _csort_</span></span>
  
> <span data-ttu-id="0dd14-112">Anzahl der Sortierreihenfolgen, die in die neue Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0dd14-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="0dd14-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="0dd14-113">_ _name_</span></span>
  
> <span data-ttu-id="0dd14-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="0dd14-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0dd14-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0dd14-115">Remarks</span></span>

<span data-ttu-id="0dd14-116">Verwenden Sie **das Makro SizedSSortOrderSet,** um einen Sortierreihenfolgensatz mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0dd14-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="0dd14-117">Führen Sie die folgende Gliederung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedSSortOrderSet** als Zeiger auf eine **SSortOrderSet-Struktur** resultiert:</span><span class="sxs-lookup"><span data-stu-id="0dd14-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="0dd14-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd14-118">See also</span></span>

- [<span data-ttu-id="0dd14-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0dd14-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="0dd14-120">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="0dd14-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

