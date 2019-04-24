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
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328847"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="1f54b-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="1f54b-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="1f54b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f54b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f54b-105">Wendet einen Filter auf eine Tabelle an, wobei der Zeilensatz nur auf die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1f54b-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1f54b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f54b-106">Parameters</span></span>

 <span data-ttu-id="1f54b-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="1f54b-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="1f54b-108">in Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Bedingungen des Filters definiert.</span><span class="sxs-lookup"><span data-stu-id="1f54b-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="1f54b-109">Durch das Übergeben von NULL im _lpRestriction_ -Parameter wird der aktuelle Filter entfernt.</span><span class="sxs-lookup"><span data-stu-id="1f54b-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="1f54b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f54b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1f54b-111">in Bitmaske von Flags, die das Timing des Einschränkungs Vorgangs steuert.</span><span class="sxs-lookup"><span data-stu-id="1f54b-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="1f54b-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1f54b-112">The following flags can be set:</span></span>
    
<span data-ttu-id="1f54b-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="1f54b-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="1f54b-114">Startet den Vorgang asynchron und gibt vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="1f54b-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="1f54b-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="1f54b-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="1f54b-116">Verzögert die Auswertung des Filters, bis die Daten in der Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1f54b-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f54b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f54b-117">Return value</span></span>

<span data-ttu-id="1f54b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f54b-118">S_OK</span></span> 
  
> <span data-ttu-id="1f54b-119">Der Filter wurde erfolgreich angewendet.</span><span class="sxs-lookup"><span data-stu-id="1f54b-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="1f54b-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1f54b-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1f54b-121">Ein anderer Vorgang wird ausgeführt, der verhindert, dass der Einschränkungs Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1f54b-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="1f54b-122">Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f54b-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="1f54b-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="1f54b-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="1f54b-124">Die Tabelle kann den Vorgang nicht ausführen, da der bestimmte Filter, auf den durch den _lpRestriction_ -Parameter verwiesen wird, zu kompliziert ist.</span><span class="sxs-lookup"><span data-stu-id="1f54b-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1f54b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f54b-125">Remarks</span></span>

<span data-ttu-id="1f54b-126">Die **IMAPITable:: Restrict** -Methode richtet eine Einschränkung oder einen Filter für eine Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="1f54b-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="1f54b-127">Wenn es eine frühere Einschränkung gibt, wird sie verworfen und die neue angewendet.</span><span class="sxs-lookup"><span data-stu-id="1f54b-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="1f54b-128">Das Anwenden einer Einschränkung hat keine Auswirkungen auf die zugrunde liegenden Daten einer Tabelle; Es ändert lediglich die Ansicht, indem die Zeilen eingeschränkt werden, die in Zeilen mit Daten abgerufen werden können, die die Einschränkung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1f54b-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="1f54b-129">Es gibt verschiedene Arten von Einschränkungen, die jeweils mit einer anderen Struktur beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1f54b-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="1f54b-130">Die [SRestriction](srestriction.md) -Struktur enthält zwei Elemente: ein Wert, der den Typ der Einschränkung und die spezifische Struktur angibt, die für diesen Typ gilt.</span><span class="sxs-lookup"><span data-stu-id="1f54b-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="1f54b-131">Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von **Restrict** ausgeblendet werden, werden nie generiert.</span><span class="sxs-lookup"><span data-stu-id="1f54b-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="1f54b-132">Eine Eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1f54b-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="1f54b-133">Für eine mehrwertige Eigenschaft, die in einer Eigenschaftseinschränkung verwendet werden soll, muss das MVI_FLAG-Flag festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="1f54b-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="1f54b-134">Wenn dieses Flag nicht festgelegt ist, wird es als vollständig geordnetes Tupel behandelt.</span><span class="sxs-lookup"><span data-stu-id="1f54b-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="1f54b-135">Bei einem Vergleich zwischen zwei mehrwertigen Spalten werden die Spaltenelemente in der Reihenfolge verglichen, wobei die Relation der Spalten bei der ersten Ungleichung gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="1f54b-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="1f54b-136">Gleichheit wird nur zurückgegeben, wenn die verglichenen Spalten die gleichen Werte in derselben Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f54b-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="1f54b-137">Wenn eine Spalte weniger Werte als die andere hat, ist die berichtete Relation die eines NULL-Werts für den anderen Wert.</span><span class="sxs-lookup"><span data-stu-id="1f54b-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="1f54b-138">Weitere Informationen zu Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1f54b-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f54b-139">Wenn Sie dynamische Abfragen zum Suchen nach Daten auf dem Server erstellen, verwenden Sie die **FindRow** -Methode, anstatt die **Restrict** -Methode und die **QueryRows** -Methode zusammen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f54b-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="1f54b-140">Die **Restrict** -Methode erstellt eine zwischengespeicherte Ansicht, die zum Auswerten aller Nachrichten verwendet wird, die im Basisordner hinzugefügt oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="1f54b-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="1f54b-141">Wenn eine Clientanwendung die **Restrict** -Methode für jede dynamische Abfrage verwendet, wird für jede Abfrage eine zwischengespeicherte Ansicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f54b-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1f54b-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1f54b-142">Notes to callers</span></span>

