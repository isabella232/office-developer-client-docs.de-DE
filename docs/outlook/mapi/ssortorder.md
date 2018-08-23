---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 331dc05b30390bb803d186f157e0fe9edb779ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571668"
---
# <a name="ssortorder"></a><span data-ttu-id="cd2b2-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="cd2b2-103">SSortOrder</span></span>
 
<span data-ttu-id="cd2b2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd2b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd2b2-105">Definiert, wie die Zeilen einer Tabelle, nach welcher Spalte die Sortierschlüssel und die Richtung der Sortierung als verwendet zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd2b2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cd2b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd2b2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd2b2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="cd2b2-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="cd2b2-108">Members</span></span>

<span data-ttu-id="cd2b2-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="cd2b2-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="cd2b2-110">Eigenschafts-Tag, die die Sortierung wichtige oder für eine kategorisierte Sortierung die Kategorie-Spalte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="cd2b2-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="cd2b2-111">**ulOrder**</span></span>
  
> <span data-ttu-id="cd2b2-112">Die Reihenfolge, in der die Daten sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="cd2b2-113">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cd2b2-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="cd2b2-114">TABLE_SORT_ASCEND: Die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="cd2b2-115">TABLE_SORT_COMBINE: Der Sortiervorgang sollte eine Kategorie erstellen, die die Eigenschaft als die Sortierung Schlüsselspalte im **UlPropTag** -Member mit die Sortierung Schlüsselspalte angegeben, in der vorherigen **SSortOrder** Struktur identifiziert kombiniert.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="cd2b2-116">TABLE_SORT_COMBINE kann nur verwendet werden, wenn die Struktur **SSortOrder** an mehrere Sortierreihenfolgen für eine kategorisierte Sortierung als Einstiegspunkt in einer [SSortOrderSet](ssortorderset.md) Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="cd2b2-117">TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder** Struktur in einer **SSortOrderSet** Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="cd2b2-118">TABLE_SORT_DESCEND: Die Tabelle sollte in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="cd2b2-119">TABLE_SORT_CATEG_MAX: Die Tabelle sollten auf den maximalen Wert des Elements **UlPropTag** für Datenzeilen in den durch die vorherigen Sortierreihenfolge in der Struktur **SSortOrderSet** angegebenen Kategorien sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="cd2b2-120">TABLE_SORT_CATEG_MIN: Die Tabelle sollten auf den minimalen Wert des Elements **UlPropTag** für Datenzeilen in den durch die vorherigen Sortierreihenfolge in der Struktur der in **SSortOrderSet** angegebenen Kategorien sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cd2b2-121">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="cd2b2-121">Remarks</span></span>

<span data-ttu-id="cd2b2-122">Eine **SSortOrder** -Struktur wird verwendet, um wird beschrieben, wie Sie einen standard Sortiervorgang oder ein kategorisierten Sortiervorgang durchführen.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="cd2b2-123">**SSortOrder** Strukturen werden in eine **SSortOrderSet** -Struktur, die mehrere Sortierschlüsseln und erfahren Sie, wie beschrieben in der Regel zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="cd2b2-124">**SSortOrderSet** Strukturen werden in die folgenden Funktionen und Interface-Methoden verwendet:</span><span class="sxs-lookup"><span data-stu-id="cd2b2-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="cd2b2-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="cd2b2-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="cd2b2-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="cd2b2-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="cd2b2-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="cd2b2-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="cd2b2-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="cd2b2-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="cd2b2-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="cd2b2-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="cd2b2-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="cd2b2-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="cd2b2-131">Der Bereich der zulässigen Spalten in einer Tabelle, die als Sortierschlüssel verwendet werden kann, hängt von den Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="cd2b2-132">Spalten, die Teil der aktuellen Spalte sind können immer als Sortierschlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="cd2b2-133">Jedoch bestimmt jeder Anbieter, ob Sortierschlüssel definiert werden können, mithilfe von Verfügbare Spalten, die nicht in der aktuellen Spalte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="cd2b2-134">Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable::QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn das Flag TBL_ALL_COLUMNS festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="cd2b2-135">Die **UlOrder** Datenmember gibt Richtungspfeile Reihenfolge und Kategorisierungsinformationen, beispielsweise nach Unterhaltungen ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)), d. h., gesprochene Thread, der eine Reihe von Nachrichten und Antworten ist.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="cd2b2-136">Zeilen können in ein aufsteigender oder absteigender Reihenfolge mit zuletzt positioniert alle NULL-Einträge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="cd2b2-137">Der Wert TABLE_SORT_COMBINE gibt an, dass in **UlPropTag** angegebene Spalte mit der vorherigen Kategoriespalte zu eine zusammengesetzte Kategorie bilden kombiniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="cd2b2-138">D. h., können Sie statt auf eindeutige Werte der einzelnen Spalten kategorisieren, TABLE_SORT_COMBINE zur Kategorisierung auf eindeutige Werte aus einer Kombination von Spalten.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="cd2b2-139">Beispielsweise könnte eine einzelne Kategorie auf Gruppennachrichten aus einem bestimmten Absender auf ein bestimmtes Thema definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="cd2b2-140">Festlegen des Werts auf TABLE_SORT_COMBINE Reduzierung der Anzahl von Kategorien in Zeilen, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="cd2b2-141">Mehrwertige Spalten sortieren wird universell von allen Implementierungen der Tabelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="cd2b2-142">Unterstützt, wenden Sie die MV_FLAG verwenden das Makro MVI_PROP das Eigenschafts-Tag im **UlPropTag** -Member zum Identifizieren des Sortierschlüssels als mehrwertige Spalte.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="cd2b2-143">Sortieren nach einer Spalte mit mehreren Werten basiert auf die einzelnen Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd2b2-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cd2b2-144">Die **UlOrder** Memberwerte TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN möglicherweise nicht in der herunterladbaren Headerdatei definiert werden derzeit ist, in diesem Fall können Sie diesen Code mithilfe der folgenden Werte hinzufügen: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="cd2b2-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="cd2b2-145">Weitere Informationen zu Standard- und kategorisierten Sortieren finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="cd2b2-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd2b2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd2b2-146">See also</span></span>

- [<span data-ttu-id="cd2b2-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="cd2b2-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="cd2b2-148">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="cd2b2-148">MAPI Structures</span></span>](mapi-structures.md)

