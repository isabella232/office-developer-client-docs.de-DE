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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795536"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="d58d2-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="d58d2-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="d58d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d58d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d58d2-105">Erstellt eine benannte Struktur, die eine [DTBLBUTTON](dtblbutton.md) -Struktur für die Beschreibung einer Schaltfläche und ein Label mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="d58d2-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d58d2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d58d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="d58d2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d58d2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d58d2-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="d58d2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d58d2-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d58d2-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="d58d2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58d2-110">Parameters</span></span>

 <span data-ttu-id="d58d2-111">_n_</span><span class="sxs-lookup"><span data-stu-id="d58d2-111">_n_</span></span>
  
> <span data-ttu-id="d58d2-112">Länge der Beschriftung, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d58d2-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="d58d2-113">_u_</span><span class="sxs-lookup"><span data-stu-id="d58d2-113">_u_</span></span>
  
> <span data-ttu-id="d58d2-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="d58d2-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d58d2-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d58d2-115">Remarks</span></span>

<span data-ttu-id="d58d2-116">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="d58d2-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="d58d2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d58d2-117">See also</span></span>



[<span data-ttu-id="d58d2-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="d58d2-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="d58d2-119">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="d58d2-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

