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
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438099"
---
# <a name="ssortorderset"></a><span data-ttu-id="5dd5a-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="5dd5a-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="5dd5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dd5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dd5a-105">Definiert eine Auflistung von Sortierschlüsseln für eine Tabelle, die für die standardmäßige oder kategorisierte Sortierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dd5a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5dd5a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5dd5a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5dd5a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5dd5a-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="5dd5a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="5dd5a-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="5dd5a-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="5dd5a-110">Members</span><span class="sxs-lookup"><span data-stu-id="5dd5a-110">Members</span></span>

 <span data-ttu-id="5dd5a-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="5dd5a-111">**cSorts**</span></span>
  
> <span data-ttu-id="5dd5a-112">Die Anzahl der [SSortOrder](ssortorder.md) -Strukturen, die im **einersortierreihenfolge** -Element enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="5dd5a-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="5dd5a-113">**cCategories**</span></span>
  
> <span data-ttu-id="5dd5a-114">Anzahl der Spalten, die als Category-Spalten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="5dd5a-115">Mögliche Werte reichen von NULL, die eine nicht kategorisierte oder Standardsortierung angibt, bis zu der vom **cSorts** -Element angegebenen Nummer.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="5dd5a-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="5dd5a-116">**cExpanded**</span></span>
  
> <span data-ttu-id="5dd5a-117">Die Anzahl der Kategorien, die in einem erweiterten Zustand beginnen, wobei alle Zeilen, die auf die Kategorie angewendet werden, in der Tabellenansicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="5dd5a-118">Mögliche Werte liegen zwischen 0 und der von **cCategories**angegebenen Zahl.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="5dd5a-119">**Einersortierreihenfolge**</span><span class="sxs-lookup"><span data-stu-id="5dd5a-119">**aSort**</span></span>
  
> <span data-ttu-id="5dd5a-120">Array von **SSortOrder** -Strukturen, die jeweils eine Sortierreihenfolge definieren.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5dd5a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dd5a-121">Remarks</span></span>

<span data-ttu-id="5dd5a-122">Eine **SSortOrderSet** -Struktur wird zum Definieren mehrerer Sortierreihenfolgen für die standardmäßige und kategorisierte Sortierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="5dd5a-123">Jede **SSortOrderSet** -Struktur enthält mindestens eine **SSortOrder** -Struktur, die die Richtung der Sortierung und die Spalte definiert, die als Sortierschlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="5dd5a-124">Für die kategorisierte Sortierung wird diese Spalte als Kategorie verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="5dd5a-125">Wenn der Wert des **cSorts** -Elements den Wert des **cCategories** -Elements überschreitet, gibt es mehr Sortierschlüssel als Kategorien, und Kategorien werden aus den Spalten erstellt, die zuerst im **SSortOrder** -Array angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="5dd5a-126">Wenn **cSorts** beispielsweise auf 3 festgelegt ist und **cCategories** auf 2 festgelegt ist, werden die Spalten, die durch das **ulPropTag** -Element der ersten beiden Einträge im **SSortOrder** -Array beschrieben werden, als Category-Spalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="5dd5a-127">Der erste Eintrag dient als Gruppierung der obersten Ebene; der zweite Eintrag als sekundäre Gruppierung.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="5dd5a-128">Alle Zeilen, die mit den beiden rubrikengruppen übereinstimmen, werden mit dem im dritten Eintrag definierten Sortierschlüssel sortiert.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="5dd5a-129">Das **cExpanded** -Element gibt die Anzahl der Kategorien an, die zuerst erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="5dd5a-130">Wenn es mehrere Kategorien gibt, beginnt die Tabellen Implementierung mit der ersten Spalte, die als Kategorie festgelegt werden soll, und wird in sequenzieller Reihenfolge mit den nachfolgenden Category-Spalten fortgesetzt, bis die Anzahl der **cCategories** überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="5dd5a-131">Wenn mehr Kategorien Spalten vorhanden sind als erweiterte Spalten, werden die Spalten für die Kategorie reduziert.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="5dd5a-132">Wenn **cExpanded** gleich NULL ist, steht der Tabellen Benutzer nur Überschriftenzeilen der obersten Ebene zur Anzeige zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="5dd5a-133">Ist **cExpanded** gleich 1 kleiner als die Anzahl der Kategorien, sind alle Überschriftenzeilen und keine der Blattzeilen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="5dd5a-134">Wenn **cExpanded** der Anzahl von Kategorien entspricht, wird die Tabelle vollständig erweitert.</span><span class="sxs-lookup"><span data-stu-id="5dd5a-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="5dd5a-135">Weitere Informationen zu standardmäßigen und kategorisierten Sortierungen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="5dd5a-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5dd5a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dd5a-136">See also</span></span>



[<span data-ttu-id="5dd5a-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="5dd5a-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="5dd5a-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="5dd5a-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="5dd5a-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="5dd5a-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="5dd5a-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5dd5a-140">MAPI Structures</span></span>](mapi-structures.md)

