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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792488"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="6790c-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="6790c-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="6790c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6790c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6790c-105">Gibt eine oder mehrere Zeilen aus einer Tabelle, beginnend bei der aktuellen Cursorposition zurück.</span><span class="sxs-lookup"><span data-stu-id="6790c-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="6790c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6790c-106">Parameters</span></span>

 <span data-ttu-id="6790c-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="6790c-107">_lRowCount_</span></span>
  
> <span data-ttu-id="6790c-108">[in] Maximale Anzahl der Zeilen, die zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6790c-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="6790c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6790c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6790c-110">[in] Bitmaske der Flags, die steuern, wie Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6790c-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="6790c-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6790c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="6790c-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="6790c-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="6790c-113">Verhindert, dass den Cursor als Ergebnis des Zeile Abrufs vorwärts verschoben.</span><span class="sxs-lookup"><span data-stu-id="6790c-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="6790c-114">Wenn das Flag TBL_NOADVANCE festgelegt ist, zurückgegeben, die der Cursor verweist auf die erste Zeile.</span><span class="sxs-lookup"><span data-stu-id="6790c-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="6790c-115">Wenn das Flag TBL_NOADVANCE nicht festgelegt ist, zeigt der Cursor auf die Zeile nach der letzten Zeile zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6790c-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="6790c-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="6790c-116">_lppRows_</span></span>
  
> <span data-ttu-id="6790c-117">[out] Zeiger auf einen Zeiger auf eine [SRowSet](srowset.md) -Struktur, die die Tabellenzeilen.</span><span class="sxs-lookup"><span data-stu-id="6790c-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6790c-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6790c-118">Return value</span></span>

<span data-ttu-id="6790c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6790c-119">S_OK</span></span> 
  
> <span data-ttu-id="6790c-120">Die Zeilen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6790c-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="6790c-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="6790c-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="6790c-122">Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang Zeile nicht gestartet dass.</span><span class="sxs-lookup"><span data-stu-id="6790c-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="6790c-123">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="6790c-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="6790c-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6790c-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="6790c-125">Der Parameter _IRowCount_ wird auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6790c-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6790c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6790c-126">Remarks</span></span>

<span data-ttu-id="6790c-127">**Die QueryRows** Ruft eine oder mehrere Zeilen mit Daten aus einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="6790c-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="6790c-128">Der Wert des Parameters _IRowCount_ wirkt sich auf der Ausgangspunkt für das Abrufen.</span><span class="sxs-lookup"><span data-stu-id="6790c-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="6790c-129">_IRowCount_ positiv darf, werden vorwärts, ab der aktuellen Position Zeilen gelesen.</span><span class="sxs-lookup"><span data-stu-id="6790c-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="6790c-130">Wenn _IRowCount_ negativ ist, setzt **QueryRows** Startpunkt durch Verschieben rückwärts die angegebene Anzahl von Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="6790c-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="6790c-131">Nach dem Zurücksetzen von des Cursors werden die Zeilen in der Reihenfolge gelesen.</span><span class="sxs-lookup"><span data-stu-id="6790c-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="6790c-132">Der **cRows** Member in der [SRowSet](srowset.md) -Struktur, die auf das durch den Parameter _LppRows_ gibt die Anzahl von Zeilen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6790c-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="6790c-133">Wenn keine Zeilen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6790c-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="6790c-134">Der Cursor wurde bereits am Anfang der Tabelle positioniert, und der Wert der _IRowCount_ negativ ist.</span><span class="sxs-lookup"><span data-stu-id="6790c-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="6790c-135">\Endash oder \endash</span><span class="sxs-lookup"><span data-stu-id="6790c-135">-Or-</span></span> 
    
