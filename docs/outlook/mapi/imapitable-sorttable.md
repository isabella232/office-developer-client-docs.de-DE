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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432366"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="a581a-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a581a-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="a581a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a581a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a581a-105">Die **IMAPITable::SortTable-Methode** sortiert die Zeilen der Tabelle in Abhängigkeit von Sortierkriterien.</span><span class="sxs-lookup"><span data-stu-id="a581a-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a581a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a581a-106">Parameters</span></span>

<span data-ttu-id="a581a-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="a581a-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="a581a-108">[in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die anzuwendende Sortierkriterien enthält.</span><span class="sxs-lookup"><span data-stu-id="a581a-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="a581a-109">Das Übergeben einer **SSortOrderSet-Struktur,** die null Spalten enthält, bedeutet, dass die Tabelle nicht in einer bestimmten Reihenfolge sortiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a581a-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="a581a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a581a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a581a-111">[in] Bitmaske von Flags, die das Timing des **IMAPITable::SortTable-Vorgangs** steuert.</span><span class="sxs-lookup"><span data-stu-id="a581a-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="a581a-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a581a-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="a581a-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="a581a-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="a581a-114">Startet den Vorgang asynchron und gibt zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a581a-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="a581a-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="a581a-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="a581a-116">Der Abschluss der Sortierung wird so lange auf die Daten in der Tabelle verf?en.</span><span class="sxs-lookup"><span data-stu-id="a581a-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a581a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a581a-117">Return value</span></span>

<span data-ttu-id="a581a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a581a-118">S_OK</span></span> 
  
> <span data-ttu-id="a581a-119">Der Sortiervorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a581a-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="a581a-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a581a-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a581a-121">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortiervorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a581a-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="a581a-122">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="a581a-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a581a-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a581a-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a581a-124">Die Tabelle unterstützt den angeforderten Sortiertyp nicht.</span><span class="sxs-lookup"><span data-stu-id="a581a-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="a581a-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="a581a-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="a581a-126">Die Tabelle kann den Vorgang nicht ausführen, da die bestimmten Sortierkriterien, auf die der  _lpSortCriteria-Parameter_ verweist, zu komplex sind.</span><span class="sxs-lookup"><span data-stu-id="a581a-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="a581a-127">**SortTable** kann MAPI_E_TOO_COMPLEX unter den folgenden Bedingungen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a581a-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="a581a-128">Für eine Eigenschaftenspalte, die von der Implementierung nicht sortiert werden kann, wird ein Sortiervorgang angefordert.</span><span class="sxs-lookup"><span data-stu-id="a581a-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="a581a-129">Die Implementierung unterstützt die im **ulOrder-Element** der **SSortOrderSet-Struktur** angeforderte Sortierreihenfolge nicht.</span><span class="sxs-lookup"><span data-stu-id="a581a-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="a581a-130">Die Anzahl der spalten, die sortiert werden sollen, wie im **cSorts-Element** in **SSortOrderSet** angegeben, ist größer, als die Implementierung verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="a581a-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="a581a-131">Ein Sortiervorgang wird angefordert, wie durch ein Eigenschaftentag in **SSortOrderSet** angegeben, basierend auf einer Eigenschaft, die sich nicht im verfügbaren oder aktiven Satz befindet, und die Implementierung unterstützt das Sortieren von Eigenschaften, die nicht im verfügbaren Satz enthalten sind, nicht.</span><span class="sxs-lookup"><span data-stu-id="a581a-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="a581a-132">Eine Eigenschaft wird in einem Sortierreihenfolgensatz mehrmals angegeben, wie von mehreren Instanzen desselben Eigenschaftstags angegeben, und die Implementierung kann einen solchen Sortiervorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="a581a-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="a581a-133">Ein Sortiervorgang basierend auf mehrwertigen Eigenschaftenspalten wird mithilfe von MVI_FLAG angefordert, und die Implementierung unterstützt die Sortierung nach mehrwertigen Eigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="a581a-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="a581a-134">Ein Eigenschaftstag für eine Eigenschaft in **SSortOrderSet** gibt eine Eigenschaft oder einen Typ an, die von der Implementierung nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a581a-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="a581a-135">Ein anderer Sortiervorgang, der die Tabelle von der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft vorwärts durchgeht, wird nur für eine Anlagentabelle angegeben, die diese Art von Sortierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a581a-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a581a-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a581a-136">Remarks</span></span>

<span data-ttu-id="a581a-137">Die **IMAPITable::SortTable-Methode** ordnet die Zeilen in einer Tabellenansicht an.</span><span class="sxs-lookup"><span data-stu-id="a581a-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="a581a-138">Während einige Tabellen sowohl die standard- als auch die kategorisierte Sortierung für verschiedene Sortierschlüsselspalten unterstützen, sind andere Tabellen in ihrer Unterstützung eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="a581a-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="a581a-139">Adressbuchanbieter unterstützen normalerweise keine Tabellensortierung.</span><span class="sxs-lookup"><span data-stu-id="a581a-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="a581a-140">Nachrichtenspeicheranbieter unterstützen die Sortierung in der Regel so weit, dass sie die Sortierreihenfolge von Ordnern behalten, die sich ergibt, wenn eine vollständige Tabelle (eine Tabelle ohne Einschränkungen) sortiert wird.</span><span class="sxs-lookup"><span data-stu-id="a581a-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="a581a-141">In einigen Tabellen kann die Sortierung in jeder Tabellenspalte durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a581a-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="a581a-142">Andere Tabellen nicht; Spalten, die nicht in der Tabellenansicht enthalten sind, sind von einem **SortTable-Aufruf nicht** betroffen.</span><span class="sxs-lookup"><span data-stu-id="a581a-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="a581a-143">Einige Tabellen erfordern, dass Sortierschlüssel nur mit Spalten im aktuellen Spaltensatz der Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a581a-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="a581a-144">Eine Tabelle kann entweder MAPI_E_NO_SUPPORT oder MAPI_E_TOO_COMPLEX **SortTable** zurückgeben, wenn sie keinen Sortiervorgang abschließen kann.</span><span class="sxs-lookup"><span data-stu-id="a581a-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="a581a-145">Darüber hinaus ist es nicht garantiert, dass Speicheranbieter den für Hierarchietabellen angegebenen Sortierreihenfolgensatz würdigen.</span><span class="sxs-lookup"><span data-stu-id="a581a-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="a581a-146">Wenn die [SSortOrderSet-Struktur](ssortorderset.md) null Spalten enthält, auf die der  _lpSortCriteria-Parameter_ verweist, gibt die Tabelle den aktuellen Spaltensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="a581a-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="a581a-147">Die aktuelle Sortierreihenfolge kann durch Aufrufen der [IMAPITable::QuerySortOrder-Methode der Tabelle abgerufen](imapitable-querysortorder.md) werden.</span><span class="sxs-lookup"><span data-stu-id="a581a-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="a581a-148">Alle Lesezeichen für eine Tabelle sind ungültig und sollten gelöscht werden, wenn ein Aufruf von **SortTable** erfolgt, und die BOOKMARK_CURRENT-Textmarke, die die aktuelle Cursorposition angibt, sollte auf den Anfang der Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a581a-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="a581a-149">Wenn Sie nach einer Spalte sortieren, die eine mehrwertige Eigenschaft ohne das flag set MVI_FLAG enthält, werden die Werte der Spalte als vollständig sortiertes Tupel behandelt.</span><span class="sxs-lookup"><span data-stu-id="a581a-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="a581a-150">Bei einem Vergleich von zwei mehrwertigen Spalten werden die Spaltenelemente in der Reihenfolge verglichen. Dabei wird das Verhältnis der Spalten bei der ersten Ungleichheit angegeben, und es wird nur Gleichheit zurückgegeben, wenn die zu vergleichenden Spalten dieselben Werte in derselben Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="a581a-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="a581a-151">Wenn eine Spalte weniger Werte als die andere hat, ist die gemeldete Beziehung die eines Nullwerts zum anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="a581a-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a581a-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a581a-152">Notes to callers</span></span>

<span data-ttu-id="a581a-153">**SortTable** funktioniert synchron, es sei denn, Sie legen eines der Flags ein.</span><span class="sxs-lookup"><span data-stu-id="a581a-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="a581a-154">Wenn Sie das TBL_BATCH festlegen, verschiebt **SortTable** den Sortiervorgang, es sei denn, Sie fordern die Daten an.</span><span class="sxs-lookup"><span data-stu-id="a581a-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="a581a-155">Wenn das TBL_ASYNC festgelegt ist, wird **SortTable** asynchron betrieben und möglicherweise vor Abschluss des Vorgangs zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a581a-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="a581a-156">Rufen Sie [die IMAPITable::Abort-Methode](imapitable-abort.md) auf, um einen asynchronen Vorgang zu beenden, wenn die Sortierung sofort durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a581a-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="a581a-157">Wenn **SortTable** nicht fortgesetzt werden kann, da mindestens ein asynchroner Vorgang in der Tabelle ausgeführt wird, wird MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="a581a-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="a581a-158">Um eine optimale Leistung zu erzielen, rufen Sie **SetColumns** auf, um den Spaltensatz der Tabelle anzupassen, und **beschränken** Sie, um die Anzahl der Zeilen in der Tabelle zu beschränken, bevor Sie **SortTable** aufrufen, um die Sortierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a581a-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="a581a-159">Wenn **SortTable** fehlschlägt, ist die Sortierreihenfolge, die vor dem Fehler wirksam war, weiterhin wirksam.</span><span class="sxs-lookup"><span data-stu-id="a581a-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a581a-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a581a-160">See also</span></span>

- [<span data-ttu-id="a581a-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="a581a-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="a581a-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="a581a-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="a581a-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a581a-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="a581a-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a581a-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="a581a-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a581a-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="a581a-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a581a-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="a581a-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a581a-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

