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
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328854"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="17342-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="17342-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="17342-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17342-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17342-105">Die **IMAPITable:: sortable** -Methode sortiert die Zeilen der Tabelle, je nach Sortierkriterien.</span><span class="sxs-lookup"><span data-stu-id="17342-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="17342-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17342-106">Parameters</span></span>

<span data-ttu-id="17342-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="17342-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="17342-108">in Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die anzuwendenden Sortierkriterien enthält.</span><span class="sxs-lookup"><span data-stu-id="17342-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="17342-109">Durch das Übergeben einer **SSortOrderSet** -Struktur mit NULL-Spalten wird angegeben, dass die Tabelle nicht in einer bestimmten Reihenfolge sortiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="17342-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="17342-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="17342-110">_ulFlags_</span></span>
  
> <span data-ttu-id="17342-111">in Bitmaske von Flags, die das Timing des **IMAPITable:: sortable** -Vorgangs steuert.</span><span class="sxs-lookup"><span data-stu-id="17342-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="17342-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="17342-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="17342-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="17342-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="17342-114">Startet den Vorgang asynchron und wird zurückgegeben, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="17342-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="17342-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="17342-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="17342-116">Verschiebt den Abschluss des Sortiervorgangs, bis die Daten in der Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="17342-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17342-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17342-117">Return value</span></span>

<span data-ttu-id="17342-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="17342-118">S_OK</span></span> 
  
> <span data-ttu-id="17342-119">Der Sortiervorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="17342-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="17342-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="17342-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="17342-121">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortiervorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="17342-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="17342-122">Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="17342-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="17342-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="17342-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="17342-124">Die Tabelle unterstützt den angeforderten Sortiertyp nicht.</span><span class="sxs-lookup"><span data-stu-id="17342-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="17342-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="17342-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="17342-126">Die Tabelle kann den Vorgang nicht ausführen, da die bestimmten Sortierkriterien, auf die durch den _lpSortCriteria_ -Parameter verwiesen wird, zu komplex sind.</span><span class="sxs-lookup"><span data-stu-id="17342-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="17342-127">**Sortable** kann MAPI_E_TOO_COMPLEX unter den folgenden Bedingungen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="17342-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="17342-128">Ein Sortiervorgang wird für eine Eigenschaftsspalte angefordert, die von der Implementierung nicht sortiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="17342-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="17342-129">Die Implementierung unterstützt nicht die im **ulOrder** -Element der **SSortOrderSet** -Struktur angeforderte Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="17342-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="17342-130">Die Anzahl der zu sortierenden Spalten, wie im **cSorts** -Element in **SSortOrderSet**angegeben, ist größer als die Implementierung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="17342-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="17342-131">Ein Sortiervorgang wird, wie durch ein Property-Tag in **SSortOrderSet**angegeben, angefordert, basierend auf einer Eigenschaft, die sich nicht im verfügbaren oder aktiven Satz befindet, und die Implementierung unterstützt das Sortieren von Eigenschaften nicht im verfügbaren Satz.</span><span class="sxs-lookup"><span data-stu-id="17342-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="17342-132">Eine Eigenschaft wird mehrmals in einem Sortier Reihenfolge-Satz angegeben, wie durch mehrere Instanzen desselben Property-Tags angegeben, und die Implementierung kann keinen solchen Sortiervorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="17342-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="17342-133">Ein Sortiervorgang basierend auf mehrwertigen Eigenschaftsspalten wird mithilfe von MVI_FLAG angefordert, und die Implementierung unterstützt das Sortieren von mehrwertigen Eigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="17342-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="17342-134">Ein Property-Tag für eine Eigenschaft in **SSortOrderSet** gibt eine Eigenschaft oder einen Typ an, die von der Implementierung nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="17342-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="17342-135">Ein anderer Sortiervorgang als einer, der die Tabelle aus der **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft Forward durchläuft, wird nur für eine Anlagentabelle angegeben, die diesen Sortiertyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17342-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17342-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17342-136">Remarks</span></span>

