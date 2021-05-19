---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416293"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="16602-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="16602-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="16602-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16602-105">Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, beginnend an der aktuellen Cursorposition.</span><span class="sxs-lookup"><span data-stu-id="16602-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="16602-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="16602-106">Parameters</span></span>

 <span data-ttu-id="16602-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="16602-107">_lRowCount_</span></span>
  
> <span data-ttu-id="16602-108">[in] Maximale Anzahl von Zeilen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="16602-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="16602-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16602-109">_ulFlags_</span></span>
  
> <span data-ttu-id="16602-110">[in] Bitmaske von Flags, die steuern, wie Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="16602-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="16602-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="16602-111">The following flag can be set:</span></span>
    
<span data-ttu-id="16602-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="16602-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="16602-113">Verhindert, dass der Cursor als Ergebnis des Zeilenabrufs fortschreitet.</span><span class="sxs-lookup"><span data-stu-id="16602-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="16602-114">Wenn das TBL_NOADVANCE festgelegt ist, zeigt der Cursor auf die erste zurückgegebene Zeile.</span><span class="sxs-lookup"><span data-stu-id="16602-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="16602-115">Wenn das TBL_NOADVANCE nicht festgelegt ist, zeigt der Cursor auf die Zeile nach der letzten zurückgegebenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="16602-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="16602-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="16602-116">_lppRows_</span></span>
  
> <span data-ttu-id="16602-117">[out] Zeiger auf einen Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die Tabellenzeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="16602-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="16602-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16602-118">Return value</span></span>

<span data-ttu-id="16602-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="16602-119">S_OK</span></span> 
  
> <span data-ttu-id="16602-120">Die Zeilen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="16602-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="16602-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="16602-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="16602-122">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilenabrufvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="16602-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="16602-123">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="16602-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="16602-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="16602-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="16602-125">Der  _Parameter IRowCount_ ist auf Null festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16602-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="16602-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16602-126">Remarks</span></span>

<span data-ttu-id="16602-127">Die **IMAPITable::QueryRows-Methode** ruft eine oder mehrere Datenzeilen aus einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="16602-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="16602-128">Der Wert des  _IRowCount-Parameters_ wirkt sich auf den Ausgangspunkt für den Abruf aus.</span><span class="sxs-lookup"><span data-stu-id="16602-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="16602-129">Wenn  _IRowCount_ positiv ist, werden Zeilen in Vorwärtsrichtung gelesen, beginnend an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="16602-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="16602-130">Wenn  _IRowCount_ negativ ist, **setzt QueryRows** den Ausgangspunkt zurück, indem die angegebene Anzahl von Zeilen rückwärts bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="16602-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="16602-131">Nachdem der Cursor zurückgesetzt wurde, werden Zeilen in der Vorwärtsreihenfolge gelesen.</span><span class="sxs-lookup"><span data-stu-id="16602-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="16602-132">Das **cRows-Element** in der [SRowSet-Struktur,](srowset.md) auf das der  _lppRows-Parameter_ verweist, gibt die Anzahl der zurückgegebenen Zeilen an.</span><span class="sxs-lookup"><span data-stu-id="16602-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="16602-133">Wenn null Zeilen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="16602-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="16602-134">Der Cursor wurde bereits am Anfang der Tabelle positioniert, und der Wert von  _IRowCount ist_ negativ.</span><span class="sxs-lookup"><span data-stu-id="16602-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="16602-135">-Or-</span><span class="sxs-lookup"><span data-stu-id="16602-135">-Or-</span></span> 
    
