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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338661"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="f98dd-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f98dd-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="f98dd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f98dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f98dd-105">Beschreibt ein Gruppenfeld-Steuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f98dd-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f98dd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f98dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="f98dd-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f98dd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f98dd-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="f98dd-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="f98dd-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="f98dd-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="f98dd-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="f98dd-110">Members</span></span>

 <span data-ttu-id="f98dd-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="f98dd-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="f98dd-112">Position im Arbeitsspeicher der Zeichenfolge, die das Gruppenfeld begleitet.</span><span class="sxs-lookup"><span data-stu-id="f98dd-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="f98dd-113">Wenn diese Option angezeigt wird, wird Sie oben links im Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f98dd-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="f98dd-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f98dd-114">**ulFlags**</span></span>
  
> <span data-ttu-id="f98dd-115">Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabel** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f98dd-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="f98dd-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f98dd-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="f98dd-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f98dd-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f98dd-118">Die Bezeichnung ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="f98dd-118">The label is in Unicode format.</span></span> <span data-ttu-id="f98dd-119">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="f98dd-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f98dd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f98dd-120">Remarks</span></span>

<span data-ttu-id="f98dd-121">Eine **DTBLGROUPBOX** -Struktur beschreibt ein Gruppenfeld-Steuerelement, mit dem andere Steuerelemente im Dialogfeld visuell zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f98dd-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="f98dd-122">Die Hervorhebungs Technik umfasst das umschließen der anderen Steuerelemente durch ein Feld.</span><span class="sxs-lookup"><span data-stu-id="f98dd-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="f98dd-123">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f98dd-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f98dd-124">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="f98dd-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f98dd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f98dd-125">See also</span></span>



[<span data-ttu-id="f98dd-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f98dd-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="f98dd-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f98dd-127">MAPI Structures</span></span>](mapi-structures.md)

