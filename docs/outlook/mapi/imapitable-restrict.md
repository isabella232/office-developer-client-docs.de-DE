---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414620"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="8d16f-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8d16f-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="8d16f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d16f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d16f-105">Wendet einen Filter auf eine Tabelle an, wodurch der Zeilensatz auf nur die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8d16f-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8d16f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d16f-106">Parameters</span></span>

 <span data-ttu-id="8d16f-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="8d16f-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="8d16f-108">[in] Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Bedingungen des Filters definiert.</span><span class="sxs-lookup"><span data-stu-id="8d16f-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="8d16f-109">Durch übergeben von NULL im  _lpRestriction-Parameter_ wird der aktuelle Filter entfernt.</span><span class="sxs-lookup"><span data-stu-id="8d16f-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="8d16f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d16f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8d16f-111">[in] Bitmaske von Flags, die das Timing des Einschränkungsvorgangs steuert.</span><span class="sxs-lookup"><span data-stu-id="8d16f-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="8d16f-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8d16f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="8d16f-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="8d16f-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="8d16f-114">Startet den Vorgang asynchron und gibt zurück, bevor der Vorgang abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8d16f-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="8d16f-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="8d16f-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="8d16f-116">Die Auswertung des Filters wird so lange verf?en, bis die Daten in der Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d16f-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d16f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d16f-117">Return value</span></span>

<span data-ttu-id="8d16f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d16f-118">S_OK</span></span> 
  
> <span data-ttu-id="8d16f-119">Der Filter wurde erfolgreich angewendet.</span><span class="sxs-lookup"><span data-stu-id="8d16f-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="8d16f-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="8d16f-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="8d16f-121">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Einschränkungsvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8d16f-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="8d16f-122">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="8d16f-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="8d16f-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="8d16f-124">Die Tabelle kann den Vorgang nicht ausführen, da der bestimmte Filter, auf den der  _lpRestriction-Parameter_ verweist, zu kompliziert ist.</span><span class="sxs-lookup"><span data-stu-id="8d16f-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8d16f-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d16f-125">Remarks</span></span>

<span data-ttu-id="8d16f-126">Die **IMAPITable::Restrict-Methode** richtet eine Einschränkung oder einen Filter für eine Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="8d16f-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="8d16f-127">Wenn es eine vorherige Einschränkung gibt, wird sie verworfen und die neue angewendet.</span><span class="sxs-lookup"><span data-stu-id="8d16f-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="8d16f-128">Das Anwenden einer Einschränkung hat keine Auswirkungen auf die zugrunde liegenden Daten einer Tabelle. Es ändert einfach die Ansicht, indem die Zeilen, die abgerufen werden können, auf Zeilen mit Daten begrenzt werden, die die Einschränkung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="8d16f-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="8d16f-129">Es gibt verschiedene Arten von Einschränkungen, die jeweils mit einer anderen Struktur beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="8d16f-130">Die [SRestriction-Struktur](srestriction.md) enthält zwei Elemente: einen Wert, der den Typ der Einschränkung und die spezifische Struktur angibt, die für diesen Typ gilt.</span><span class="sxs-lookup"><span data-stu-id="8d16f-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="8d16f-131">Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von Restrict aus der Ansicht ausgeblendet **werden,** werden nie generiert.</span><span class="sxs-lookup"><span data-stu-id="8d16f-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="8d16f-132">Eine Eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8d16f-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="8d16f-133">Für eine mehrwertige Eigenschaft, die in einer Eigenschaftseinschränkung verwendet werden soll, muss MVI_FLAG festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="8d16f-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="8d16f-134">Wenn dieses Flag nicht festgelegt ist, wird es als vollständig geordnetes Tupel behandelt.</span><span class="sxs-lookup"><span data-stu-id="8d16f-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="8d16f-135">Bei einem Vergleich von zwei mehrwertigen Spalten werden die Spaltenelemente in der Reihenfolge verglichen und das Verhältnis der Spalten bei der ersten Ungleichung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d16f-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="8d16f-136">Gleichheit wird nur zurückgegeben, wenn die verglichenen Spalten dieselben Werte in derselben Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d16f-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="8d16f-137">Wenn eine Spalte weniger Werte als die andere hat, ist die gemeldete Beziehung die eines Nullwerts zum anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="8d16f-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="8d16f-138">Weitere Informationen zu Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="8d16f-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d16f-139">Wenn Sie dynamische Abfragen zum Suchen nach Daten auf dem Server erstellen, verwenden Sie die **FindRow-Methode,** anstatt die **Restrict-Methode** und die **QueryRows-Methode** zusammen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="8d16f-140">Die **Restrict-Methode** erstellt eine zwischengespeicherte Ansicht, die zum Auswerten aller Nachrichten verwendet wird, die dem Basisordner hinzugefügt oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="8d16f-141">Wenn eine Clientanwendung die **Restrict-Methode** für jede dynamische Abfrage verwendet, wird für jede Abfrage eine zwischengespeicherte Ansicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d16f-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d16f-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8d16f-142">Notes to callers</span></span>

