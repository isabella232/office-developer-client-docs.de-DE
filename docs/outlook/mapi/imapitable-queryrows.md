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
# <a name="imapitablequeryrows"></a><span data-ttu-id="5b6e7-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="5b6e7-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="5b6e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b6e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b6e7-105">Gibt eine oder mehrere Zeilen aus einer Tabelle zurück, die an der aktuellen Cursorposition beginnen.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="5b6e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b6e7-106">Parameters</span></span>

 <span data-ttu-id="5b6e7-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="5b6e7-107">_lRowCount_</span></span>
  
> <span data-ttu-id="5b6e7-108">in Maximale Anzahl der zurückzugebenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="5b6e7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b6e7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5b6e7-110">in Bitmaske von Flags, die Steuern, wie Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="5b6e7-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5b6e7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5b6e7-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="5b6e7-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="5b6e7-113">Verhindert das Fortschreiten des Cursors als Ergebnis des Zeilen Abrufs.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="5b6e7-114">Wenn das TBL_NOADVANCE-Flag festgelegt ist, zeigt der Cursor auf die erste zurückgegebene Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="5b6e7-115">Wenn das TBL_NOADVANCE-Flag nicht festgelegt ist, zeigt der Cursor auf die Zeile nach der letzten zurückgegebenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="5b6e7-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="5b6e7-116">_lppRows_</span></span>
  
> <span data-ttu-id="5b6e7-117">Out Zeiger auf einen Zeiger auf eine [SRowSet](srowset.md) -Struktur, in der sich die Tabellenzeilen befinden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5b6e7-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b6e7-118">Return value</span></span>

<span data-ttu-id="5b6e7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b6e7-119">S_OK</span></span> 
  
> <span data-ttu-id="5b6e7-120">Die Zeilen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="5b6e7-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="5b6e7-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5b6e7-122">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilenabruf Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="5b6e7-123">Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="5b6e7-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b6e7-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="5b6e7-125">Der Parameter _IRowCount_ wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5b6e7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b6e7-126">Remarks</span></span>

<span data-ttu-id="5b6e7-127">Die **IMAPITable:: QueryRows** -Methode ruft eine oder mehrere Datenzeilen aus einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="5b6e7-128">Der Wert des _IRowCount_ -Parameters wirkt sich auf den Anfangspunkt des Abrufs aus.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="5b6e7-129">Wenn _IRowCount_ positiv ist, werden Zeilen nach vorn gelesen, beginnend an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="5b6e7-130">Wenn _IRowCount_ negativ ist, wird der Startpunkt von **QueryRows** zurückgesetzt, indem die angegebene Anzahl von Zeilen rückwärts bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="5b6e7-131">Nach dem Zurücksetzen des Cursors werden die Zeilen in der Forward-Reihenfolge gelesen.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="5b6e7-132">Das **Crows** -Element in der [SRowSet](srowset.md) -Struktur, auf die durch den _lppRows_ -Parameter verwiesen wird, gibt die Anzahl der zurückgegebenen Zeilen an.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="5b6e7-133">Wenn null Zeilen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="5b6e7-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="5b6e7-134">Der Cursor war bereits am Anfang der Tabelle positioniert, und der Wert von _IRowCount_ ist negativ.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="5b6e7-135">Oder</span><span class="sxs-lookup"><span data-stu-id="5b6e7-135">-Or-</span></span> 
    
- <span data-ttu-id="5b6e7-136">Der Cursor wurde bereits am Ende der Tabelle positioniert, und der Wert von _IRowCount_ ist positiv.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="5b6e7-137">Die Anzahl der Spalten und ihre Reihenfolge ist für jede Zeile identisch.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="5b6e7-138">Wenn eine Eigenschaft nicht für eine Zeile vorhanden ist oder beim Lesen einer Eigenschaft ein Fehler auftritt, enthält die **SPropValue** -Struktur für die-Eigenschaft in der Zeile die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="5b6e7-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="5b6e7-139">PT_ERROR für den Eigenschaftentyp im **ulPropTag** -Element.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="5b6e7-140">MAPI_E_NOT_FOUND für den **Wert** Member.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="5b6e7-141">Der für die [SPropValue](spropvalue.md) -Strukturen im Zeilensatz, auf den der _lppRows_ -Parameter zeigt, verwendete Arbeitsspeicher muss für jede Zeile separat reserviert und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="5b6e7-142">Verwenden Sie [mapifreebufferfreigegeben](mapifreebuffer.md) , um die Eigenschaftswert Strukturen freizugeben und den Zeilensatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="5b6e7-143">Wenn ein Aufruf von **QueryRows** NULL zurückgibt, aber den Anfang oder das Ende der Tabelle angibt, muss nur die **SRowSet** -Struktur selbst freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="5b6e7-144">Weitere Informationen zum reservieren und Freigeben von Arbeitsspeicher in einer **SRowSet** -Struktur finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="5b6e7-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="5b6e7-145">Die zurückgegebenen Zeilen und die Reihenfolge, in der Sie zurückgegeben werden, hängen davon ab, ob erfolgreiche Aufrufe an [IMAPITable:: Restrict](imapitable-restrict.md) und [IMAPITable:: sortable](imapitable-sorttable.md)vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="5b6e7-146">Filter Zeilen aus der Ansicht **einschränken** , sodass **QueryRows** nur die Zeilen zurückgibt, die den in der Einschränkung angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="5b6e7-147">**Sortable** legt eine Standard-oder kategorisierte Sortierreihenfolge fest, die sich auf die Reihenfolge der von **QueryRows**zurückgegebenen Zeilen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="5b6e7-148">Die zurückgegebenen Zeilen befinden sich in der in der [SSortOrderSet](ssortorderset.md) -Struktur angegebenen \*\*\*\* Reihenfolge, die an sortable übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="5b6e7-149">Die für jede Zeile zurückgegebenen Spalten und die Reihenfolge, in der Sie zurückgegeben werden, hängen davon ab, ob ein erfolgreicher Aufruf an [IMAPITable::](imapitable-setcolumns.md)SetColumns erfolgt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="5b6e7-150">\*\*\*\* SetColumns richtet eine Spaltengruppe ein, die die Eigenschaften angibt, die in Spalten in der Tabelle enthalten sein sollen, und die Reihenfolge, in der Sie eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="5b6e7-151">Wenn ein \*\*\*\* SetColumns-Aufruf ausgeführt wurde, stimmen die Spalten in jeder Zeile und die Reihenfolge dieser Spalten mit dem im Aufruf angegebenen Spaltensatz überein.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="5b6e7-152">Wenn kein \*\*\*\* SetColumns-Aufruf ausgeführt wurde, gibt die Tabelle den Standardspaltensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="5b6e7-153">Wenn keiner dieser Aufrufe vorgenommen wurde, gibt **QueryRows** alle Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="5b6e7-154">Jede Zeile enthält den standardmäßigen Spaltensatz in der Standardreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="5b6e7-155">Wenn der in einem Aufruf von [IMAPITable::](imapitable-setcolumns.md) SetColumns eingerichtete Spaltensatz Spalten enthält, die auf PR_NULL festgelegt sind, enthält das [SPropValue](spropvalue.md) -Array innerhalb des in _lppRows_ zurückgegebenen Rowsets leere Slots.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5b6e7-156">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="5b6e7-156">Notes to implementers</span></span>

