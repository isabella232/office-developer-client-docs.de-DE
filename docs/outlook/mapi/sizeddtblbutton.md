---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590344"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="46e55-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="46e55-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="46e55-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46e55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46e55-105">Erstellt eine benannte Struktur, die eine [DTBLBUTTON](dtblbutton.md) -Struktur für die Beschreibung einer Schaltfläche und ein Label mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="46e55-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46e55-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="46e55-106">Header file:</span></span>  <br/> |<span data-ttu-id="46e55-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46e55-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="46e55-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="46e55-108">Related structure:</span></span>  <br/> |<span data-ttu-id="46e55-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="46e55-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="46e55-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e55-110">Parameters</span></span>

 <span data-ttu-id="46e55-111">_n_</span><span class="sxs-lookup"><span data-stu-id="46e55-111">_n_</span></span>
  
> <span data-ttu-id="46e55-112">Länge der Beschriftung, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="46e55-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="46e55-113">_u_</span><span class="sxs-lookup"><span data-stu-id="46e55-113">_u_</span></span>
  
> <span data-ttu-id="46e55-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="46e55-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46e55-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="46e55-115">Remarks</span></span>

<span data-ttu-id="46e55-116">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="46e55-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="46e55-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46e55-117">See also</span></span>



[<span data-ttu-id="46e55-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="46e55-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="46e55-119">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="46e55-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

