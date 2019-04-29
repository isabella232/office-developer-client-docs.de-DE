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
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439723"
---
# <a name="ssortorder"></a><span data-ttu-id="798a6-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="798a6-103">SSortOrder</span></span>
 
<span data-ttu-id="798a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="798a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="798a6-105">Definiert, wie die Zeilen einer Tabelle, die Spalte, die als Sortierschlüssel verwendet werden soll, und die Richtung der Sortierung sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="798a6-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="798a6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="798a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="798a6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="798a6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="798a6-108">Members</span><span class="sxs-lookup"><span data-stu-id="798a6-108">Members</span></span>

<span data-ttu-id="798a6-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="798a6-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="798a6-110">Eigenschaftentag, der den Sortierschlüssel oder für eine kategorisierte Sortierung die Spalte Category identifiziert.</span><span class="sxs-lookup"><span data-stu-id="798a6-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="798a6-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="798a6-111">**ulOrder**</span></span>
  
> <span data-ttu-id="798a6-112">Die Reihenfolge, in der die Daten sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="798a6-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="798a6-113">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="798a6-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="798a6-114">TABLE_SORT_ASCEND: die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="798a6-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="798a6-115">TABLE_SORT_COMBINE: der Sortiervorgang sollte eine Kategorie erstellen, die die Eigenschaft, die als Sortierschlüsselspalte im **ulPropTag** -Element identifiziert wurde, mit der in der vorherigen **SSortOrder** -Struktur angegebenen Sortierschlüsselspalte kombiniert.</span><span class="sxs-lookup"><span data-stu-id="798a6-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="798a6-116">TABLE_SORT_COMBINE kann nur verwendet werden, wenn die **SSortOrder** -Struktur als Eintrag in einer [SSortOrderSet](ssortorderset.md) -Struktur verwendet wird, um mehrere Sortierreihenfolgen für eine kategorisierte Sortierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="798a6-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="798a6-117">TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder** -Struktur in einer **SSortOrderSet** -Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="798a6-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="798a6-118">TABLE_SORT_DESCEND: die Tabelle sollte in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="798a6-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="798a6-119">TABLE_SORT_CATEG_MAX: die Tabelle sollte nach dem Maximalwert des **ulPropTag** -Elements für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der **SSortOrderSet** -Struktur angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="798a6-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="798a6-120">TABLE_SORT_CATEG_MIN: die Tabelle sollte nach dem Minimalwert des **ulPropTag** -Elements für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der in **SSortOrderSet** -Struktur angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="798a6-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="798a6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="798a6-121">Remarks</span></span>

<span data-ttu-id="798a6-122">Eine **SSortOrder** -Struktur wird verwendet, um die Ausführung eines Standard Sortiervorgangs oder eines kategorisierten Sortiervorgangs zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="798a6-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="798a6-123">**SSortOrder** -Strukturen werden in der Regel in einer **SSortOrderSet** -Struktur kombiniert, um mehrere Sortierschlüssel und-Richtungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="798a6-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="798a6-124">**SSortOrderSet** -Strukturen werden in den folgenden Funktionen und Schnittstellenmethoden verwendet:</span><span class="sxs-lookup"><span data-stu-id="798a6-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="798a6-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="798a6-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="798a6-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="798a6-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="798a6-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="798a6-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="798a6-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="798a6-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="798a6-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="798a6-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="798a6-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="798a6-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="798a6-131">Der zulässige Spalten Umfang in einer Tabelle, der als Sortierschlüssel verwendet werden kann, hängt vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="798a6-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="798a6-132">Spalten, die Teil des aktuellen Spaltensatzes sind, können immer als Sortierschlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="798a6-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="798a6-133">Jeder Anbieter bestimmt jedoch, ob Sortierschlüssel mithilfe verfügbarer Spalten definiert werden können, die nicht in der aktuellen Spaltengruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="798a6-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="798a6-134">Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable:: QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn das TBL_ALL_COLUMNS-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="798a6-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="798a6-135">Das **ulOrder** -Element gibt sowohl Richtungs Reihenfolge-als auch Kategorisierungsinformationen an, beispielsweise nach Unterhaltung ([eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)), also konversationsthread, bei dem es sich um eine Reihe von Nachrichten und Antworten handelt.</span><span class="sxs-lookup"><span data-stu-id="798a6-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="798a6-136">Zeilen können in aufsteigender oder absteigender Reihenfolge mit allen NULL-Einträgen in der letzten Position sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="798a6-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="798a6-137">Der TABLE_SORT_COMBINE-Wert gibt an, dass die in **ulPropTag** angegebene Spalte mit der vorherigen Kategorie-Spalte kombiniert werden soll, um eine zusammengesetzte Kategorie zu bilden.</span><span class="sxs-lookup"><span data-stu-id="798a6-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="798a6-138">Anstatt jedoch auf eindeutigen Werten einzelner Spalten zu kategorisieren, ermöglicht TABLE_SORT_COMBINE die Kategorisierung von eindeutigen Werten einer Kombination von Spalten.</span><span class="sxs-lookup"><span data-stu-id="798a6-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="798a6-139">Beispielsweise kann eine einzelne Kategorie definiert werden, um Nachrichten zu gruppieren, die von einem bestimmten Absender zu einem bestimmten Betreff empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="798a6-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="798a6-140">Wenn Sie den Wert auf TABLE_SORT_COMBINE festlegen, wird die Anzahl der angezeigten Kategorie-Zeilen reduziert.</span><span class="sxs-lookup"><span data-stu-id="798a6-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="798a6-141">Das Sortieren von mehrwertigen Spalten wird von allen Tabellen Implementierungen nicht universell unterstützt.</span><span class="sxs-lookup"><span data-stu-id="798a6-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="798a6-142">Wenn Sie unterstützt werden, wenden Sie das MV_FLAG mithilfe des MVI_PROP-Makros auf das Property-Tag im **ulPropTag** -Element an, um den Sortierschlüssel als mehrwertige Spalte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="798a6-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="798a6-143">Das Sortieren in einer mehrwertigen Spalte basiert auf der Verwendung der einzelnen Werte.</span><span class="sxs-lookup"><span data-stu-id="798a6-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="798a6-144">Die **ulOrder** -Elementwerte TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie Sie mit den folgenden Werten zu Ihrem Code hinzufügen: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="798a6-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="798a6-145">Weitere Informationen zu standardmäßigen und kategorisierten Sortierungen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="798a6-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="798a6-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="798a6-146">See also</span></span>

- [<span data-ttu-id="798a6-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="798a6-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="798a6-148">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="798a6-148">MAPI Structures</span></span>](mapi-structures.md)