<span data-ttu-id="5b6e7-157">Sie können einem Anrufer gestatten, eine nicht unterstützte Spalte anzufordern, die in den Spaltensatz eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="5b6e7-158">Wenn dies der Fall ist, platzieren Sie PT_ERROR im Eigenschafts Teil des Property-Tags und MAPI_E_NOT_FOUND im Eigenschaftswert für die nicht unterstützte Spalte.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="5b6e7-159">Behandeln Sie die Zeilenanzahl als Anforderung anstatt als Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="5b6e7-160">Sie können an einer beliebigen Stelle von null Zeilen zurückkehren, wenn es keine Zeilen in der Richtung der Abfrage gibt, um die angeforderte Nummer.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="5b6e7-161">Gibt nur die Zeilen zurück, die dem Benutzer angezeigt werden, wenn Zeilen aus einer kategorisierten Tabellenansicht angefordert werden, sodass der Aufrufer gültige Annahmen über den Datenbereich treffen und zusätzliche Arbeit vermeiden kann.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5b6e7-162">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="5b6e7-162">Notes to callers</span></span>

<span data-ttu-id="5b6e7-163">In der Regel werden Sie so viele Zeilen wie im Parameter _lRowCount_ angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="5b6e7-164">Wenn jedoch Speicher-oder Implementierungs Grenzwerte ein Problem sind oder wenn der Vorgang vorzeitig den Anfang oder das Ende der Tabelle erreicht, gibt **QueryRows** weniger Zeilen zurück als angefordert.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="5b6e7-165">Wenn **QUERYROWS** MAPI_E_BUSY zurückgibt, rufen Sie die [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) -Methode auf, und wiederholen Sie den Aufruf von **QueryRows** , wenn der asynchrone Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="5b6e7-166">Beachten Sie beim Aufrufen von **QueryRows**, dass der Zeitpunkt der asynchronen Benachrichtigungen potenziell dazu führen kann, dass der aus **QueryRows** zurückgegebene Zeilensatz die zugrunde liegenden Daten nicht genau darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="5b6e7-167">Beispielsweise bewirkt ein Aufruf von **QueryRows** in der Inhaltstabelle eines Ordners nach dem Löschen einer Nachricht, jedoch vor dem Empfang der entsprechenden Benachrichtigung, dass die gelöschte Zeile im Zeilensatz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="5b6e7-168">Warten Sie immer, bis eine Benachrichtigung eingeht, bevor Sie die Benutzeransicht der Daten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="5b6e7-169">Weitere Informationen zum Abrufen von Zeilen aus Tabellen finden Sie unter [Abrufen von Daten aus Tabellenzeilen](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="5b6e7-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b6e7-170">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5b6e7-170">MFCMAPI reference</span></span>

<span data-ttu-id="5b6e7-171">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b6e7-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5b6e7-172">**File**</span></span>|<span data-ttu-id="5b6e7-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5b6e7-173">**Function**</span></span>|<span data-ttu-id="5b6e7-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5b6e7-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b6e7-175">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="5b6e7-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5b6e7-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="5b6e7-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="5b6e7-177">MFCMAPI verwendet die **IMAPITable:: QueryRows** -Methode zum Abrufen von Zeilen in der Tabelle, um Sie in die Ansicht zu laden.</span><span class="sxs-lookup"><span data-stu-id="5b6e7-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b6e7-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b6e7-178">See also</span></span>



[<span data-ttu-id="5b6e7-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="5b6e7-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="5b6e7-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="5b6e7-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="5b6e7-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="5b6e7-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="5b6e7-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="5b6e7-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="5b6e7-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="5b6e7-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="5b6e7-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5b6e7-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="5b6e7-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5b6e7-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5b6e7-186">SRow</span><span class="sxs-lookup"><span data-stu-id="5b6e7-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="5b6e7-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="5b6e7-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="5b6e7-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b6e7-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="5b6e7-189">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5b6e7-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

