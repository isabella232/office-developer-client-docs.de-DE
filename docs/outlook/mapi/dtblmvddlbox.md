---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420745"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="025e8-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="025e8-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="025e8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="025e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="025e8-105">Beschreibt eine Dropdownliste, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="025e8-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="025e8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="025e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="025e8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="025e8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="025e8-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="025e8-108">Members</span></span>

 <span data-ttu-id="025e8-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="025e8-109">**ulFlags**</span></span>
  
> <span data-ttu-id="025e8-110">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="025e8-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="025e8-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="025e8-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="025e8-112">Eigenschaftstag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="025e8-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="025e8-113">Die verschiedenen Werte dieser Eigenschaft werden als unterschiedliche Einträge in der Dropdownliste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="025e8-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="025e8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="025e8-114">Remarks</span></span>

<span data-ttu-id="025e8-115">Eine **DTBLMVDDLBOX-Struktur** beschreibt eine mehrwertige Dropdownliste eine schreibgeschützte Liste von Elementen.</span><span class="sxs-lookup"><span data-stu-id="025e8-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="025e8-116">Mithilfe einer mehrwertigen Dropdownliste werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt.</span><span class="sxs-lookup"><span data-stu-id="025e8-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="025e8-117">Die angezeigten Daten stammen aus der Im **ulMVPropTag-Element identifizierten** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="025e8-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="025e8-118">Es ist nicht erforderlich, von der Eigenschaftenschnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="025e8-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="025e8-119">Da Benutzer keine Auswahl aus diesen Listenfeldern treffen können, werden daten nicht in die Eigenschaftsschnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="025e8-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="025e8-120">Für die mehrwertige Dropdownliste werden nur mehrwertige Zeichenfolgeneigenschaften unterstützt. Andere mehrwertige Eigenschaftstypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="025e8-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="025e8-121">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="025e8-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="025e8-122">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="025e8-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="025e8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="025e8-123">See also</span></span>



[<span data-ttu-id="025e8-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="025e8-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="025e8-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="025e8-125">MAPI Structures</span></span>](mapi-structures.md)

