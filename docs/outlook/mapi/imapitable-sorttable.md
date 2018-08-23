---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: efeff92f1a21d076c1ee58b82ad3ab25797df014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592304"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="1e10b-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="1e10b-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="1e10b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e10b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e10b-105">Die **SortTable** -Methode ordnet die Zeilen der Tabelle ist, je nach sortieren Kriterien.</span><span class="sxs-lookup"><span data-stu-id="1e10b-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1e10b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e10b-106">Parameters</span></span>

<span data-ttu-id="1e10b-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="1e10b-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="1e10b-108">[in] Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierkriterien anzuwendende enthält.</span><span class="sxs-lookup"><span data-stu-id="1e10b-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="1e10b-109">Übergeben eine **SSortOrderSet** -Struktur, die keine Spalten enthält, gibt an, dass die Tabelle nicht vorhanden ist, in einer bestimmten Reihenfolge sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1e10b-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="1e10b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e10b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1e10b-111">[in] Bitmaske aus Flags, die den Zeitpunkt des Vorgangs **SortTable** steuert.</span><span class="sxs-lookup"><span data-stu-id="1e10b-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="1e10b-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1e10b-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="1e10b-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="1e10b-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="1e10b-114">Die Operation asynchron startet und zurückgibt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1e10b-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="1e10b-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="1e10b-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="1e10b-116">Nach Abschluss der Sortierung verzögert, bis die Daten in der Tabelle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1e10b-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e10b-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1e10b-117">Return value</span></span>

<span data-ttu-id="1e10b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e10b-118">S_OK</span></span> 
  
> <span data-ttu-id="1e10b-119">Der Sortiervorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1e10b-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="1e10b-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1e10b-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1e10b-121">Ein anderer Vorgang wird ausgeführt, die den Sortiervorgang Neustart verhindert.</span><span class="sxs-lookup"><span data-stu-id="1e10b-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="1e10b-122">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="1e10b-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="1e10b-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1e10b-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1e10b-124">Die Tabelle unterstützt nicht den Typ der Sortierung angefordert.</span><span class="sxs-lookup"><span data-stu-id="1e10b-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="1e10b-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="1e10b-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="1e10b-126">Die Tabelle kann nicht den Vorgang ausgeführt werden, da die bestimmten Sortierkriterien auf das durch den Parameter _LpSortCriteria_ ist zu komplex.</span><span class="sxs-lookup"><span data-stu-id="1e10b-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="1e10b-127">**SortTable** kann unter den folgenden Umständen MAPI_E_TOO_COMPLEX zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e10b-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="1e10b-128">Ein Sortiervorgang ist für eine Spalte angefordert, dass die Implementierung sortieren kann.</span><span class="sxs-lookup"><span data-stu-id="1e10b-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="1e10b-129">Die Implementierung unterstützt nicht die Sortierreihenfolge im **UlOrder** Member der Struktur **SSortOrderSet** angefordert.</span><span class="sxs-lookup"><span data-stu-id="1e10b-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="1e10b-130">Die Anzahl der Spalten sortiert werden, wie in den **cSorts** Member in **SSortOrderSet**angegeben, ist größer als die Implementierung verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e10b-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="1e10b-131">Ein Sortiervorgang angefordert, gekennzeichnet durch ein Tag-Eigenschaft in **SSortOrderSet**, basierend auf einer Eigenschaft, die nicht in der Sammlung verfügbar oder aktiv ist und die Implementierung unterstützt nicht das Sortieren nach Eigenschaften nicht in der verfügbare Satz.</span><span class="sxs-lookup"><span data-stu-id="1e10b-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="1e10b-132">Eine Eigenschaft angegeben ist mehrmals in einer Reihenfolge sortiert, wie mehrere Instanzen des gleichen Eigenschaftstags angegeben, und die Implementierung dieser einen Sortiervorgang kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e10b-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="1e10b-133">Ein mehrwertige Eigenschaftenspalten Grundlage Sortiervorgang ist mit MVI_FLAG angefordert und die Implementierung die Sortierung auf mehrwertige Eigenschaften nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e10b-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="1e10b-134">Ein Eigenschaftentag für eine Eigenschaft im **SSortOrderSet** gibt eine Eigenschaft oder Typ, der die Implementierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e10b-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="1e10b-135">Ein Sortiervorgang, die durch die Tabelle aus der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft vorwärts wird fortgesetzt wird nur für eine Anlagentabelle angegeben, die diese Art der Sortierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e10b-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e10b-136">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1e10b-136">Remarks</span></span>