- <span data-ttu-id="6790c-136">Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert der _IRowCount_ positiv ist.</span><span class="sxs-lookup"><span data-stu-id="6790c-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="6790c-137">Die Anzahl der Spalten und ihrer Reihenfolge wird für jede Zeile identisch.</span><span class="sxs-lookup"><span data-stu-id="6790c-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="6790c-138">Wenn eine Eigenschaft für eine Zeile nicht vorhanden, oder es wird ein Fehler beim Lesen einer Eigenschaft, enthält die **SPropValue** -Struktur für die Eigenschaft in der Zeile die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="6790c-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="6790c-139">PT_ERROR für den Eigenschaftentyp im **UlPropTag** -Member.</span><span class="sxs-lookup"><span data-stu-id="6790c-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="6790c-140">MAPI_E_NOT_FOUND für **das Element** .</span><span class="sxs-lookup"><span data-stu-id="6790c-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="6790c-141">Für die [SPropValue](spropvalue.md) Strukturen in der Zeile auf das durch den Parameter _LppRows_ verwendeter Arbeitsspeicher muss separat belegt und für jede Zeile freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6790c-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="6790c-142">Verwenden Sie [MAPIFreeBuffer](mapifreebuffer.md) , um die Eigenschaft Wert Strukturen frei, und legen Sie die Zeile frei, um.</span><span class="sxs-lookup"><span data-stu-id="6790c-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="6790c-143">Wenn Sie ein Anruf an **QueryRows** gibt 0 (null) zurück, jedoch muss, der angibt, der Anfang oder das Ende der Tabelle nur die **SRowSet** Struktur selbst freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6790c-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="6790c-144">Weitere Informationen zum Zuordnen und Freigeben von Arbeitsspeicher in eine **SRowSet** -Struktur finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="6790c-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="6790c-145">Die Zeilen, die zurückgegeben werden und die Reihenfolge, in der sie zurückgegeben werden, hängt davon ab, unabhängig davon, ob erfolgreiche Anrufe an die [Methode IMAPITable:: Restrict](imapitable-restrict.md) und [SortTable](imapitable-sorttable.md)vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="6790c-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="6790c-146">**Restrict** Filter Zeilen aus der Ansicht verursacht **QueryRows** , um nur die Zeilen zurück, die in der Einschränkung angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6790c-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="6790c-147">**SortTable** richtet einen Standard oder kategorisiert Sortierreihenfolge, beeinflussen die Abfolge von Zeilen von **QueryRows**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6790c-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="6790c-148">Die zurückgegebenen Zeilen werden in der Reihenfolge, in der **SortTable**übergeben [SSortOrderSet](ssortorderset.md) Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="6790c-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="6790c-149">Die Spalten für jede Zeile zurückgegeben und hängen von der Reihenfolge, in dem sie zurückgegeben werden, unabhängig davon, ob ein erfolgreicher Aufruf an [IMAPITable::SetColumns](imapitable-setcolumns.md)vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6790c-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="6790c-150">**SetColumns** richtet einen Spaltensatz angeben die Eigenschaften, die Spalten in der Tabelle und die Reihenfolge, in der sie enthalten sein sollen, berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="6790c-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="6790c-151">Wenn ein Anruf **SetColumns** vorgenommen wurden, übereinstimmen bestimmten Spalten in jeder Zeile und die Reihenfolge der Spalten die Spalte festlegen in der Anruf angegeben.</span><span class="sxs-lookup"><span data-stu-id="6790c-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="6790c-152">Falls kein Aufruf **SetColumns** vorgenommen wurden, gibt die Tabelle die standardspaltensammlung zurück.</span><span class="sxs-lookup"><span data-stu-id="6790c-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="6790c-153">Wenn keine dieser Anrufe vorgenommen wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="6790c-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="6790c-154">Jede Zeile enthält die Standardspalte in Standardreihenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6790c-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="6790c-155">Wenn die Spalte in einem Aufruf von [IMAPITable::SetColumns](imapitable-setcolumns.md) hergestellt Spalten auf PR_NULL gesetzt enthält, wird das Array [SPropValue](spropvalue.md) innerhalb der Zeile, die in _LppRows_ zurückgegeben leere Steckplätze enthalten.</span><span class="sxs-lookup"><span data-stu-id="6790c-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6790c-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="6790c-156">Notes to implementers</span></span>

