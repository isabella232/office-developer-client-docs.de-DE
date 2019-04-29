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
# <a name="proptype"></a><span data-ttu-id="31292-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="31292-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="31292-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31292-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31292-105">Gibt den Eigenschaftentyp eines angegebenen Property-Tags zurück.</span><span class="sxs-lookup"><span data-stu-id="31292-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31292-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="31292-106">Header file:</span></span>  <br/> |<span data-ttu-id="31292-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="31292-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="31292-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="31292-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="31292-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="31292-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="31292-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="31292-110">Parameters</span></span>

 <span data-ttu-id="31292-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="31292-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="31292-112">Property-Tag, das den zurückzugebenden Eigenschaftentyp enthält.</span><span class="sxs-lookup"><span data-stu-id="31292-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31292-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31292-113">Remarks</span></span>

<span data-ttu-id="31292-114">Das **PROP_TYPE** -Makro kann verwendet werden, um den Typ einer Eigenschaft zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="31292-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="31292-115">Beispielsweise führt das Aufrufen von PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) dazu, dass der Wert PT_BINARY zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31292-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="31292-116">Jedes Property-Tag enthält den Eigenschaftentyp im niedrigwertigen Wort (Bits 0 bis 15) und den Eigenschaftenbezeichner im hochwertigen Wort (Bits 16 bis 31).</span><span class="sxs-lookup"><span data-stu-id="31292-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="31292-117">Das **PROP_TYPE** -Makro extrahiert den Eigenschaftentyp und fügt ihn in die Bits 0 bis 15 der zurückzugebenden Ganzzahl ein.</span><span class="sxs-lookup"><span data-stu-id="31292-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="31292-118">Die restlichen Bits des Rückgabewerts werden auf Nullen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="31292-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31292-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31292-119">See also</span></span>



[<span data-ttu-id="31292-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="31292-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="31292-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="31292-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

