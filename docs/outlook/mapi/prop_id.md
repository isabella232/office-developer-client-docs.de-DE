---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409132"
---
# <a name="propid"></a><span data-ttu-id="600ac-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="600ac-103">PROP_ID</span></span>

  
  
<span data-ttu-id="600ac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="600ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="600ac-105">Gibt den Eigenschaftenbezeichner eines angegebenen Property-Tags zurück.</span><span class="sxs-lookup"><span data-stu-id="600ac-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="600ac-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="600ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="600ac-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="600ac-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="600ac-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="600ac-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="600ac-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="600ac-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="600ac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="600ac-110">Parameters</span></span>

 <span data-ttu-id="600ac-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="600ac-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="600ac-112">Property-Tag, das den zurückzugebenden Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="600ac-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="600ac-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="600ac-113">Remarks</span></span>

<span data-ttu-id="600ac-114">Jedes Property-Tag enthält den Eigenschaftentyp im niedrigwertigen Wort (Bits 0 bis 15) und den Eigenschaftenbezeichner im hochwertigen Wort (Bits 16 bis 31).</span><span class="sxs-lookup"><span data-stu-id="600ac-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="600ac-115">Das **PROP_ID** -Makro extrahiert den Eigenschaftenbezeichner und fügt ihn in Bits 0 bis 15 der zurückzugebenden Ganzzahl ein.</span><span class="sxs-lookup"><span data-stu-id="600ac-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="600ac-116">Die restlichen Bits des Rückgabewerts werden auf Nullen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="600ac-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="600ac-117">Das **PROP_ID** -Makro kann verwendet werden, um beispielsweise einen Bezeichner abzurufen, der an [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="600ac-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="600ac-118">**GetNamesFromIDs** Ruft den Eigenschaftennamen ab, der einem Bezeichner für eine benannte Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="600ac-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="600ac-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="600ac-119">See also</span></span>



[<span data-ttu-id="600ac-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="600ac-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="600ac-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="600ac-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

