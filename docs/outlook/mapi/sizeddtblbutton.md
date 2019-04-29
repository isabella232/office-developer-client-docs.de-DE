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
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421914"
---
# <a name="sizeddtblbutton"></a><span data-ttu-id="9f667-103">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="9f667-103">SizedDtblButton</span></span>

  
  
<span data-ttu-id="9f667-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f667-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f667-105">Erstellt eine benannte Struktur, die eine [DTBLBUTTON](dtblbutton.md) -Struktur zur Beschreibung einer Schaltfläche und einer Beschriftung einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="9f667-105">Creates a named structure that includes a [DTBLBUTTON](dtblbutton.md) structure for describing a button and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f667-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9f667-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f667-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9f667-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9f667-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="9f667-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9f667-109">**DTBLBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9f667-109">**DTBLBUTTON**</span></span> <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a><span data-ttu-id="9f667-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f667-110">Parameters</span></span>

 <span data-ttu-id="9f667-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9f667-111">_n_</span></span>
  
> <span data-ttu-id="9f667-112">Die Länge der Bezeichnung, die in die neue Struktur eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f667-112">Length of the label to be included in the new structure.</span></span>
    
 <span data-ttu-id="9f667-113">_u_</span><span class="sxs-lookup"><span data-stu-id="9f667-113">_u_</span></span>
  
> <span data-ttu-id="9f667-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="9f667-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f667-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f667-115">Remarks</span></span>

<span data-ttu-id="9f667-116">Die neue Struktur wird mit den folgenden Elementen erstellt:</span><span class="sxs-lookup"><span data-stu-id="9f667-116">The new structure is created with the following members:</span></span>
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a><span data-ttu-id="9f667-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f667-117">See also</span></span>



[<span data-ttu-id="9f667-118">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="9f667-118">DTBLBUTTON</span></span>](dtblbutton.md)


[<span data-ttu-id="9f667-119">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="9f667-119">Macros Related to Structures</span></span>](macros-related-to-structures.md)

