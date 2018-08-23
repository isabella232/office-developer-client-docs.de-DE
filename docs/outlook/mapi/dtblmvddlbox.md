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
ms.openlocfilehash: 910f779f3463ee5dccd052655a442ef24c2cce58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570681"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="cb5aa-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="cb5aa-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="cb5aa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb5aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb5aa-105">Beschreibt ein Dropdown-Listenfeld, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb5aa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cb5aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="cb5aa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb5aa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="cb5aa-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="cb5aa-108">Members</span></span>

 <span data-ttu-id="cb5aa-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="cb5aa-109">**ulFlags**</span></span>
  
> <span data-ttu-id="cb5aa-110">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cb5aa-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="cb5aa-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="cb5aa-112">Eigenschaftentag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="cb5aa-113">Die unterschiedlichen Werte dieser Eigenschaft werden als unterschiedliche Einträge in der Dropdown-Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb5aa-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="cb5aa-114">Remarks</span></span>

<span data-ttu-id="cb5aa-115">Eine Struktur **DTBLMVDDLBOX** beschreibt eine mehrwertige Dropdown-Liste eine schreibgeschützte Liste von Elementen.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="cb5aa-116">Mithilfe ein mehrwertiges Dropdown-Listenfeld werden Werte angezeigt, wenn ein Benutzer auf eine Bildlaufleiste klickt.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="cb5aa-117">Die Daten, die angezeigt werden, stammt aus der Eigenschaft im **UlMVPropTag** -Member identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="cb5aa-118">Es ist nicht erforderlich zum Lesen aus der Eigenschaft-Schnittstelle, die das Display-Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="cb5aa-119">Darüber hinaus, da Benutzer nicht vor dieser Art von Listenfelder eine Auswahl treffen können, werden Daten nicht auf die Eigenschaft Schnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="cb5aa-120">Nur mehrwertige Zeichenfolgeneigenschaften werden für die mehrwertige Dropdown-Liste unterstützt. andere mehrwertige Eigenschaft werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="cb5aa-121">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cb5aa-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="cb5aa-122">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cb5aa-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb5aa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb5aa-123">See also</span></span>



[<span data-ttu-id="cb5aa-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="cb5aa-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="cb5aa-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="cb5aa-125">MAPI Structures</span></span>](mapi-structures.md)