- <span data-ttu-id="16602-136">Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert von  _IRowCount ist_ positiv.</span><span class="sxs-lookup"><span data-stu-id="16602-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="16602-137">Die Anzahl der Spalten und deren Reihenfolge ist für jede Zeile identisch.</span><span class="sxs-lookup"><span data-stu-id="16602-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="16602-138">Wenn für eine Zeile keine Eigenschaft vorhanden ist oder ein Fehler beim Lesen einer Eigenschaft auftritt, enthält die **SPropValue-Struktur** für die Eigenschaft in der Zeile die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="16602-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="16602-139">PT_ERROR für den Eigenschaftentyp im **ulPropTag-Element.**</span><span class="sxs-lookup"><span data-stu-id="16602-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="16602-140">MAPI_E_NOT_FOUND für das **Value-Element.**</span><span class="sxs-lookup"><span data-stu-id="16602-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="16602-141">Für die [SPropValue-Strukturen](spropvalue.md) im Zeilensatz, auf den der  _lppRows-Parameter_ verweist, verwendeter Arbeitsspeicher muss für jede Zeile separat zugewiesen und frei werden.</span><span class="sxs-lookup"><span data-stu-id="16602-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="16602-142">Verwenden [Sie MAPIFreeBuffer,](mapifreebuffer.md) um die Eigenschaftenwertstrukturen frei zu machen und den Zeilensatz frei zu machen.</span><span class="sxs-lookup"><span data-stu-id="16602-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="16602-143">Wenn ein Aufruf von **QueryRows** jedoch Null zurückgibt und den Anfang oder das Ende der Tabelle angibt, muss nur die **SRowSet-Struktur** selbst frei.</span><span class="sxs-lookup"><span data-stu-id="16602-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="16602-144">Weitere Informationen zum Zuordnen und Freispeichern von Arbeitsspeicher in einer **SRowSet-Struktur** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="16602-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="16602-145">Die zurückgegebenen Zeilen und die Reihenfolge, in der sie zurückgegeben werden, hängen davon ab, ob erfolgreiche Aufrufe an [IMAPITable::Restrict](imapitable-restrict.md) und [IMAPITable::SortTable](imapitable-sorttable.md)ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="16602-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="16602-146">**Beschränken** Sie Zeilen aus der Ansicht, sodass **QueryRows** nur die Zeilen zurück gibt, die den in der Einschränkung angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="16602-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="16602-147">**SortTable** richtet eine standard- oder kategorisierte Sortierreihenfolge ein, die sich auf die Reihenfolge der von QueryRows zurückgegebenen **Zeilen ausdingt.**</span><span class="sxs-lookup"><span data-stu-id="16602-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="16602-148">Die zurückgegebenen Zeilen befinden sich in der in der [SSortOrderSet-Struktur](ssortorderset.md) angegebenen Reihenfolge, die an **SortTable übergeben wird.**</span><span class="sxs-lookup"><span data-stu-id="16602-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="16602-149">Die für jede Zeile zurückgegebenen Spalten und die Reihenfolge, in der sie zurückgegeben werden, hängen davon ab, ob ein erfolgreicher Aufruf an [IMAPITable::SetColumns erfolgt ist.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="16602-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="16602-150">**SetColumns** richtet einen Spaltensatz ein und gibt die Eigenschaften an, die in Spalten in der Tabelle enthalten sein sollen, und die Reihenfolge, in der sie eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="16602-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="16602-151">Wenn ein **SetColumns-Aufruf** ausgeführt wurde, entsprechen die einzelnen Spalten in jeder Zeile und die Reihenfolge dieser Spalten der im Aufruf angegebenen Spaltensatz.</span><span class="sxs-lookup"><span data-stu-id="16602-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="16602-152">Wenn kein **SetColumns-Aufruf** erfolgt ist, gibt die Tabelle den Standardspaltensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="16602-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="16602-153">Wenn keiner dieser Aufrufe ausgeführt wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="16602-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="16602-154">Jede Zeile enthält die Standardspalte, die in der Standardreihenfolge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="16602-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="16602-155">Wenn der spaltensatz, der in einem Aufruf von [IMAPITable::SetColumns](imapitable-setcolumns.md) eingerichtet wurde, Spalten enthält, die auf PR_NULL festgelegt sind, enthält das [SPropValue-Array](spropvalue.md) innerhalb des in  _lppRows_ zurückgegebenen Zeilensatz leere Slots.</span><span class="sxs-lookup"><span data-stu-id="16602-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="16602-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="16602-156">Notes to implementers</span></span>

