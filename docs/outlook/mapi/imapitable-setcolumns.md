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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416349"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="e7248-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e7248-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="e7248-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7248-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7248-105">Definiert die bestimmten Eigenschaften und die Reihenfolge der Eigenschaften, die in der Tabelle als Spalten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7248-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e7248-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7248-106">Parameters</span></span>

 <span data-ttu-id="e7248-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e7248-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e7248-108">[in] Zeiger auf ein Array von Eigenschaftstags, die Eigenschaften identifizieren, die als Spalten in der Tabelle enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="e7248-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="e7248-109">Der Eigenschaftentypteil jedes Tags kann auf einen  gültigen Typ festgelegt oder PR_NULL, um Platz für nachfolgende Ergänzungen zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e7248-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="e7248-110">Der  _lpPropTagArray-Parameter_ kann nicht auf NULL festgelegt werden. Jede Tabelle muss mindestens eine Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="e7248-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="e7248-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7248-111">_ulFlags_</span></span>
  
> <span data-ttu-id="e7248-112">[in] Bitmaske von Flags, die die Rückgabe eines asynchronen Aufrufs von **SetColumns** steuert, z. B. wenn **SetColumns** in der Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7248-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="e7248-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e7248-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="e7248-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="e7248-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="e7248-115">Fordert an, dass der Spalteneinstellungsvorgang asynchron ausgeführt wird, wodurch **SetColumns** möglicherweise zurückgesendet wird, bevor der Vorgang vollständig abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e7248-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="e7248-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="e7248-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="e7248-117">Ermöglicht der Tabelle, den Spalteneinstellungsvorgang so lange zu verschieben, bis die Daten tatsächlich erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e7248-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7248-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7248-118">Return value</span></span>

<span data-ttu-id="e7248-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7248-119">S_OK</span></span> 
  
> <span data-ttu-id="e7248-120">Der Spalteneinstellungsvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e7248-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="e7248-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e7248-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e7248-122">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Spalteneinstellungsvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e7248-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="e7248-123">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7248-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7248-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7248-124">Remarks</span></span>

<span data-ttu-id="e7248-125">Der Spaltensatz einer Tabelle ist die Gruppe von Eigenschaften, aus der die Spalten für die Zeilen in der Tabelle besteht.</span><span class="sxs-lookup"><span data-stu-id="e7248-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="e7248-126">Für jeden Tabellentyp ist ein Standardspaltensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e7248-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="e7248-127">Der Standardspaltensatz besteht aus den Eigenschaften, die der Tabellen implementier automatisch enthält.</span><span class="sxs-lookup"><span data-stu-id="e7248-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="e7248-128">Tabellenbenutzer können diesen Standardsatz ändern, indem sie die **IMAPITable::SetColumns-Methode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7248-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="e7248-129">Sie können anfordern, dass dem Standardsatz weitere Spalten hinzugefügt werden, wenn der Tabellen implementier sie unterstützt, dass Spalten entfernt oder die Reihenfolge der Spalten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e7248-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="e7248-130">**SetColumns** gibt die Spalten an, die mit jeder Zeile zurückgegeben werden, und die Reihenfolge dieser Spalten innerhalb der Zeile.</span><span class="sxs-lookup"><span data-stu-id="e7248-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="e7248-131">Der Erfolg des **SetColumns-Vorgangs** wird erst sichtbar, nachdem ein nachfolgender Aufruf zum Abrufen der Daten der Tabelle erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="e7248-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="e7248-132">Dann werden Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="e7248-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e7248-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e7248-133">Notes to implementers</span></span>

<span data-ttu-id="e7248-134">Einige Anbieter lassen einen **SetColumns-Aufruf** zu, um nur Tabellenspalten zu bestellen, die Teil der verfügbaren Spalten für eine Tabellenansicht sind.</span><span class="sxs-lookup"><span data-stu-id="e7248-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="e7248-135">Andere Anbieter ermöglichen einen **SetColumns-Aufruf,** um alle Tabellenspalten zu sortieren, einschließlich derjenigen, die Eigenschaften enthalten, die nicht im ursprünglichen Spaltensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e7248-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="e7248-136">Wenn TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollten Anbieter den Eigenschaftstyp PT_ERROR und den Eigenschaftswert NULL für Spalten zurückgeben, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e7248-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="e7248-137">Sie müssen nicht auf das TBL_ASYNC reagieren, das anfordert, dass der Vorgang asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="e7248-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="e7248-138">Wenn Sie keine asynchrone Spaltensatzdefinition unterstützen, führen Sie den Vorgang synchron aus.</span><span class="sxs-lookup"><span data-stu-id="e7248-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="e7248-139">Wenn Sie das TBL_ASYNC unterstützen können und ein weiterer asynchroner Vorgang noch ausgeführt wird, geben Sie die MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="e7248-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="e7248-140">Andernfalls geben Sie S_OK zurück, unabhängig davon, ob Sie alle Eigenschaften unterstützen, die im Eigenschaftentagarray enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e7248-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="e7248-141">Fehler, die sich aus nicht unterstützten Eigenschaften ergeben, sollten von **IMAPITable-Methoden** zurückgegeben werden, die Daten abrufen, z. B. **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="e7248-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="e7248-142">Generieren Sie keine Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von Restrict ausgeblendet **werden.**</span><span class="sxs-lookup"><span data-stu-id="e7248-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="e7248-143">Beim Senden von Tabellenbenachrichtigungen müssen  die Reihenfolge der Eigenschaften im Zeilenm member der [TABLE_NOTIFICATION-Struktur](table_notification.md) und die durch den letzten **SetColumns-Aufruf** angegebene Reihenfolge mit dem Zeitpunkt identisch sein, zu dem die Benachrichtigungsanforderung gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7248-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="e7248-144">Ein weiteres Flag, TBL_BATCH, ermöglicht Anrufern anzugeben, dass der Tabellen implementierer die Auswertung der Ergebnisse des Vorgangs auf einen späteren Zeitpunkt zurückdingen kann.</span><span class="sxs-lookup"><span data-stu-id="e7248-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="e7248-145">Wenn möglich, sollten Anrufer dieses Flag festlegen, da der Batchvorgang die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="e7248-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="e7248-146">Für Anrufer ist es häufig praktisch, einige Spalten im abgerufenen Zeilensatz für Werte zu reservieren, die später hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e7248-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="e7248-147">Aufrufer tun **dies, indem PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) an den gewünschten Positionen im Eigenschaftstagarray platziert werden, das an **SetColumns übergeben wird;** Die Tabelle gibt dann die PR_NULL **an** diesen Positionen in allen Zeilen zurück, die mit **QueryRows abgerufen werden.**</span><span class="sxs-lookup"><span data-stu-id="e7248-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e7248-148">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e7248-148">Notes to callers</span></span>

