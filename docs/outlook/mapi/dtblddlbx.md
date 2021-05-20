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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438848"
---
# <a name="dtblddlbx"></a><span data-ttu-id="e3ec5-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="e3ec5-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="e3ec5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3ec5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3ec5-105">Beschreibt ein Dropdownlistensteuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3ec5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e3ec5-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3ec5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3ec5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="e3ec5-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e3ec5-108">Members</span></span>

 <span data-ttu-id="e3ec5-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e3ec5-109">**ulFlags**</span></span>
  
> <span data-ttu-id="e3ec5-110">Reserviert, muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="e3ec5-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="e3ec5-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="e3ec5-112">Eigenschaftstag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="e3ec5-113">Diese Eigenschaft ist eine der Spalten in der Vom **ulPRTableName-Element** identifizierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="e3ec5-114">Die Werte für diese Eigenschaft werden in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="e3ec5-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="e3ec5-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="e3ec5-116">Eigenschaftstag für eine Eigenschaft eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-116">Property tag for a property of any type.</span></span> <span data-ttu-id="e3ec5-117">Diese Eigenschaft ist eine der Spalten in der Vom **ulPRTableName-Element** identifizierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="e3ec5-118">Wenn der Benutzer der Liste einen Eigenschaftswert für das **ulPRDisplayProperty-Element** aus den Zeilen der Tabelle auswählt, die vom **ulPRTableName-Element** identifiziert werden, wird das entsprechende **ulPRSetProperty-Element** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="e3ec5-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="e3ec5-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="e3ec5-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="e3ec5-121">Die Tabelle sollte zwei Spalten enthalten: **ulPRDisplayProperty** und **ulPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="e3ec5-122">Die Zeilen der Tabelle sollten den Elementen in der Liste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3ec5-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3ec5-123">Remarks</span></span>

<span data-ttu-id="e3ec5-124">Eine **DTBLDDLBX-Struktur** beschreibt ein Dropdownlistensteuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer es erweitert.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="e3ec5-125">Die drei von den Eigenschaftstags identifizierten Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzeigen und eine zugehörige Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="e3ec5-126">Das **ulPRTableName-Element** ist ein Tabellenobjekt, auf das über einen Aufruf von [IMAPIProp::OpenProperty zugegriffen wird.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="e3ec5-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="e3ec5-127">Die Tabelle verfügt über zwei Spalten: eine Spalte für die eigenschaft, die vom **ulPRDisplayProperty-Element** identifiziert wird, und die andere für die Eigenschaft, die vom **ulPRSetProperty-Element** identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="e3ec5-128">Die **ulPRDisplayProperty-Eigenschaft** steuert die Listenanzeige.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="e3ec5-129">Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um die entsprechende Eigenschaft wie vom **ulPRSetProperty-Element** identifiziert zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e3ec5-130">Dies bedeutet, dass die Eigenschaft in derselben Zeile wie die ausgewählte Anzeigeeigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="e3ec5-131">Das **ulPRSetProperty-Element** kann nicht auf PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="e3ec5-132">Ein Anfangswert wird in der Liste angezeigt, wenn MAPI die eigenschaft abgerufen hat, die durch das **ulPRSetProperty-Element** durch einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) dargestellt wurde und eine Zeile in der Tabelle mit dem Wert für das **ulPRSetProperty-Element** gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="e3ec5-133">Der anfängliche angezeigte Wert ist der Inhalt der **ulPRDisplayProperty-Spalte** aus dieser Zeile, die der Eigenschaft im **ulPRDisplayProperty-Element** der Struktur entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="e3ec5-134">Der von **GetProps** zurückgegebene Wert für die vom **ulPRDisplayProperty-Element** identifizierte Eigenschaft wird zum Anfänglichen Wert, der angezeigt wird, wenn die Liste zum ersten Mal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e3ec5-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="e3ec5-135">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e3ec5-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e3ec5-136">Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e3ec5-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="e3ec5-137">Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e3ec5-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3ec5-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3ec5-138">See also</span></span>



[<span data-ttu-id="e3ec5-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e3ec5-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="e3ec5-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="e3ec5-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="e3ec5-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e3ec5-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="e3ec5-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e3ec5-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="e3ec5-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e3ec5-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="e3ec5-144">Implementierung der Anzeigetabelle</span><span class="sxs-lookup"><span data-stu-id="e3ec5-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="e3ec5-145">Anzeigen von Tabellen</span><span class="sxs-lookup"><span data-stu-id="e3ec5-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="e3ec5-146">Übersicht über den MAPI-Eigenschaftstyp</span><span class="sxs-lookup"><span data-stu-id="e3ec5-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

