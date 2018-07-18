---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791611"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="3895e-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="3895e-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="3895e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3895e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3895e-105">Beschreibt eine mehrwertige Liste, die in einem Dialogfeld angezeigt werden, die aus einer Tabelle anzeigen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3895e-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3895e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3895e-106">Header file:</span></span>  <br/> |<span data-ttu-id="3895e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3895e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="3895e-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="3895e-108">Members</span></span>

 <span data-ttu-id="3895e-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3895e-109">**ulFlags**</span></span>
  
> <span data-ttu-id="3895e-110">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="3895e-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3895e-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="3895e-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="3895e-112">Eigenschaftentag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="3895e-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3895e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3895e-113">Remarks</span></span>

<span data-ttu-id="3895e-114">Eine Struktur **DTBLMVLISTBOX** beschreibt eine standard mehrwertige Liste, die eine schreibgeschützte Liste der Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="3895e-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="3895e-115">Eine mehrwertige Liste verwenden, werden die Werte sofort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3895e-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="3895e-116">Die Daten, die angezeigt werden, stammt aus der Eigenschaft im **UlMVPropTag** -Member identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3895e-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="3895e-117">Es ist nicht erforderlich zum Lesen aus der Eigenschaft-Schnittstelle, die das Display-Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3895e-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="3895e-118">Darüber hinaus, da der Benutzer eine Auswahl aus Risiko dieser Arten von Listen nicht können, werden Daten nicht auf die Eigenschaft Schnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="3895e-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="3895e-119">Nur mehrwertige Zeichenfolgeneigenschaften werden für die Liste mit mehreren Werten unterstützt. andere mehrwertige Eigenschaft werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3895e-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="3895e-120">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3895e-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3895e-121">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="3895e-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3895e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3895e-122">See also</span></span>



[<span data-ttu-id="3895e-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3895e-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="3895e-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3895e-124">MAPI Structures</span></span>](mapi-structures.md)

