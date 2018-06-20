---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2db95697cd98e66da9fb3d0cd0180b238c0a8dff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791594"
---
# <a name="dtblddlbx"></a><span data-ttu-id="a82a5-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="a82a5-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="a82a5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a82a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a82a5-105">Beschreibt ein Dropdown-Listenfeld-Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a82a5-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a82a5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a82a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="a82a5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a82a5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="a82a5-108">Members</span><span class="sxs-lookup"><span data-stu-id="a82a5-108">Members</span></span>

 <span data-ttu-id="a82a5-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a82a5-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a82a5-110">Reserviert, muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a82a5-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="a82a5-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="a82a5-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="a82a5-112">Eigenschaftentag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="a82a5-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="a82a5-113">Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **UlPRTableName** -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a82a5-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="a82a5-114">Die Werte für diese Eigenschaft sind in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a82a5-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="a82a5-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="a82a5-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="a82a5-116">Eigenschaftentag für eine Eigenschaft eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="a82a5-116">Property tag for a property of any type.</span></span> <span data-ttu-id="a82a5-117">Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **UlPRTableName** -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a82a5-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="a82a5-118">Wenn der Benutzer der Liste einen Eigenschaftswert für das Element **UlPRDisplayProperty** aus den Zeilen der Tabelle der Member **UlPRTableName** identifizierten auswählt, wird der entsprechende **UlPRSetProperty** Member festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a82a5-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="a82a5-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="a82a5-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="a82a5-120">Rufen Sie die Eigenschaftentag für ein Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe einer **OpenProperty** geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="a82a5-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="a82a5-121">Die Tabelle sollte zwei Spalten: **UlPRDisplayProperty** und **UlPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="a82a5-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="a82a5-122">Die Zeilen der Tabelle sollten die Elemente in der Liste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a82a5-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a82a5-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a82a5-123">Remarks</span></span>

<span data-ttu-id="a82a5-124">Eine Struktur **DTBLDDLBX** beschreibt ein Dropdown-Listenfeld-Steuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer entscheidet, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a82a5-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="a82a5-125">Die Eigenschaftentags identifizierten drei Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzuzeigen, und legen Sie eine verknüpfte-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a82a5-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="a82a5-126">Der **UlPRTableName** -Member ist ein Table-Objekt, das durch einen Aufruf von [IMAPIProp::OpenProperty](imapiprop-openproperty.md)zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a82a5-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="a82a5-127">Die Tabelle enthält zwei Spalten: eine Spalte für die Eigenschaft durch das **UlPRDisplayProperty** -Element, und das andere für die identifizierten **UlPRSetProperty** Members-Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a82a5-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="a82a5-128">Die **UlPRDisplayProperty** -Eigenschaft steuert die Anzeige der Browserliste.</span><span class="sxs-lookup"><span data-stu-id="a82a5-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="a82a5-129">Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) , um die entsprechende Eigenschaft festzulegen, wie durch das **UlPRSetProperty** -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a82a5-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="a82a5-130">Dies bedeutet, dass die Eigenschaft in der gleichen Zeile wie die ausgewählten Anzeigeeigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a82a5-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="a82a5-131">Das **UlPRSetProperty** -Element kann nicht auf **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a82a5-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="a82a5-132">Anfangswert wird in der Liste angezeigt, wenn MAPI dargestellte vom **UlPRSetProperty** Member durch einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) Eigenschaft abgerufen und befindet sich eine Zeile in der Tabelle mit dem Wert für den **UlPRSetProperty** Member hat.</span><span class="sxs-lookup"><span data-stu-id="a82a5-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="a82a5-133">Der erste angezeigte Wert entspricht dem Inhalt der **UlPRDisplayProperty** Spalte aus dieser Zeile, die die Eigenschaft im **UlPRDisplayProperty** -Member der Struktur entspricht.</span><span class="sxs-lookup"><span data-stu-id="a82a5-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="a82a5-134">Der von **GetProps** für die identifizierten **UlPRDisplayProperty** Members-Eigenschaft zurückgegebene Wert wird der erste Wert, der angezeigt wird, wenn die Liste zuerst angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a82a5-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="a82a5-135">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a82a5-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="a82a5-136">Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="a82a5-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="a82a5-137">Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a82a5-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a82a5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a82a5-138">See also</span></span>



[<span data-ttu-id="a82a5-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="a82a5-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="a82a5-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="a82a5-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="a82a5-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="a82a5-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="a82a5-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a82a5-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="a82a5-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a82a5-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="a82a5-144">Implementierung der Anzeige-Tabelle</span><span class="sxs-lookup"><span data-stu-id="a82a5-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="a82a5-145">Anzeigen von Tabellen</span><span class="sxs-lookup"><span data-stu-id="a82a5-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="a82a5-146">Übersicht über Typ von MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a82a5-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

