---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792470"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="da72d-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="da72d-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="da72d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da72d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da72d-105">Definiert die jeweiligen Eigenschaften und die Reihenfolge der Eigenschaften als Spalten in der Tabelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="da72d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da72d-106">Parameters</span></span>

 <span data-ttu-id="da72d-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="da72d-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="da72d-108">[in] Zeiger auf ein Array von Eigenschaftentags, identifiziert Eigenschaften als Spalten in der Tabelle eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="da72d-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="da72d-109">Der Eigenschaft Typ Teil jedes Tag kann ein gültiger Typ oder **PR_NULL** Reservieren von Speicherplatz für nachfolgende Ergänzungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="da72d-110">Der _LpPropTagArray_ -Parameter kann nicht auf NULL festgelegt werden. Jede Tabelle muss mindestens eine Spalte haben.</span><span class="sxs-lookup"><span data-stu-id="da72d-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="da72d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da72d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="da72d-112">[in] Bitmaske aus Flags, die steuert die Rückgabe von einen asynchronen Aufruf an **SetColumns**, beispielsweise wenn **SetColumns** in der Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da72d-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="da72d-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="da72d-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="da72d-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="da72d-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="da72d-115">Anforderungen, die der Vorgang der Spalte Einstellung werden ausgeführt, asynchron verursacht **SetColumns** , potenziell zurückzugeben, bevor der Vorgang vollständig abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="da72d-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="da72d-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="da72d-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="da72d-117">Ermöglicht die Tabelle, um den Vorgang der Spalte Einstellung verschieben, bis die Daten tatsächlich erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="da72d-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da72d-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="da72d-118">Return value</span></span>

<span data-ttu-id="da72d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="da72d-119">S_OK</span></span> 
  
> <span data-ttu-id="da72d-120">Der Spalte Einstellung Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="da72d-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="da72d-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="da72d-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="da72d-122">Ein anderer Vorgang wird ausgeführt, die verhindert, die Spalte festlegen Vorgang dass gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="da72d-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="da72d-123">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="da72d-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da72d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da72d-124">Remarks</span></span>

<span data-ttu-id="da72d-125">Die Spalte einer Tabelle ist die Gruppe von Eigenschaften, die die Spalten für die Zeilen in der Tabelle bilden.</span><span class="sxs-lookup"><span data-stu-id="da72d-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="da72d-126">Es ist eine Standardspalte für jede Art von Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da72d-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="da72d-127">Die standardspaltensammlung besteht aus den Eigenschaften, die der Tabelle Implementierer automatisch enthält.</span><span class="sxs-lookup"><span data-stu-id="da72d-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="da72d-128">Benutzer können diese durch Aufrufen der Methode **IMAPITable::SetColumns** Standard ändern.</span><span class="sxs-lookup"><span data-stu-id="da72d-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="da72d-129">Sie können anfordern, dass weitere Spalten hinzugefügt werden, auf den Standardwert festgelegt, wenn die Tabelle-Implementierung unterstützt diese Spalten entfernt werden soll, oder die Reihenfolge der Spalten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="da72d-130">**SetColumns** gibt die Spalten, die zurückgegeben werden mit jeder Zeile und die Reihenfolge der diese Spalten in der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="da72d-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="da72d-131">Der Erfolg des Vorgangs **SetColumns** wird deutlich, nachdem ein nachfolgender Aufruf ausgeführt wurde, um die Daten der Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="da72d-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="da72d-132">Es ist, dass Fehler gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="da72d-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="da72d-133">Notes to implementers</span></span>

