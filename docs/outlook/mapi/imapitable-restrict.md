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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792478"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="308b3-103">Methode IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="308b3-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="308b3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="308b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="308b3-105">Wendet einen Filter auf eine Tabelle, reduzieren die Zeile festgelegt, um nur die Zeilen, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="308b3-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="308b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="308b3-106">Parameters</span></span>

 <span data-ttu-id="308b3-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="308b3-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="308b3-108">[in] Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Bedingungen des Filters definieren.</span><span class="sxs-lookup"><span data-stu-id="308b3-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="308b3-109">Übergeben von NULL im Parameter _LpRestriction_ entfernt den aktuellen Filter.</span><span class="sxs-lookup"><span data-stu-id="308b3-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="308b3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="308b3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="308b3-111">[in] Bitmaske aus Flags, die den Zeitpunkt des Vorgangs Einschränkung steuert.</span><span class="sxs-lookup"><span data-stu-id="308b3-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="308b3-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="308b3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="308b3-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="308b3-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="308b3-114">Die Operation asynchron startet und gibt vor dem Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="308b3-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="308b3-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="308b3-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="308b3-116">Bewertung des Filters verzögert, bis die Daten in der Tabelle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="308b3-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="308b3-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="308b3-117">Return value</span></span>

<span data-ttu-id="308b3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="308b3-118">S_OK</span></span> 
  
> <span data-ttu-id="308b3-119">Der Filter wurde erfolgreich angewendet.</span><span class="sxs-lookup"><span data-stu-id="308b3-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="308b3-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="308b3-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="308b3-121">Ein anderer Vorgang wird ausgeführt, die verhindert, den Einschränkung Vorgang gestartet wird dass.</span><span class="sxs-lookup"><span data-stu-id="308b3-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="308b3-122">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="308b3-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="308b3-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="308b3-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="308b3-124">Die Tabelle kann nicht den Vorgang ausgeführt werden, da der bestimmte Filter auf das durch den Parameter _LpRestriction_ zu kompliziert ist.</span><span class="sxs-lookup"><span data-stu-id="308b3-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="308b3-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="308b3-125">Remarks</span></span>

<span data-ttu-id="308b3-126">Die **Methode IMAPITable:: Restrict** -Methode stellt eine Einschränkung oder ein Filter für eine Tabelle her.</span><span class="sxs-lookup"><span data-stu-id="308b3-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="308b3-127">Wenn eine vorherige Einschränkung vorhanden ist, es verworfen, und die neue Datenbank angewendet.</span><span class="sxs-lookup"><span data-stu-id="308b3-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="308b3-128">Anwenden einer Einschränkung hat keine Auswirkung auf die zugrunde liegenden Daten einer Tabelle; Diese ändert der Ansicht einfach durch Beschränken der Zeilen, die abgerufen werden können, um Zeilen mit Daten, die die Einschränkung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="308b3-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="308b3-129">Es gibt verschiedene Arten von Einschränkungen, jeweils mit einer anderen Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="308b3-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="308b3-130">Die [SRestriction](srestriction.md) -Datenstruktur enthält zwei Elemente: ein Wert, der den Typ der Einschränkung und die spezifische Struktur für dieses Typs angibt.</span><span class="sxs-lookup"><span data-stu-id="308b3-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="308b3-131">Benachrichtigungen für Zeilen der Tabelle, die durch Aufrufe **Restrict** ausgeblendet sind, werden nie generiert.</span><span class="sxs-lookup"><span data-stu-id="308b3-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="308b3-132">Eine eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="308b3-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="308b3-133">Eine mehrwertige Eigenschaft in einer eigenschaftseinschränkung verwendet werden muss die MVI_FLAG gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="308b3-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="308b3-134">Wenn dieses Flag festgelegt ist, wird es als ein solcher geordnete Tupel behandelt.</span><span class="sxs-lookup"><span data-stu-id="308b3-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="308b3-135">Ein Vergleich von zwei mehrwertige Spalten werden die Spalte Elemente in der Reihenfolge, reporting die Beziehung der Spalten auf dem ersten Zeichen verglichen.</span><span class="sxs-lookup"><span data-stu-id="308b3-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="308b3-136">Gleichheit wird nur zurückgegeben, wenn die Spalten im Vergleich dieselben Werte wie in der gleichen Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="308b3-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="308b3-137">Wenn eine Spalte weniger Werte als die andere verfügt, kann die gemeldete Beziehung, die über einen null-Wert auf den anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="308b3-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="308b3-138">Weitere Informationen zu Beschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="308b3-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="308b3-139">Wenn Sie dynamische Abfragen von Daten auf dem Server erstellen, verwenden Sie anstelle der **Restrict** -Methode und die **QueryRows** -Methode zusammen mit **FindRow** -Methode.</span><span class="sxs-lookup"><span data-stu-id="308b3-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="308b3-140">Die **Restrict** -Methode erstellt eine zwischengespeicherte Ansicht, die verwendet wird, für alle Nachrichten, die in den Basisordner geändert oder hinzugefügt ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="308b3-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="308b3-141">Wenn eine Clientanwendung die **Restrict** -Methode für jede dynamische Abfrage verwendet wird, wird eine zwischengespeicherte Ansicht für jede Abfrage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="308b3-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="308b3-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="308b3-142">Notes to callers</span></span>