<span data-ttu-id="17342-137">Die **IMAPITable:: sortable** -Methode ordnet die Zeilen in einer Tabellenansicht an.</span><span class="sxs-lookup"><span data-stu-id="17342-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="17342-138">Während einige Tabellen sowohl die standardmäßige als auch die kategorisierte Sortierung in verschiedenen Sortierschlüsselspalten unterstützen, sind andere Tabellen in ihrer Unterstützung eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="17342-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="17342-139">Adressbuchanbieter unterstützen die Tabellensortierung normalerweise nicht.</span><span class="sxs-lookup"><span data-stu-id="17342-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="17342-140">Nachrichtenspeicher Anbieter unterstützen die Sortierung in der Regel so weit, dass Sie die Sortierreihenfolge von Ordnern beibehalten, die beim Sortieren einer vollständigen Tabelle (eine Tabelle ohne Einschränkungen) auftreten.</span><span class="sxs-lookup"><span data-stu-id="17342-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="17342-141">In einigen Tabellen kann die Sortierung für eine beliebige Tabellenspalte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="17342-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="17342-142">Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind, werden \*\*\*\* von einem sortable-Aufruf nicht beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="17342-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="17342-143">Einige Tabellen erfordern, dass Sortierschlüssel nur mit Spalten im aktuellen Spaltensatz der Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="17342-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="17342-144">Eine Tabelle kann MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX aus der **sortable** zurückgeben, wenn ein Sortiervorgang nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="17342-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="17342-145">Darüber hinaus werden Speicheranbieter nicht unbedingt für die für Hierarchietabellen angegebenen Sortierreihenfolgen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="17342-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="17342-146">Wenn in der [SSortOrderSet](ssortorderset.md) -Struktur NULL-Spalten vorhanden sind, auf die durch den _lpSortCriteria_ -Parameter verwiesen wird, gibt die Tabelle den aktuellen Spaltensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="17342-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="17342-147">Die aktuelle Sortierreihenfolge kann abgerufen werden, indem die [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode der Tabelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="17342-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="17342-148">Alle Lesezeichen für eine Tabelle sind ungültig und sollten gelöscht werden, wenn ein \*\*\*\* Aufruf der sortable-Funktion erfolgt, und das BOOKMARK_CURRENT-Lesezeichen, das die aktuelle Cursorposition angibt, sollte auf den Anfang der Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="17342-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="17342-149">Wenn Sie nach einer Spalte sortieren, die eine mehrwertige Eigenschaft ohne das MVI_FLAG-Flagsatz enthält, werden die Werte der Spalte als vollständig geordnetes Tupel behandelt.</span><span class="sxs-lookup"><span data-stu-id="17342-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="17342-150">Ein Vergleich zwischen zwei mehrwertigen Spalten vergleicht die Spaltenelemente in der Reihenfolge, gibt die Relation der Spalten bei der ersten Ungleichheit zurück und gibt die Gleichheit nur, wenn die verglichenen Spalten die gleichen Werte in der gleichen Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="17342-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="17342-151">Wenn eine Spalte weniger Werte als die andere hat, ist die berichtete Relation die eines NULL-Werts für den anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="17342-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="17342-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="17342-152">Notes to callers</span></span>

<span data-ttu-id="17342-153">Die **Sortier** Tabellenfunktion funktioniert synchron, es sei denn, Sie legen eine der Flags fest.</span><span class="sxs-lookup"><span data-stu-id="17342-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="17342-154">Wenn Sie das TBL_BATCH-Flag festlegen \*\*\*\* , verschiebt sortable den Sortiervorgang, es sei denn, Sie fordern die Daten an.</span><span class="sxs-lookup"><span data-stu-id="17342-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="17342-155">Wenn das TBL_ASYNC-Flag festgelegt \*\*\*\* ist, wird die sortable-Operation asynchron ausgeführt, und möglicherweise vor dem Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17342-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="17342-156">Rufen Sie die [IMAPITable:: Abort](imapitable-abort.md) -Methode auf, um einen asynchronen Vorgang zu beenden, der ausgeführt wird, wenn Ihre Sortierung sofort ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="17342-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="17342-157">Wenn \*\*\*\* die sortable-Funktion nicht fortgesetzt werden kann, da mindestens ein asynchroner Vorgang in der Tabelle ausgeführt wird, wird MAPI_E_BUSY zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17342-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="17342-158">Um eine optimale Leistung zu \*\*\*\* erzielen, rufen Sie SetColumns auf, um den Spaltensatz der Tabelle anzupassen und die Anzahl der Zeilen in der Tabelle einzuschränken, bevor Sie **sortable** aufrufen, um die Sortierung auszuführen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="17342-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="17342-159">Bei jeder fehlerhaften **Sortier** Funktion wird die Sortierreihenfolge, die vor dem Fehler wirksam war, weiterhin wirksam.</span><span class="sxs-lookup"><span data-stu-id="17342-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17342-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17342-160">See also</span></span>

- [<span data-ttu-id="17342-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="17342-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="17342-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="17342-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="17342-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="17342-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="17342-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="17342-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="17342-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="17342-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="17342-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="17342-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="17342-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17342-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

