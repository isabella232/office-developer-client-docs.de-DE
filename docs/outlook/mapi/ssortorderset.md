---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1604c4a1a0d1bf4008595b0d150b4f7eb3d1c2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795625"
---
# <a name="ssortorderset"></a><span data-ttu-id="db62f-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="db62f-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="db62f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db62f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db62f-105">Definiert eine Auflistung von Sortierschlüsseln für eine Tabelle, die für die Standard- oder kategorisierte Sortierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db62f-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db62f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="db62f-106">Header file:</span></span>  <br/> |<span data-ttu-id="db62f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db62f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="db62f-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="db62f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="db62f-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="db62f-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="db62f-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="db62f-110">Members</span></span>

 <span data-ttu-id="db62f-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="db62f-111">**cSorts**</span></span>
  
> <span data-ttu-id="db62f-112">Anzahl der [SSortOrder](ssortorder.md) -Strukturen, die im **aSort** -Member enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="db62f-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="db62f-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="db62f-113">**cCategories**</span></span>
  
> <span data-ttu-id="db62f-114">Anzahl der Spalten, die die Kategorie Spalten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="db62f-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="db62f-115">Mögliche Werte reichen von 0 (null), die eine Sortierung nicht kategorisiert oder standard angibt, der durch die **cSorts** Mitglied angegebenen Nummer.</span><span class="sxs-lookup"><span data-stu-id="db62f-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="db62f-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="db62f-116">**cExpanded**</span></span>
  
> <span data-ttu-id="db62f-117">Anzahl der Kategorien, die im erweiterten Zustand, starten, in dem alle Zeilen, die für die Kategorie gelten in der Tabellenansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="db62f-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="db62f-118">Mögliche Werte reichen von 0 bis auf die Anzahl von **cCategories**angegeben.</span><span class="sxs-lookup"><span data-stu-id="db62f-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="db62f-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="db62f-119">**aSort**</span></span>
  
> <span data-ttu-id="db62f-120">Array von **SSortOrder** -Strukturen, jede eine Sortierreihenfolge definieren.</span><span class="sxs-lookup"><span data-stu-id="db62f-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="db62f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db62f-121">Remarks</span></span>

<span data-ttu-id="db62f-122">Eine **SSortOrderSet** Struktur wird für die Definition mehrerer Sortierreihenfolgen für die Standard- und kategorisierte Sortierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="db62f-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="db62f-123">Jede **SSortOrderSet** -Datenstruktur enthält mindestens eine **SSortOrder** Struktur definieren die Richtung der Sortierung und die Spalte, die als Sortierschlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db62f-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="db62f-124">Diese Spalte wird für die kategorisierten Sortierung als die Kategorie verwendet.</span><span class="sxs-lookup"><span data-stu-id="db62f-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="db62f-125">Wenn der Wert des Elements **cSorts** den Wert des Elements **cCategories** überschreitet, es sind weitere Sortierschlüsseln als Kategorien, und Kategorien aus der Spalten, die im Array **SSortOrder** ersten angezeigt werden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="db62f-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="db62f-126">Wenn **cSorts** auf 3 festgelegt ist und **cCategories** auf 2 festgelegt wird, werden die Spalten beschrieben, die von der **UlPropTag** Mitglied die ersten beiden Einträge im Array **SSortOrder** wie die Kategorie Spalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="db62f-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="db62f-127">Der erste Eintrag dient als die Kategorie der obersten Ebene gruppieren; der zweite Eintrag als sekundäre Gruppierung.</span><span class="sxs-lookup"><span data-stu-id="db62f-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="db62f-128">Alle Zeilen, die die Spalten zwei Kategorie entsprechen werden mit den Sortierschlüssel definiert im dritten Eintrag sortiert.</span><span class="sxs-lookup"><span data-stu-id="db62f-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="db62f-129">Das **cExpanded** -Element gibt die Anzahl der Rubriken, die auf den ersten erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="db62f-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="db62f-130">Wenn mehrere Kategorien vorhanden sind, wird die Implementierung der Tabelle beginnt mit der ersten Spalte, als Kategorie festgelegt werden sollen und sequenziell mit den nachfolgenden Kategorie Spalten wird fortgesetzt, bis die Anzahl der **cCategories** überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="db62f-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="db62f-131">Wenn mehrere Kategorie Spalten als erweiterte Spalten vorhanden sind vorhanden sind, werden die Spalten Kategorie reduziert.</span><span class="sxs-lookup"><span data-stu-id="db62f-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="db62f-132">Wenn **cExpanded** gleich NULL ist, steht nur die oberste Ebene Überschrift-Zeile der Tabelle Benutzer für die Anzeige.</span><span class="sxs-lookup"><span data-stu-id="db62f-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="db62f-133">Wenn **cExpanded** eins kleiner ist als die Anzahl der Rubriken gleich ist, sind alle Überschriftenzeilen und keine Endknoten Zeile verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db62f-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="db62f-134">Wenn die Anzahl der Rubriken **cExpanded** entspricht, wird die Tabelle vollständig erweitert.</span><span class="sxs-lookup"><span data-stu-id="db62f-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="db62f-135">Weitere Informationen zu Standard- und kategorisierten Sortieren finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="db62f-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db62f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db62f-136">See also</span></span>



[<span data-ttu-id="db62f-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="db62f-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="db62f-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="db62f-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="db62f-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="db62f-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="db62f-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="db62f-140">MAPI Structures</span></span>](mapi-structures.md)

