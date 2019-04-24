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
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340103"
---
# <a name="dtblddlbx"></a><span data-ttu-id="45496-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="45496-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="45496-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45496-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45496-105">Beschreibt ein Dropdownlisten-Steuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45496-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45496-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="45496-106">Header file:</span></span>  <br/> |<span data-ttu-id="45496-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="45496-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="45496-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="45496-108">Members</span></span>

 <span data-ttu-id="45496-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="45496-109">**ulFlags**</span></span>
  
> <span data-ttu-id="45496-110">Reserviert, muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="45496-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="45496-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="45496-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="45496-112">Property-Tag für eine Eigenschaft vom Typ PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="45496-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="45496-113">Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **ulPRTableName** -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="45496-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="45496-114">Die Werte für diese Eigenschaft werden in der Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45496-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="45496-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="45496-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="45496-116">Property-Tag für eine Eigenschaft eines beliebigen Typs.</span><span class="sxs-lookup"><span data-stu-id="45496-116">Property tag for a property of any type.</span></span> <span data-ttu-id="45496-117">Diese Eigenschaft ist eine der Spalten in der Tabelle, die durch das **ulPRTableName** -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="45496-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="45496-118">Wenn der Benutzer der Liste einen Eigenschaftswert für das **ulPRDisplayProperty** -Element aus den Zeilen der Tabelle auswählt, die durch das **ulPRTableName** -Element identifiziert wird, wird das entsprechende **ulPRSetProperty** -Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45496-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="45496-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="45496-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="45496-120">Property-Tag für eine Table-Eigenschaft vom Typ PT_OBJECT, die mithilfe eines **openProperty** -Aufrufs geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="45496-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="45496-121">Die Tabelle sollte zwei Spalten aufweisen: **ulPRDisplayProperty** und **ulPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="45496-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="45496-122">Die Zeilen der Tabelle sollten den Elementen in der Liste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="45496-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45496-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45496-123">Remarks</span></span>

<span data-ttu-id="45496-124">Eine **DTBLDDLBX** -Struktur beschreibt ein Dropdownlisten-Steuerelement, das als einzelnes Element angezeigt wird, bis der Benutzer die Erweiterung auswählt.</span><span class="sxs-lookup"><span data-stu-id="45496-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="45496-125">Die drei durch die Property-Tags identifizierten Eigenschaften arbeiten zusammen, um die Informationen in der Liste anzuzeigen und eine zugehörige Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="45496-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="45496-126">Der **ulPRTableName** -Member ist ein Table-Objekt, auf das über einen Aufruf von [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="45496-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="45496-127">Die Tabelle enthält zwei Spalten: eine Spalte für die Eigenschaft, die vom **ulPRDisplayProperty** -Element identifiziert wird, und die andere für die Eigenschaft, die vom **ulPRSetProperty** -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="45496-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="45496-128">Die **ulPRDisplayProperty** -Eigenschaft steuert die Listenanzeige.</span><span class="sxs-lookup"><span data-stu-id="45496-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="45496-129">Wenn ein Benutzer einen der Werte aus der Anzeige auswählt, ruft MAPI [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um die entsprechende Eigenschaft festzulegen, die vom **ulPRSetProperty** -Mitglied identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="45496-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="45496-130">Dies hat zur Folge, dass die Eigenschaft in derselben Zeile wie die ausgewählte Anzeigeeigenschaft angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="45496-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="45496-131">Das **ulPRSetProperty** -Element kann nicht auf **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="45496-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="45496-132">In der Liste wird ein Anfangswert angezeigt, wenn MAPI die vom **ulPRSetProperty** -Element dargestellte Eigenschaft durch einen Aufruf von [IMAPIProp::](imapiprop-getprops.md) GetProps abgerufen und eine Zeile in der Tabelle mit dem Wert für das **ulPRSetProperty** -Element gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="45496-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="45496-133">Der anfänglich angezeigte Wert ist der Inhalt der **ulPRDisplayProperty** -Spalte aus dieser Zeile, die mit der-Eigenschaft im **ulPRDisplayProperty** -Element der Struktur übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="45496-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="45496-134">Der von getProps zurückgegebene Wert für die durch das **ulPRDisplayProperty** -Element angegebene Eigenschaft wird zum Anfangswert, der angezeigt wird, wenn die Liste zum ersten Mal angezeigt wird. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="45496-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="45496-135">Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="45496-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="45496-136">Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="45496-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="45496-137">Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="45496-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45496-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45496-138">See also</span></span>



[<span data-ttu-id="45496-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="45496-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="45496-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="45496-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="45496-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="45496-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="45496-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="45496-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="45496-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="45496-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="45496-144">Anzeigen der Tabellen Implementierung</span><span class="sxs-lookup"><span data-stu-id="45496-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="45496-145">Anzeige Tabellen</span><span class="sxs-lookup"><span data-stu-id="45496-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="45496-146">Übersicht über die MAPI-EigenschaftsTypen</span><span class="sxs-lookup"><span data-stu-id="45496-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

