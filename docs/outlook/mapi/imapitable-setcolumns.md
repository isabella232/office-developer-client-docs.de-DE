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
# <a name="imapitablesetcolumns"></a><span data-ttu-id="edf09-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="edf09-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="edf09-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edf09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edf09-105">Definiert die Eigenschaften und die Reihenfolge der Eigenschaften, die als Spalten in der Tabelle angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edf09-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="edf09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edf09-106">Parameters</span></span>

 <span data-ttu-id="edf09-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="edf09-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="edf09-108">in Zeiger auf ein Array von Eigenschaftstags, das Eigenschaften angibt, die als Spalten in der Tabelle eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edf09-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="edf09-109">Der Eigenschaftentyp Teil jedes Tags kann auf einen gültigen Typ oder auf **PR_NULL** festgelegt werden, um Platz für nachfolgende Ergänzungen zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="edf09-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="edf09-110">Der Parameter _lpPropTagArray_ kann nicht auf NULL festgelegt werden; jede Tabelle muss mindestens eine Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="edf09-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="edf09-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edf09-111">_ulFlags_</span></span>
  
> <span data-ttu-id="edf09-112">in Bitmaske von Flags, die die Rückgabe eines asynchronen Aufrufs an SetColumns steuert, beispielsweise wenn SetColumns in Notification verwendet wird. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="edf09-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="edf09-113">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="edf09-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="edf09-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="edf09-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="edf09-115">Fordert, dass der Vorgang der Spalten Einstellung asynchron ausgeführt \*\*\*\* wird, sodass SetColumns potenziell zurückgegeben werden können, bevor der Vorgang vollständig abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="edf09-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="edf09-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="edf09-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="edf09-117">Ermöglicht es der Tabelle, den Vorgang der Spalten Einstellung zu verschieben, bis die Daten tatsächlich erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="edf09-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edf09-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edf09-118">Return value</span></span>

<span data-ttu-id="edf09-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="edf09-119">S_OK</span></span> 
  
> <span data-ttu-id="edf09-120">Die Spalten Einstellung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="edf09-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="edf09-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="edf09-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="edf09-122">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass die Spalten Einstellung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="edf09-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="edf09-123">Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edf09-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edf09-124">Remarks</span></span>

<span data-ttu-id="edf09-125">Der Spaltensatz einer Tabelle ist die Gruppe von Eigenschaften, die die Spalten für die Zeilen in der Tabelle bilden.</span><span class="sxs-lookup"><span data-stu-id="edf09-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="edf09-126">Für jeden Tabellentyp ist eine Standardspaltengruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="edf09-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="edf09-127">Der Standardspaltensatz besteht aus den Eigenschaften, die von der Tabellen Implementierung automatisch eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="edf09-128">Tabellen Benutzer können diese Standardeinstellung ändern, indem Sie die **IMAPITable::** SetColumns-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="edf09-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="edf09-129">Sie können anfordern, dass andere Spalten dem Standardsatz hinzugefügt werden, wenn die Tabellen Implementierung Sie unterstützt, dass Spalten entfernt werden, oder dass die Reihenfolge der Spalten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="edf09-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="edf09-130">\*\*\*\* SetColumns gibt die Spalten an, die mit jeder Zeile und der Reihenfolge dieser Spalten innerhalb der Zeile zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="edf09-131">Der Erfolg des SetColumns-Vorgangs ist nur offensichtlich, nachdem ein weiterer Aufruf ausgeführt wurde, um die Daten der Tabelle abzurufen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="edf09-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="edf09-132">Es werden dann Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="edf09-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="edf09-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="edf09-133">Notes to implementers</span></span>