<span data-ttu-id="8d16f-143">Um die aktuelle Einschränkung zu verwerfen, ohne eine neue zu erstellen, übergeben Sie NULL in  _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="8d16f-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="8d16f-144">Wenn ein weiterer asynchroner Tabellenaufruf ausgeführt wird, wodurch **Restrict** MAPI_E_BUSY zurück gibt, können Sie [IMAPITable::Abort](imapitable-abort.md) aufrufen, um den Anruf zu beenden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="8d16f-145">**Restrict** wird synchron ausgeführt, es sei denn, Sie legen eines der Flags ein.</span><span class="sxs-lookup"><span data-stu-id="8d16f-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="8d16f-146">Wenn Sie das TBL_BATCH festlegen, verschiebt **Restrict** die Auswertung der Einschränkung, es sei denn, Sie fordern die Daten an.</span><span class="sxs-lookup"><span data-stu-id="8d16f-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="8d16f-147">Wenn das TBL_ASYNC festgelegt ist, wird **Restrict** asynchron betrieben und möglicherweise vor Abschluss des Vorgangs zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8d16f-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="8d16f-148">Alle Lesezeichen für eine Tabelle werden verworfen, wenn ein Aufruf von **Restrict** erfolgt, und BOOKMARK_CURRENT, die aktuelle Cursorposition, wird auf den Anfang der Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d16f-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="8d16f-149">Wenn Sie versuchen, einer Eigenschaft, die nicht im Spaltensatz der Tabelle enthalten ist, eine Eigenschaftseinschränkung aufzuerzwingen, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8d16f-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="8d16f-150">Wenn Sie nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, kombinieren Sie die Eigenschaftseinschränkung mit einer vorhandenen Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="8d16f-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="8d16f-151">Mit der vorhandenen Einschränkung wird überprüft, ob die Eigenschaft vorhanden ist, bevor versucht wird, die Eigenschaftseinschränkung zu verhängen.</span><span class="sxs-lookup"><span data-stu-id="8d16f-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="8d16f-152">Erwarten Sie keine Tabellenbenachrichtigung für eine Zeile, die aufgrund einer Einschränkung aus einer Tabelle gefiltert wurde.</span><span class="sxs-lookup"><span data-stu-id="8d16f-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8d16f-153">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8d16f-153">MFCMAPI reference</span></span>

<span data-ttu-id="8d16f-154">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8d16f-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8d16f-155">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8d16f-155">**File**</span></span>|<span data-ttu-id="8d16f-156">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8d16f-156">**Function**</span></span>|<span data-ttu-id="8d16f-157">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8d16f-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d16f-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8d16f-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8d16f-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="8d16f-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="8d16f-160">MFCMAPI verwendet die **IMAPITable::Restrict-Methode,** um eine Einschränkung für eine Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d16f-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d16f-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d16f-161">See also</span></span>



[<span data-ttu-id="8d16f-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="8d16f-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="8d16f-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="8d16f-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="8d16f-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="8d16f-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="8d16f-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="8d16f-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="8d16f-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8d16f-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="8d16f-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d16f-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="8d16f-168">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8d16f-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