<span data-ttu-id="e7248-149">Beim Erstellen des Eigenschaftentagarrays für den  _lpPropTagArray-Parameter_ müssen Sie die Tags in der Reihenfolge sortieren, in der die Spalten in der Tabellenansicht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7248-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="e7248-150">Sie können mehrwertige Eigenschaften angeben, die in den Spaltensatz eingeschlossen werden sollen, indem Sie das Kennzeichen der mehrwertigen Instanz oder MVI_FLAG Eigenschaftstags anwenden.</span><span class="sxs-lookup"><span data-stu-id="e7248-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="e7248-151">Legen Sie dieses Flag durch Übergeben des Eigenschaftstags für die einwertig version der Eigenschaft als Parameter an das MVI_PROP makro wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e7248-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="e7248-152">Das MVI_PROP-Makro wird MVI_FLAG eigenschaft festlegen und das Tag in ein mehrwertiges Tag umfunktioniert.</span><span class="sxs-lookup"><span data-stu-id="e7248-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="e7248-153">Wenn Sie fälschlicherweise versuchen, MVI_PROP einer einwertigen Eigenschaft auf aufruft, ignoriert MAPI den Aufruf und belassen das Eigenschaftstag unverändert.</span><span class="sxs-lookup"><span data-stu-id="e7248-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="e7248-154">Sie können Eigenschaftstags, die auf PR_NULL festgelegt sind, in das Eigenschaftentagarray **hinzufügen,** um Platz im Spaltensatz zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="e7248-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="e7248-155">Wenn Sie Speicherplatz reservieren, können Sie einem Spaltensatz hinzufügen, ohne ein neues Eigenschaftentagarray zuweisen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e7248-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="e7248-156">Wenn der Aufruf von **SetColumns** eine Änderung der Reihenfolge der Spalten einer Tabelle bewirkt und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, kann die Anzahl der Zeilen in der Tabelle erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="e7248-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="e7248-157">In diesem Fall werden alle Lesezeichen für die Tabelle verworfen.</span><span class="sxs-lookup"><span data-stu-id="e7248-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="e7248-158">Weitere Informationen dazu, wie sich mehrwertige Spalten auf Tabellen auswirken, finden Sie unter [Working with Multivalued Columns](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="e7248-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="e7248-159">Das Festlegen von Spalten ist standardmäßig ein synchroner Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e7248-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="e7248-160">Sie können jedoch zulassen, dass die Tabelle den Vorgang so lange verschiebt, bis die Daten benötigt werden, indem Sie TBL_BATCH festlegen.</span><span class="sxs-lookup"><span data-stu-id="e7248-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="e7248-161">Das Festlegen dieses Kennzeichens kann die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="e7248-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="e7248-162">Ein weiteres Flag, TBL_ASYNC, macht den Vorgang asynchron, sodass **SetColumns** zurückgeben kann, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e7248-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="e7248-163">Rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md)auf, um zu bestimmen, wann der Abschluss erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e7248-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="e7248-164">Wenn ein Aufruf von **SetColumns** MAPI_E_BUSY, der angibt, dass ein anderer Vorgang das Starten des Vorgangs verhindert, können Sie [IMAPITable::Abort](imapitable-abort.md) aufrufen, um den ausgeführten Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e7248-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="e7248-165">Sie können auch [HrAddColumnsEx aufrufen,](hraddcolumnsex.md) um einen Spaltensatz zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e7248-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="e7248-166">Der Unterschied zwischen **HrAddColumnsEx und** **IMAPITable::SetColumns** ist, dass **HrAddColumnsEx** weniger flexibel ist. Es können nur Spalten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e7248-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="e7248-167">Die zusätzlichen Spalten werden am Anfang des Spaltensatzs platziert. alle vorhandenen Spalten werden nach diesen Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7248-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e7248-168">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="e7248-168">MFCMAPI reference</span></span>

<span data-ttu-id="e7248-169">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e7248-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e7248-170">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e7248-170">**File**</span></span>|<span data-ttu-id="e7248-171">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e7248-171">**Function**</span></span>|<span data-ttu-id="e7248-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e7248-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e7248-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e7248-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e7248-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="e7248-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="e7248-175">MFCMAPI verwendet die **IMAPITable::SetColumns-Methode,** um die gewünschten Spalten für die Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="e7248-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7248-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7248-176">See also</span></span>



[<span data-ttu-id="e7248-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e7248-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="e7248-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="e7248-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="e7248-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="e7248-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="e7248-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e7248-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="e7248-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e7248-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e7248-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="e7248-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="e7248-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e7248-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e7248-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e7248-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e7248-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e7248-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e7248-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e7248-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e7248-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e7248-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e7248-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7248-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e7248-189">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e7248-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