<span data-ttu-id="da72d-134">Einige Anbieter zulassen Gespräch **SetColumns** bestellen nur die Spalten, die Teil der Spalten für eine Tabellenansicht verfügbaren sind.</span><span class="sxs-lookup"><span data-stu-id="da72d-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="da72d-135">Andere Anbieter zulassen Gespräch **SetColumns** , um alle Spalten der Tabelle, einschließlich derjenigen, die Eigenschaften nicht in der ursprünglichen Spalte Sammlung enthält bestellen.</span><span class="sxs-lookup"><span data-stu-id="da72d-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="da72d-136">TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollte Anbieter zurückgeben, der Eigenschaftentyp PT_ERROR und den Wert einer Eigenschaft NULL für Spalten, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="da72d-137">Sie müssen nicht reagieren Sie auf die Kennzeichnung des TBL_ASYNC anfordern, dass der Vorgang asynchron sein.</span><span class="sxs-lookup"><span data-stu-id="da72d-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="da72d-138">Wenn Sie asynchrone Set-Spaltendefinition nicht unterstützen, führen Sie den Vorgang synchron.</span><span class="sxs-lookup"><span data-stu-id="da72d-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="da72d-139">Wenn Sie das Kennzeichen TBL_ASYNC und eine andere asynchrone unterstützen können wird Vorgang noch ausgeführt, MAPI_E_BUSY zurück.</span><span class="sxs-lookup"><span data-stu-id="da72d-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="da72d-140">Geben Sie andernfalls S_OK zurück, unabhängig davon, ob Sie alle Eigenschaften in Array der Tag-Eigenschaft enthalten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="da72d-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="da72d-141">Fehler aufgrund von nicht unterstützten Eigenschaften sollte **IMAPITable** Methoden zurückgegeben werden, die Daten enthält, wie **QueryRows**abrufen.</span><span class="sxs-lookup"><span data-stu-id="da72d-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="da72d-142">Generieren Sie Benachrichtigungen für Zeilen, in denen ausgeblendet sind nicht aus der Ansicht durch **Restrict**Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="da72d-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="da72d-143">Beim Senden von Benachrichtigungen der Tabelle, die Reihenfolge der Eigenschaften in der **Zeile** Mitglied der [TABLE_NOTIFICATION](table_notification.md) -Struktur und der Reihenfolge vom angegebenen muss des letzten Aufrufs **SetColumns** mit dem Zeitpunkt der Erstellung, die die Benachrichtigung anfordern gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="da72d-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="da72d-144">Eine andere Kennzeichnung, TBL_BATCH, ermöglicht es dem Aufrufer anzugeben, dass der Tabelle Implementierer verzögern kann die Ergebnisse des Vorgangs bis zu einem späteren Zeitpunkt auswerten.</span><span class="sxs-lookup"><span data-stu-id="da72d-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="da72d-145">Wann immer möglich, sollten Aufrufer dieses Flag festgelegt, da im Batchmodus Vorgang verbessert die Leistung.</span><span class="sxs-lookup"><span data-stu-id="da72d-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="da72d-146">Häufig ist es sinnvoll für Anrufer, reservieren einige Spalten in der abgerufenen Rowset für Werte, die später hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="da72d-147">Anrufer Zweck zu diesem Platzieren von **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) an den gewünschten Positionen im Array Eigenschaft-Tag **SetColumns**übergeben; die Tabelle wird dann wieder Durchgang **PR_NULL** an diese Positionen in allen Zeilen mit **QueryRows**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="da72d-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="da72d-148">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="da72d-148">Notes to callers</span></span>