<span data-ttu-id="16602-157">Sie können zulassen, dass ein Aufrufer eine nicht unterstützte Spalte in den Spaltensatz einrist.</span><span class="sxs-lookup"><span data-stu-id="16602-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="16602-158">Platzieren Sie in diesem Fall PT_ERROR im Eigenschaftentypteil des Eigenschaftstags und MAPI_E_NOT_FOUND eigenschaftswert für die nicht unterstützte Spalte.</span><span class="sxs-lookup"><span data-stu-id="16602-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="16602-159">Behandeln Sie die Zeilenanzahl als Anforderung und nicht als Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16602-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="16602-160">Sie können eine beliebige Stelle von Nullzeilen zurückgeben, wenn keine Zeilen in Der Richtung der Abfrage vorhanden sind, zur angeforderten Nummer.</span><span class="sxs-lookup"><span data-stu-id="16602-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="16602-161">Gibt nur die Zeilen zurück, die dem Benutzer angezeigt werden, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden, sodass der Aufrufer gültige Annahmen über den Umfang der Daten treffen und zusätzliche Arbeit vermeiden kann.</span><span class="sxs-lookup"><span data-stu-id="16602-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="16602-162">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="16602-162">Notes to callers</span></span>

<span data-ttu-id="16602-163">In der Regel erhalten Sie so viele Zeilen wie im _lRowCount-Parameter angegeben._</span><span class="sxs-lookup"><span data-stu-id="16602-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="16602-164">Wenn speicher- oder implementierungsbeschränkungen jedoch ein Problem sind oder wenn der Vorgang den Anfang oder das Ende der Tabelle vorzeitig erreicht, gibt **QueryRows** weniger Zeilen zurück als angefordert.</span><span class="sxs-lookup"><span data-stu-id="16602-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="16602-165">Wenn **QueryRows** MAPI_E_BUSY zurückgibt, rufen Sie die [IMAPITable::WaitForCompletion-Methode](imapitable-waitforcompletion.md) auf, und wiederholen Sie den Aufruf von **QueryRows,** wenn der asynchrone Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="16602-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="16602-166">Beachten Sie beim Aufrufen von **QueryRows,** dass das Timing asynchroner Benachrichtigungen dazu führen kann, dass der Zeilensatz, den Sie von **QueryRows** erhalten, die zugrunde liegenden Daten nicht genau repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="16602-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="16602-167">Beispielsweise wird durch einen Aufruf von **QueryRows** an die Inhaltstabelle eines Ordners nach dem Löschen einer Nachricht, aber vor dem Eingang der entsprechenden Benachrichtigung die gelöschte Zeile im Zeilensatz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="16602-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="16602-168">Warten Sie immer, bis eine Benachrichtigung eintrifft, bevor Sie die Ansicht der Daten des Benutzers aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="16602-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="16602-169">Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="16602-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="16602-170">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="16602-170">MFCMAPI reference</span></span>

<span data-ttu-id="16602-171">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="16602-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="16602-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="16602-172">**File**</span></span>|<span data-ttu-id="16602-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="16602-173">**Function**</span></span>|<span data-ttu-id="16602-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="16602-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16602-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="16602-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="16602-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="16602-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="16602-177">MFCMAPI verwendet die **IMAPITable::QueryRows-Methode,** um Zeilen in der Tabelle abzurufen, die in die Ansicht geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="16602-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16602-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16602-178">See also</span></span>



[<span data-ttu-id="16602-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="16602-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="16602-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="16602-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="16602-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="16602-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="16602-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="16602-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="16602-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="16602-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="16602-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="16602-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="16602-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="16602-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="16602-186">SRow</span><span class="sxs-lookup"><span data-stu-id="16602-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="16602-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="16602-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="16602-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16602-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="16602-189">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="16602-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