<span data-ttu-id="308b3-143">Um der aktuellen Einschränkung verwerfen, ohne einen neuen Anwendungspool erstellen, übergeben Sie NULL _LpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="308b3-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="308b3-144">Wenn eine andere asynchrone Tabelle Anruf ausgeführt wird, können, auf dem Sie [IMAPITable::Abort](imapitable-abort.md) , um den Anruf zu beenden anrufen **Restrict** zurückzugebenden MAPI_E_BUSY, verursacht.</span><span class="sxs-lookup"><span data-stu-id="308b3-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="308b3-145">**Restrict** arbeitet synchron, es sei denn, Sie eines der Flags festlegen.</span><span class="sxs-lookup"><span data-stu-id="308b3-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="308b3-146">Wenn Sie das TBL_BATCH-Flag festlegen, verschiebt **Restrict** die Auswertung der Einschränkung, es sei denn, Sie die Daten anfordern.</span><span class="sxs-lookup"><span data-stu-id="308b3-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="308b3-147">Wenn das Flag TBL_ASYNC festgelegt ist, arbeitet **Restrict**asynchron potenziell vor dem Abschluss des Vorgangs zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="308b3-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="308b3-148">Wenn **Restrict** wird aufgerufen, und BOOKMARK_CURRENT der aktuellen Cursorposition an den Anfang der Tabelle festgelegt ist, werden alle Textmarken für eine Tabelle verworfen.</span><span class="sxs-lookup"><span data-stu-id="308b3-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="308b3-149">Wenn Sie versuchen, eine eigenschaftseinschränkung für eine Eigenschaft zugrunde liegen, die nicht in der Tabelle Spalte Set ist, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="308b3-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="308b3-150">Wenn Sie nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, Kombinieren der eigenschaftseinschränkung mit einer Einschränkung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="308b3-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="308b3-151">Die Einschränkung überprüft, ob der-Eigenschaft, bevor Sie versuchen, die eigenschaftseinschränkung bedingen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="308b3-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="308b3-152">Davon ausgehen, dass eine Benachrichtigung zu erhalten Tabelle in einer Zeile, die gefiltert wurde aus einer Tabelle aufgrund einer Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="308b3-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="308b3-153">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="308b3-153">MFCMAPI reference</span></span>

<span data-ttu-id="308b3-154">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="308b3-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="308b3-155">**Datei**</span><span class="sxs-lookup"><span data-stu-id="308b3-155">**File**</span></span>|<span data-ttu-id="308b3-156">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="308b3-156">**Function**</span></span>|<span data-ttu-id="308b3-157">**Comment**</span><span class="sxs-lookup"><span data-stu-id="308b3-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="308b3-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="308b3-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="308b3-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="308b3-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="308b3-160">MFCMAPI (engl.) verwendet die **Methode IMAPITable:: Restrict** -Methode, um eine Einschränkung für eine Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="308b3-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="308b3-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="308b3-161">See also</span></span>



[<span data-ttu-id="308b3-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="308b3-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="308b3-163">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="308b3-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="308b3-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="308b3-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="308b3-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="308b3-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="308b3-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="308b3-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="308b3-167">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="308b3-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="308b3-168">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="308b3-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