<span data-ttu-id="da72d-149">Beim Erstellen des Arrays-Tag-Eigenschaft für den Parameter _LpPropTagArray_ Reihenfolge, die Tags in der Reihenfolge, in der Sie die Spalten in der Tabelle angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="da72d-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="da72d-150">Mehrwertige Eigenschaften, die in der Spalte festlegen, indem die mehrwertige Instanzenflag oder MVI_FLAG-Konstante, um das Eigenschafts-Tag anwenden enthalten sein können angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="da72d-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="da72d-151">Legen Sie dieses Flag, indem das Eigenschafts-Tag für die ein einwertiges Version der-Eigenschaft als Parameter an das Makro MVI_PROP wie folgt:</span><span class="sxs-lookup"><span data-stu-id="da72d-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="da72d-152">Das Makro MVI_PROP wird für die Eigenschaft, aktivieren das Tag in einem mehrwertigen Tag MVI_FLAG festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da72d-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="da72d-153">Wenn Sie versehentlich MVI_PROP für eine Eigenschaft einwertig aufrufen versuchen, MAPI den Anruf ignoriert und das Eigenschafts-Tag unverändert lassen.</span><span class="sxs-lookup"><span data-stu-id="da72d-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="da72d-154">Sie können durch Festlegen auf **PR_NULL** im Array Tag-Eigenschaft wird in der Spalte Menge Speicherplatz reservieren Eigenschaftentags einschließen.</span><span class="sxs-lookup"><span data-stu-id="da72d-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="da72d-155">Reservieren von Speicherplatz, können Sie eine Spalte festgelegt, ohne dass eine neue Eigenschaft Tag eines Arrays hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="da72d-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="da72d-156">Wenn der Aufruf **SetColumns** , eine Änderung Reihenfolge einer Tabelle Spalten veranlasst und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, ist es möglich, für die Anzahl der Zeilen in der Tabelle zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="da72d-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="da72d-157">In diesem Fall werden alle Textmarken für die Tabelle verworfen.</span><span class="sxs-lookup"><span data-stu-id="da72d-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="da72d-158">Weitere Informationen dazu, wie Sie mehrwertige Spalten Tabellen beeinflussen, finden Sie unter [Arbeiten mit Spalten mit mehreren Werten](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="da72d-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="da72d-159">Festlegen von Spalten ist standardmäßig eine synchrone Operation.</span><span class="sxs-lookup"><span data-stu-id="da72d-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="da72d-160">Sie können jedoch die Tabelle, um den Vorgang zu verschieben, solange die Daten benötigt werden, indem Sie das TBL_BATCH-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="da72d-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="da72d-161">Wenn Sie dieses Flag kann die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="da72d-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="da72d-162">Einer anderen Kennzeichnung, TBL_ASYNC, wird den Vorgang asynchron, sodass **SetColumns** , zurückzugeben, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="da72d-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="da72d-163">Um zu bestimmen, tritt Abschluss, rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="da72d-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="da72d-164">Ein Aufruf von **SetColumns** zurück MAPI_E_BUSY, was bedeutet, dass ein anderer Vorgang den Vorgang gestartet wird, verhindert können Sie [IMAPITable::Abort](imapitable-abort.md) , um den Vorgang in Arbeit abzubrechen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="da72d-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="da72d-165">Sie können auch [HrAddColumnsEx](hraddcolumnsex.md) zum Ändern einer Spalte aufrufen.</span><span class="sxs-lookup"><span data-stu-id="da72d-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="da72d-166">Der Unterschied zwischen **HrAddColumnsEx** und **IMAPITable::SetColumns** ist, dass **HrAddColumnsEx** weniger flexibel ist. Es kann nur Spalten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="da72d-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="da72d-167">Am Anfang des Satzes Spalte werden die zusätzlichen Spalten angeordnet. nach dieser Spalten werden alle vorhandene Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da72d-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="da72d-168">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="da72d-168">MFCMAPI reference</span></span>

<span data-ttu-id="da72d-169">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da72d-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da72d-170">**Datei**</span><span class="sxs-lookup"><span data-stu-id="da72d-170">**File**</span></span>|<span data-ttu-id="da72d-171">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="da72d-171">**Function**</span></span>|<span data-ttu-id="da72d-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="da72d-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da72d-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="da72d-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="da72d-174">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="da72d-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="da72d-175">MFCMAPI (engl.) verwendet die **IMAPITable::SetColumns** -Methode, um die gewünschten Spalten für die Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da72d-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da72d-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da72d-176">See also</span></span>



[<span data-ttu-id="da72d-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="da72d-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="da72d-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="da72d-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="da72d-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="da72d-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="da72d-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="da72d-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="da72d-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="da72d-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="da72d-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="da72d-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="da72d-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="da72d-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="da72d-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="da72d-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="da72d-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="da72d-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="da72d-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="da72d-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="da72d-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="da72d-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="da72d-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da72d-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="da72d-189">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="da72d-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

