---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412835"
---
# <a name="prop_type"></a><span data-ttu-id="8fb76-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="8fb76-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="8fb76-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fb76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fb76-105">Gibt den Eigenschaftentyp eines angegebenen Eigenschaftstags zurück.</span><span class="sxs-lookup"><span data-stu-id="8fb76-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fb76-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8fb76-106">Header file:</span></span>  <br/> |<span data-ttu-id="8fb76-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fb76-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8fb76-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="8fb76-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="8fb76-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8fb76-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="8fb76-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fb76-110">Parameters</span></span>

 <span data-ttu-id="8fb76-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="8fb76-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="8fb76-112">Eigenschaftstag, das den zurückgegebenen Eigenschaftentyp enthält.</span><span class="sxs-lookup"><span data-stu-id="8fb76-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8fb76-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fb76-113">Remarks</span></span>

<span data-ttu-id="8fb76-114">Das **PROP_TYPE** kann verwendet werden, um den Typ einer Eigenschaft zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8fb76-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="8fb76-115">Wenn Sie z. B. PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) aufrufen, wird der Wert PT_BINARY zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8fb76-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="8fb76-116">Jedes Eigenschaftstag enthält den Eigenschaftentyp im Wort mit niedriger Reihenfolge (Bits 0 bis 15) und den Eigenschaftenbezeichner im Wort mit hoher Ordnung (Bits 16 bis 31).</span><span class="sxs-lookup"><span data-stu-id="8fb76-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="8fb76-117">Das **PROP_TYPE** extrahiert den Eigenschaftentyp und legt ihn in bits 0 bis 15 der ganzen Zahl, die zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fb76-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="8fb76-118">Die verbleibenden Bits des Rückgabewerts werden auf Nullen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8fb76-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fb76-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fb76-119">See also</span></span>



[<span data-ttu-id="8fb76-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8fb76-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8fb76-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="8fb76-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