<span data-ttu-id="1e10b-137">Die **SortTable** -Methode ordnet die Zeilen in einer Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="1e10b-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="1e10b-138">Während einige Tabellen Standard- und kategorisierten auf verschiedenen Sortierschlüsselspalten Sortierung unterstützt wird, sind die Unterstützung mehr anderen Tabellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1e10b-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="1e10b-139">Von adressbuchanbietern implementierte unterstützt normalerweise nicht Sortierung.</span><span class="sxs-lookup"><span data-stu-id="1e10b-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="1e10b-140">Nachricht Anbieter unterstützen normalerweise sortieren, wenn sie aufzubewahren, der die Sortierreihenfolge der Ordner, die entsteht, wenn eine vollständige Tabelle (einer Tabelle ohne Einschränkungen) sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="1e10b-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="1e10b-141">Einige Tabellen zulassen Sortierung auf keiner Tabellenspalte erfolgen.</span><span class="sxs-lookup"><span data-stu-id="1e10b-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="1e10b-142">Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind durch einen Aufruf der **SortTable** nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="1e10b-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="1e10b-143">Einige Tabellen erfordern, dass Sortierschlüsseln nur mit Spalten in der Tabelle aktuellen Spalte Gruppe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1e10b-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="1e10b-144">Eine Tabelle kann entweder MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX aus **SortTable** zurückgeben, wenn einen Sortiervorgang abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e10b-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="1e10b-145">Darüber hinaus sind Anbieter nicht unbedingt berücksichtigt die Sortierreihenfolge für Hierarchietabellen angegebenen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e10b-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="1e10b-146">Wenn keine Spalten in der [SSortOrderSet](ssortorderset.md) -Struktur, die auf das durch den Parameter _LpSortCriteria_ vorhanden sind, wird die Tabelle die aktuellen Spalte Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e10b-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="1e10b-147">Die aktuelle Sortierreihenfolge kann durch Aufrufen der Tabelle [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1e10b-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="1e10b-148">Alle Lesezeichen für eine Tabelle ungültig sind, und bei **SortTable** wird aufgerufen, und die BOOKMARK_CURRENT Textmarke, die angibt, die aktuellen Cursorposition festgelegt werden sollte, an den Anfang der Tabelle gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e10b-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="1e10b-149">Wenn Sie auf eine Spalte, die eine mehrwertige Eigenschaft, ohne die MVI_FLAG-Flag enthält sortieren, werden die Werte der Spalte als vollständig geordnete Tupel behandelt.</span><span class="sxs-lookup"><span data-stu-id="1e10b-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="1e10b-150">Ein Vergleich von zwei Spalten mit mehreren Werten vergleicht die Spalte Elemente in der Reihenfolge, die Beziehung der Spalten auf der ersten Ungleichheit, reporting und Gleichheit nur zurückgegeben, wenn die zu vergleichenden Spalten dieselben Werte wie in der gleichen Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e10b-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="1e10b-151">Wenn eine Spalte weniger Werte als die andere verfügt, kann die gemeldete Beziehung, die über einen null-Wert auf den anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="1e10b-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1e10b-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1e10b-152">Notes to callers</span></span>

<span data-ttu-id="1e10b-153">**SortTable** arbeitet synchron, es sei denn, Sie eines der Flags festlegen.</span><span class="sxs-lookup"><span data-stu-id="1e10b-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="1e10b-154">Wenn Sie das TBL_BATCH-Flag festlegen, verschiebt **SortTable** Sortiervorgang, es sei denn, Sie die Daten anfordern.</span><span class="sxs-lookup"><span data-stu-id="1e10b-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="1e10b-155">Wenn das Flag TBL_ASYNC festgelegt ist, arbeitet **SortTable** asynchron potenziell vor dem Abschluss des Vorgangs zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e10b-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="1e10b-156">Rufen Sie die [IMAPITable::Abort](imapitable-abort.md) -Methode, um einer asynchronen Operation in Bearbeitung beenden, wenn die Sortierung sofort ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="1e10b-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="1e10b-157">Wenn **SortTable** fortgesetzt werden kann, da eine oder mehrere asynchrone Vorgänge in der Tabelle ausgeführt werden, wird MAPI_E_BUSY zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e10b-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="1e10b-158">Rufen Sie für eine optimale Leistung **SetColumns** zum Anpassen der Tabelle Spalte festlegen und **Restrict** zur Begrenzung der Anzahl der Zeilen in der Tabelle vor dem Aufrufen der **SortTable** , um die Sortierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="1e10b-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="1e10b-159">Bei jedem **SortTable** ein Fehler auftritt, wird die Sortierreihenfolge, die vor dem Ausfall gültig war noch wirksam.</span><span class="sxs-lookup"><span data-stu-id="1e10b-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e10b-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e10b-160">See also</span></span>

- [<span data-ttu-id="1e10b-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="1e10b-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="1e10b-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="1e10b-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="1e10b-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1e10b-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="1e10b-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="1e10b-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="1e10b-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1e10b-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="1e10b-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="1e10b-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="1e10b-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e10b-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