<span data-ttu-id="6790c-157">Sie können einen Anrufer zum Anfordern von nicht unterstützten Spalte, die in der Spalte Gruppe eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6790c-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="6790c-158">In diesem Fall wird die Eigenschaft Typ Teil der Eigenschafts-Tag und MAPI_E_NOT_FOUND im-Eigenschaftenwert für die Spalte nicht unterstützte versehen Sie PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="6790c-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="6790c-159">Die Anzahl der Zeilen einer Anforderung, sondern als Voraussetzung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="6790c-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="6790c-160">Sie können an einer beliebigen Stelle aus keine Zeilen zurückgeben, wenn keine Zeilen in die Richtung der Abfrage, auf die angeforderte Anzahl vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6790c-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="6790c-161">Nur die Zeilen, die dem Benutzer angezeigt wird, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden sodass Aufrufer gültige Annahmen bezüglich des Umfangs der Daten und zusätzliche Arbeit vermeiden zurück.</span><span class="sxs-lookup"><span data-stu-id="6790c-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6790c-162">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6790c-162">Notes to callers</span></span>

<span data-ttu-id="6790c-163">In der Regel werden Sie am Ende beliebig viele Zeilen, die Sie in der _lRowCount_ -Parameter angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="6790c-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="6790c-164">Jedoch zurück Wenn Speicher oder-Implementierung Grenzwerten handelt es sich ein Problem oder der Vorgang der Anfang oder das Ende der Tabelle vorzeitig erreicht, **QueryRows** weniger Zeilen als angefordert.</span><span class="sxs-lookup"><span data-stu-id="6790c-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="6790c-165">Wenn **QueryRows** MAPI_E_BUSY zurückgibt, wird rufen Sie die [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) -Methode auf, und wiederholen Sie den Anruf an **QueryRows** , wenn der asynchrone Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6790c-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="6790c-166">Beim Aufruf von **QueryRows**, achten Sie darauf, dass der Zeitpunkt des asynchronen Benachrichtigungen das Rowset fest potenziell dazu führen, dass Sie ähnliche aus **QueryRows** erhalten haben, nicht für die zugrunde liegenden Daten genau darstellen.</span><span class="sxs-lookup"><span data-stu-id="6790c-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="6790c-167">Legen Sie beispielsweise ein Aufruf von **QueryRows** , einen Ordner Inhalt Tabelle Folgendes, dass das Löschen einer Nachricht, aber vor dem Empfang des die entsprechende Benachrichtigung verursacht die gelöschte Zeile in der Zeile zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6790c-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="6790c-168">Warten Sie immer eine Benachrichtigung vor dem Aktualisieren der Ansicht der Daten des Benutzers eingehen.</span><span class="sxs-lookup"><span data-stu-id="6790c-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="6790c-169">Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="6790c-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6790c-170">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6790c-170">MFCMAPI reference</span></span>

<span data-ttu-id="6790c-171">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6790c-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6790c-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6790c-172">**File**</span></span>|<span data-ttu-id="6790c-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6790c-173">**Function**</span></span>|<span data-ttu-id="6790c-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6790c-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6790c-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="6790c-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="6790c-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="6790c-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="6790c-177">MFCMAPI (engl.) verwendet **die QueryRows** abzurufenden Zeilen in der Tabelle, in der Ansicht zu laden.</span><span class="sxs-lookup"><span data-stu-id="6790c-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6790c-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6790c-178">See also</span></span>



[<span data-ttu-id="6790c-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="6790c-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="6790c-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="6790c-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="6790c-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="6790c-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="6790c-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6790c-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="6790c-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6790c-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6790c-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6790c-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="6790c-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6790c-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6790c-186">SRow</span><span class="sxs-lookup"><span data-stu-id="6790c-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="6790c-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="6790c-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="6790c-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6790c-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="6790c-189">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6790c-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

