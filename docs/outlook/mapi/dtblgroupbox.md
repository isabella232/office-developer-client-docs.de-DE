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
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576316"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="6e314-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="6e314-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="6e314-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e314-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e314-105">Beschreibt ein Gruppenfeld-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e314-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e314-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6e314-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e314-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e314-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6e314-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="6e314-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="6e314-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="6e314-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="6e314-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="6e314-110">Members</span></span>

 <span data-ttu-id="6e314-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="6e314-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="6e314-112">Die Position im Speicher der Zeichenfolge, die das Gruppenfeld begleitet.</span><span class="sxs-lookup"><span data-stu-id="6e314-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="6e314-113">Wenn angezeigt wird, wird diese auf der oberen, linken Seite des Felds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e314-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="6e314-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6e314-114">**ulFlags**</span></span>
  
> <span data-ttu-id="6e314-115">Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabel** Member.</span><span class="sxs-lookup"><span data-stu-id="6e314-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="6e314-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6e314-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="6e314-117">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e314-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6e314-118">Die Beschriftung wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6e314-118">The label is in Unicode format.</span></span> <span data-ttu-id="6e314-119">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6e314-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e314-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6e314-120">Remarks</span></span>

<span data-ttu-id="6e314-121">Eine Struktur **DTBLGROUPBOX** beschreibt ein Gruppenfeld-Steuerelement, das verwendet wird, um andere Steuerelemente im Dialogfeld visuell zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6e314-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="6e314-122">Das Hervorheben Verfahren besteht im angrenzenden die andere Steuerelemente als Feld.</span><span class="sxs-lookup"><span data-stu-id="6e314-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="6e314-123">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6e314-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="6e314-124">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="6e314-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e314-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e314-125">See also</span></span>



[<span data-ttu-id="6e314-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="6e314-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="6e314-127">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6e314-127">MAPI Structures</span></span>](mapi-structures.md)