<span data-ttu-id="1f54b-143">Um die aktuelle Einschränkung zu verwerfen, ohne eine neue zu erstellen, müssen Sie in _lpRestriction_den Wert NULL überschreiten.</span><span class="sxs-lookup"><span data-stu-id="1f54b-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="1f54b-144">Wenn ein anderer asynchroner Tabellen Aufruf ausgeführt wird, wodurch **Restrict** MAPI_E_BUSY zurückgegeben wird, können Sie [IMAPITable:: Abort](imapitable-abort.md) aufrufen, um den Anruf zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1f54b-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="1f54b-145">**Restrict** arbeitet synchron, es sei denn, Sie legen eine der Flags fest.</span><span class="sxs-lookup"><span data-stu-id="1f54b-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="1f54b-146">Wenn Sie das TBL_BATCH-Flag festlegen, verschiebt **Restrict** die Bewertung der Einschränkung, es sei denn, Sie fordern die Daten an.</span><span class="sxs-lookup"><span data-stu-id="1f54b-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="1f54b-147">Wenn das TBL_ASYNC-Flag festgelegt ist, wird **Restrict**asynchron ausgeführt, was möglicherweise vor dem Abschluss des Vorgangs zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f54b-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="1f54b-148">Alle Lesezeichen für eine Tabelle werden verworfen, wenn ein Aufruf von **Restrict** ausgeführt wird und BOOKMARK_CURRENT, die aktuelle Cursorposition, auf den Anfang der Tabelle festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1f54b-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="1f54b-149">Wenn Sie versuchen, eine Eigenschaftseinschränkung für eine Eigenschaft aufzuerlegen, die nicht im Spaltensatz der Tabelle enthalten ist, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1f54b-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="1f54b-150">Wenn Sie nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, kombinieren Sie die Eigenschaftseinschränkung mit einer EXISTS-Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="1f54b-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="1f54b-151">Die EXISTS-Einschränkung überprüft, ob die Eigenschaft vorhanden ist, bevor Sie versuchen, die Eigenschaftseinschränkung aufzuzwingen.</span><span class="sxs-lookup"><span data-stu-id="1f54b-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="1f54b-152">Erwarten Sie nicht, dass Sie eine Tabellenbenachrichtigung für eine Zeile erhalten, die aufgrund einer Einschränkung aus einer Tabelle gefiltert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f54b-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1f54b-153">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1f54b-153">MFCMAPI reference</span></span>

<span data-ttu-id="1f54b-154">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1f54b-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1f54b-155">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1f54b-155">**File**</span></span>|<span data-ttu-id="1f54b-156">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1f54b-156">**Function**</span></span>|<span data-ttu-id="1f54b-157">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1f54b-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f54b-158">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="1f54b-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1f54b-159">CContentsTableListCtrl:: ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="1f54b-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="1f54b-160">MFCMAPI verwendet die **IMAPITable:: Restrict** -Methode, um eine Einschränkung für eine Tabelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1f54b-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f54b-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f54b-161">See also</span></span>



[<span data-ttu-id="1f54b-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="1f54b-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="1f54b-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="1f54b-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="1f54b-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="1f54b-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="1f54b-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1f54b-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1f54b-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="1f54b-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="1f54b-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f54b-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="1f54b-168">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1f54b-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