<span data-ttu-id="edf09-134">Einige Anbieter lassen einen \*\*\*\* SetColumns-Aufruf nur Tabellenspalten zu, die Teil der verfügbaren Spalten für eine Tabellenansicht sind.</span><span class="sxs-lookup"><span data-stu-id="edf09-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="edf09-135">Andere Anbieter ermöglichen einen \*\*\*\* SetColumns-Aufruf zum Sortieren aller Tabellenspalten, einschließlich der Eigenschaften, die nicht im ursprünglichen Spaltensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="edf09-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="edf09-136">Wenn TBL_BATCH für asynchrone Vorgänge festgelegt ist, sollten Anbieter einen Eigenschaftentyp von PT_ERROR und einen Eigenschaftswert von NULL für Spalten zurückgeben, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="edf09-137">Sie müssen nicht auf das TBL_ASYNC-Flag Antworten, das die asynchrone Operation anfordert.</span><span class="sxs-lookup"><span data-stu-id="edf09-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="edf09-138">Wenn Sie die asynchrone Spaltensatz Definition nicht unterstützen, führen Sie den Vorgang synchron aus.</span><span class="sxs-lookup"><span data-stu-id="edf09-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="edf09-139">Wenn Sie das TBL_ASYNC-Flag unterstützen können und ein weiterer asynchroner Vorgang noch ausgeführt wird, geben Sie MAPI_E_BUSY zurück.</span><span class="sxs-lookup"><span data-stu-id="edf09-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="edf09-140">Andernfalls wird S_OK zurückgegeben, unabhängig davon, ob Sie alle im Property-Tag-Array enthaltenen Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="edf09-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="edf09-141">Fehler, die aus nicht unterstützten Eigenschaften resultieren, sollten von **IMAPITable** -Methoden zurückgegeben werden, die Daten wie **QueryRows**abrufen.</span><span class="sxs-lookup"><span data-stu-id="edf09-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="edf09-142">Generieren Sie keine Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von **Restrict**ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="edf09-143">Beim Senden von Tabellen Benachrichtigungen muss die Reihenfolge der Eigenschaften im **Row** -Element der [TABLE_NOTIFICATION](table_notification.md) -Struktur und der durch den letzten SetColumns-Aufruf angegebenen Reihenfolge mit dem Zeitpunkt übereinstimmen, zu dem die Benachrichtigungsanforderung \*\*\*\* gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="edf09-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="edf09-144">Ein weiteres Flag, TBL_BATCH, ermöglicht es Aufrufern, anzugeben, dass die Tabellen Implementierung die Auswertung der Ergebnisse des Vorgangs bis zu einem späteren Zeitpunkt zurückstellen kann.</span><span class="sxs-lookup"><span data-stu-id="edf09-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="edf09-145">Wenn möglich, sollten Anrufer dieses Flag festlegen, da der Batchvorgang die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="edf09-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="edf09-146">Es ist oft hilfreich, wenn Anrufer einige Spalten im abgerufenen Zeilensatz für Werte reservieren, die später hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edf09-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="edf09-147">Anrufer tun dies, indem Sie **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)) an den gewünschten Positionen im Property Tag-Array an \*\*\*\* SetColumns übergeben; die Tabelle übergibt dann **PR_NULL** an diesen Positionen in allen Zeilen, die mit **QueryRows**abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="edf09-148">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="edf09-148">Notes to callers</span></span>

