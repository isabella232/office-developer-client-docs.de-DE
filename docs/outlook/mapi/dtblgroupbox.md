---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438393"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="f2ad8-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f2ad8-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="f2ad8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2ad8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2ad8-105">Beschreibt ein Gruppenfeldsteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2ad8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f2ad8-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2ad8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2ad8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f2ad8-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="f2ad8-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f2ad8-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="f2ad8-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="f2ad8-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="f2ad8-110">Members</span></span>

 <span data-ttu-id="f2ad8-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="f2ad8-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="f2ad8-112">Position im Arbeitsspeicher der Zeichenzeichenfolge, die das Gruppenfeld begleitet.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="f2ad8-113">Wenn sie angezeigt wird, wird die Beschriftung oben links im Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="f2ad8-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f2ad8-114">**ulFlags**</span></span>
  
> <span data-ttu-id="f2ad8-115">Bitmaske von Flags, die verwendet werden, um das Format der Bezeichnung zu bestimmen, auf das das **ulbLpszLabel-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="f2ad8-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f2ad8-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="f2ad8-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f2ad8-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f2ad8-118">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-118">The label is in Unicode format.</span></span> <span data-ttu-id="f2ad8-119">Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2ad8-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2ad8-120">Remarks</span></span>

<span data-ttu-id="f2ad8-121">Eine **DTBLGROUPBOX-Struktur** beschreibt ein Gruppenfeldsteuerelement, das zum visuellen Zuordnen anderer Steuerelemente im Dialogfeld verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="f2ad8-122">Die Hervorhebungstechnik umfasst das Um umgeben der anderen Steuerelemente durch ein Feld.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="f2ad8-123">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f2ad8-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f2ad8-124">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f2ad8-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2ad8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2ad8-125">See also</span></span>



[<span data-ttu-id="f2ad8-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f2ad8-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="f2ad8-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f2ad8-127">MAPI Structures</span></span>](mapi-structures.md)

