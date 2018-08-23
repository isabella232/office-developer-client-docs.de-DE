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
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573124"
---
# <a name="propid"></a><span data-ttu-id="f6cd7-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="f6cd7-103">PROP_ID</span></span>

  
  
<span data-ttu-id="f6cd7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6cd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6cd7-105">Gibt den Bezeichner eines angegebenen Eigenschaft-Tags.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6cd7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f6cd7-106">Header file:</span></span>  <br/> |<span data-ttu-id="f6cd7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6cd7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f6cd7-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="f6cd7-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="f6cd7-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f6cd7-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="f6cd7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6cd7-110">Parameters</span></span>

 <span data-ttu-id="f6cd7-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="f6cd7-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="f6cd7-112">Eigenschafts-Tag mit dem Bezeichner zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6cd7-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f6cd7-113">Remarks</span></span>

<span data-ttu-id="f6cd7-114">Jede Eigenschaftentag enthält den Eigenschaftstyp in das niederwertige Wort (Bits 0 bis 15) und der Eigenschaft-ID in das hohe Word (Bits 16 bis 31).</span><span class="sxs-lookup"><span data-stu-id="f6cd7-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="f6cd7-115">Das Makro **eigensch_id** extrahiert Bezeichner der und legt es in Bits 0 bis 15, der die ganze Zahl zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="f6cd7-116">Die verbleibenden Bits des Rückgabewerts werden für Nullen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="f6cd7-117">Das Makro **eigensch_id** kann verwendet werden, um einen Bezeichner zum Übergeben an [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="f6cd7-118">**GetNamesFromIDs** abgerufen, der Name der Eigenschaft einen Bezeichner für eine benannte Eigenschaft zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f6cd7-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6cd7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6cd7-119">See also</span></span>



[<span data-ttu-id="f6cd7-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f6cd7-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f6cd7-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="f6cd7-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

