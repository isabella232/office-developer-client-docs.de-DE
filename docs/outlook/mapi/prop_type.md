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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795307"
---
# <a name="proptype"></a><span data-ttu-id="2e670-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="2e670-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="2e670-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e670-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e670-105">Gibt den Eigenschaftstyp von einem Tag für die angegebene Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="2e670-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e670-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2e670-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e670-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e670-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2e670-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="2e670-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="2e670-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2e670-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="2e670-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e670-110">Parameters</span></span>

 <span data-ttu-id="2e670-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="2e670-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="2e670-112">Eigenschafts-Tag, die den Eigenschaftentyp zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e670-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e670-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e670-113">Remarks</span></span>

<span data-ttu-id="2e670-114">Das Makro **PROP_TYPE** kann verwendet werden, um den Typ einer Eigenschaft ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2e670-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="2e670-115">Beispielsweise Aufruf PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) führt den Wert PT_BINARY zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e670-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="2e670-116">Jede Eigenschaftentag enthält den Eigenschaftstyp in das niederwertige Wort (Bits 0 bis 15) und der Eigenschaft-ID in das hohe Word (Bits 16 bis 31).</span><span class="sxs-lookup"><span data-stu-id="2e670-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="2e670-117">Das Makro **PROP_TYPE** extrahiert den Eigenschaftentyp und legt es in Bits 0 bis 15, der die ganze Zahl zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e670-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="2e670-118">Die verbleibenden Bits des Rückgabewerts werden für Nullen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2e670-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e670-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e670-119">See also</span></span>



[<span data-ttu-id="2e670-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2e670-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2e670-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="2e670-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

