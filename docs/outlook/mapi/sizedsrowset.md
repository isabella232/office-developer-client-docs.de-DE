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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410931"
---
# <a name="sizedsrowset"></a><span data-ttu-id="45084-103">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="45084-103">SizedSRowSet</span></span>

<span data-ttu-id="45084-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45084-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45084-105">Erstellt eine benannte [SRowSet-Struktur,](srowset.md) die eine angegebene Anzahl von Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="45084-105">Creates a named [SRowSet](srowset.md) structure that contains a specified number of rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45084-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="45084-106">Header file:</span></span>  <br/> |<span data-ttu-id="45084-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45084-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="45084-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="45084-108">Related structure:</span></span>  <br/> |<span data-ttu-id="45084-109">**SRowSet**</span><span class="sxs-lookup"><span data-stu-id="45084-109">**SRowSet**</span></span> <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a><span data-ttu-id="45084-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45084-110">Parameters</span></span>

<span data-ttu-id="45084-111">_ _krähe_</span><span class="sxs-lookup"><span data-stu-id="45084-111">_ _crow_</span></span>
  
> <span data-ttu-id="45084-112">Anzahl der Zeilen, die in die neue Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="45084-112">Count of the number of rows to be included in the new structure.</span></span>
    
<span data-ttu-id="45084-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="45084-113">_ _name_</span></span>
  
> <span data-ttu-id="45084-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="45084-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45084-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45084-115">Remarks</span></span>

<span data-ttu-id="45084-116">Führen Sie die folgende Umsetzung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedSRowSet** als Zeiger auf eine **SRowSet-Struktur** resultiert:</span><span class="sxs-lookup"><span data-stu-id="45084-116">To use the new structure that results from the **SizedSRowSet** macro as a pointer to an **SRowSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a><span data-ttu-id="45084-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45084-117">See also</span></span>

- [<span data-ttu-id="45084-118">SRowSet</span><span class="sxs-lookup"><span data-stu-id="45084-118">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="45084-119">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="45084-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

