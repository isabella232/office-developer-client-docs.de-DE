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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439702"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="a6e9b-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="a6e9b-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="a6e9b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6e9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6e9b-105">Beschreibt eine Liste mit mehreren Werten, die in einem Dialogfeld angezeigt wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6e9b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a6e9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6e9b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a6e9b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="a6e9b-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="a6e9b-108">Members</span></span>

 <span data-ttu-id="a6e9b-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a6e9b-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a6e9b-110">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a6e9b-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="a6e9b-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="a6e9b-112">Property-Tag für eine mehrwertige Eigenschaft vom Typ PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6e9b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6e9b-113">Remarks</span></span>

<span data-ttu-id="a6e9b-114">Eine **DTBLMVLISTBOX** -Struktur beschreibt eine standardmäßige mehrwertige Liste mit einer schreibgeschützten Liste von Elementen.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="a6e9b-115">Bei Verwendung einer standardmäßigen mehrwertigen Liste werden die Werte sofort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="a6e9b-116">Die angezeigten Daten stammen aus der im **ulMVPropTag** -Element angegebenen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="a6e9b-117">Es ist nicht erforderlich, von der Eigenschaften Schnittstelle zu lesen, die der Anzeigetabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="a6e9b-118">Da Benutzer keine Auswahl aus diesen Listentypen treffen können, werden auch keine Daten in die Eigenschaften Schnittstelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="a6e9b-119">Nur mehrwertige Zeichenfolgeneigenschaften werden für die mehrwertige Liste unterstützt. andere mehrwertige Eigenschaftstypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="a6e9b-120">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a6e9b-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="a6e9b-121">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="a6e9b-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6e9b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6e9b-122">See also</span></span>



[<span data-ttu-id="a6e9b-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="a6e9b-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="a6e9b-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a6e9b-124">MAPI Structures</span></span>](mapi-structures.md)