<span data-ttu-id="edf09-149">Beim Erstellen des Eigenschaftentag Arrays für den Parameter _lpPropTagArray_ ordnen Sie die Tags in der Reihenfolge an, in der die Spalten in der Tabellenansicht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edf09-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="edf09-150">Sie können mehrwertige Eigenschaften angeben, die in den Spaltensatz eingeschlossen werden sollen, indem Sie das Flag für mehrwertige Instanzen oder MVI_FLAG-Konstante auf das Property-Tag anwenden.</span><span class="sxs-lookup"><span data-stu-id="edf09-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="edf09-151">Legen Sie dieses Flag fest, indem Sie das Property-Tag für die einwertige Version der Eigenschaft wie folgt als Parameter an das MVI_PROP-Makro übergeben:</span><span class="sxs-lookup"><span data-stu-id="edf09-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="edf09-152">Das MVI_PROP-Makro legt MVI_FLAG für die Eigenschaft fest, wobei das Tag in ein mehrwertiges Tag verwandelt wird.</span><span class="sxs-lookup"><span data-stu-id="edf09-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="edf09-153">Wenn Sie fälschlicherweise versuchen, MVI_PROP für eine einwertige Eigenschaft aufzurufen, ignoriert MAPI den Aufruf und lässt das Tag der Eigenschaft unverändert.</span><span class="sxs-lookup"><span data-stu-id="edf09-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="edf09-154">Sie können Eigenschaftstags, die auf **PR_NULL** festgelegt sind, im Property-Tag-Array einfügen, um Platz im Spaltensatz zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="edf09-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="edf09-155">Durch das Reservieren von Speicherplatz können Sie zu einem Spaltensatz hinzufügen, ohne ein neues Property-Tag-Array zuweisen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="edf09-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="edf09-156">Wenn der Aufruf von \*\*\*\* SetColumns eine Änderung an der Reihenfolge der Spalten einer Tabelle bewirkt und eine oder mehrere dieser Spalten eine mehrwertige Eigenschaft darstellen, ist es möglich, dass die Anzahl der Zeilen in der Tabelle erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="edf09-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="edf09-157">In diesem Fall werden alle Lesezeichen für die Tabelle verworfen.</span><span class="sxs-lookup"><span data-stu-id="edf09-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="edf09-158">Weitere Informationen zur Auswirkung von mehrwertigen Spalten auf Tabellen finden Sie unter [Working with](working-with-multivalued-columns.md)mehr-Valued Columns.</span><span class="sxs-lookup"><span data-stu-id="edf09-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="edf09-159">Das Festlegen von Spalten ist standardmäßig ein synchroner Vorgang.</span><span class="sxs-lookup"><span data-stu-id="edf09-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="edf09-160">Sie können jedoch zulassen, dass die Tabelle den Vorgang so lange verschiebt, bis die Daten erforderlich sind, indem Sie das TBL_BATCH-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="edf09-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="edf09-161">Durch Festlegen dieses Flags kann die Leistung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="edf09-162">Ein weiteres Flag, TBL_ASYNC, macht den Vorgang asynchron \*\*\*\* , sodass SetColumns zurückgegeben werden können, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="edf09-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="edf09-163">Um zu bestimmen, wann der Abschluss auftritt, rufen Sie [IMAPITable:: GetStatus](imapitable-getstatus.md)auf.</span><span class="sxs-lookup"><span data-stu-id="edf09-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="edf09-164">Wenn ein Aufruf von \*\*\*\* SetColumns MAPI_E_BUSY zurückgibt, was bedeutet, dass ein anderer Vorgang das Starten des Vorgangs verhindert, können Sie [IMAPITable:: Abort](imapitable-abort.md) aufrufen, um den laufenden Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="edf09-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="edf09-165">Sie können auch [HrAddColumnsEx](hraddcolumnsex.md) aufrufen, um einen Spaltensatz zu ändern.</span><span class="sxs-lookup"><span data-stu-id="edf09-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="edf09-166">Der Unterschied zwischen **HrAddColumnsEx** und **IMAPITable::** SetColumns besteht darin, dass **HrAddColumnsEx** nicht so flexibel ist; Es können nur Spalten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="edf09-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="edf09-167">Die zusätzlichen Spalten werden am Anfang des Spaltensatzes angeordnet; alle vorhandenen Spalten werden nach diesen Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="edf09-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="edf09-168">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="edf09-168">MFCMAPI reference</span></span>

<span data-ttu-id="edf09-169">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="edf09-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="edf09-170">**Datei**</span><span class="sxs-lookup"><span data-stu-id="edf09-170">**File**</span></span>|<span data-ttu-id="edf09-171">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="edf09-171">**Function**</span></span>|<span data-ttu-id="edf09-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="edf09-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edf09-173">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="edf09-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="edf09-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="edf09-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="edf09-175">MFCMAPI verwendet die **IMAPITable::** SetColumns-Methode, um die gewünschten Spalten für die Tabelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="edf09-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="edf09-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edf09-176">See also</span></span>



[<span data-ttu-id="edf09-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="edf09-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="edf09-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="edf09-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="edf09-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="edf09-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="edf09-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="edf09-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="edf09-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="edf09-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="edf09-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="edf09-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="edf09-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="edf09-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="edf09-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="edf09-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="edf09-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="edf09-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="edf09-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="edf09-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="edf09-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="edf09-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="edf09-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edf09-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="edf09-189">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="edf09-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

