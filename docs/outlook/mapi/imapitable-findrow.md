---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429572"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="34014-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="34014-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="34014-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34014-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34014-105">Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht, und verschiebt den Cursor in diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="34014-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="34014-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34014-106">Parameters</span></span>

 <span data-ttu-id="34014-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="34014-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="34014-108">[in] Ein Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Suchkriterien beschreibt.</span><span class="sxs-lookup"><span data-stu-id="34014-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="34014-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="34014-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="34014-110">[in] Eine Textmarke, die die Zeile identifiziert, in der **FindRow** mit der Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="34014-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="34014-111">Eine Textmarke kann mit der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt werden, oder einer der folgenden vordefinierten Werte kann übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="34014-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="34014-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="34014-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="34014-113">Sucht vom Anfang der Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="34014-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="34014-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="34014-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="34014-115">Sucht aus der Zeile in der Tabelle, in der sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="34014-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="34014-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="34014-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="34014-117">Sucht am Ende der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="34014-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="34014-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34014-118">_ulFlags_</span></span>
  
> <span data-ttu-id="34014-119">[in] Eine Bitmaske mit Flags, die die Richtung der Suche steuert.</span><span class="sxs-lookup"><span data-stu-id="34014-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="34014-120">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="34014-120">The following flag can be set:</span></span>
    
<span data-ttu-id="34014-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="34014-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="34014-122">Sucht rückwärts aus der zeile, die durch die Textmarke identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="34014-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34014-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34014-123">Return value</span></span>

<span data-ttu-id="34014-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="34014-124">S_OK</span></span> 
  
> <span data-ttu-id="34014-125">Der Findvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="34014-125">The find operation was successful.</span></span>
    
<span data-ttu-id="34014-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="34014-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="34014-127">Die Textmarke im  _BkOrigin-Parameter_ ist ungültig, weil sie entfernt wurde oder weil sie über die letzte angeforderte Zeile hinaus liegt.</span><span class="sxs-lookup"><span data-stu-id="34014-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="34014-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="34014-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="34014-129">Es wurden keine Zeilen gefunden, die der Einschränkung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="34014-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="34014-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="34014-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="34014-131">Der Aufruf ist erfolgreich, aber die im Vorgang verwendete Textmarke wird nicht mehr in derselben Zeile wie bei der letzten Verwendung festgelegt. Wenn die Textmarke nicht verwendet wurde, befindet sie sich nicht mehr an derselben Position wie beim Erstellen.</span><span class="sxs-lookup"><span data-stu-id="34014-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="34014-132">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="34014-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="34014-133">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="34014-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="34014-134">Weitere [Informationen finden Sie unter Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="34014-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34014-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34014-135">Remarks</span></span>

<span data-ttu-id="34014-136">Die **IMAPITable::FindRow-Methode** sucht die erste Zeile in der Tabelle, um mit einer Reihe von Suchkriterien zu übereinstimmen, die in der **SRestriction-Struktur** beschrieben sind, auf die der  _lpRestriction-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="34014-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="34014-137">In der Regel **sucht FindRow** von der angegebenen Textmarke nach vorn.</span><span class="sxs-lookup"><span data-stu-id="34014-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="34014-138">Der Aufrufer kann festlegen, dass die Suche von der Textmarke rückwärts bewegt wird, indem DIR_BACKWARD im  _ulFlags-Parameter festgelegt_ wird.</span><span class="sxs-lookup"><span data-stu-id="34014-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="34014-139">Das Vorwärtssuchen beginnt mit der aktuellen Textmarke. Die Rückwärtssuche beginnt in der Zeile vor der Textmarke.</span><span class="sxs-lookup"><span data-stu-id="34014-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="34014-140">Die Endposition der Suche befindet sich kurz vor der ersten Zeile, die die Einschränkung erfüllt hat.</span><span class="sxs-lookup"><span data-stu-id="34014-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="34014-141">Wenn die Zeile, auf die die Textmarke im  _BkOrigin-Parameter_ verweist, nicht mehr in der Tabelle vorhanden ist und die Tabelle keine neue Position für die Textmarke einrichten kann, gibt **FindRow** MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="34014-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="34014-142">Wenn die Zeile, auf die  _BkOrigin_ verweist, nicht mehr vorhanden ist und die Tabelle eine neue Position für die Textmarke einrichten kann, gibt **FindRow** MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="34014-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="34014-143">Wenn die in  _BkOrigin_ übergebene Textmarke entweder BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND zurück, wenn keine übereinstimmende Zeile gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="34014-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="34014-144">Wenn die in  _BkOrigin_ verwendete Textmarke BOOKMARK_CURRENT ist, kann **FindRow** MAPI_W_POSITION_CHANGED aber nicht MAPI_E_INVALID_BOOKMARK zurück, da immer eine aktuelle Cursorposition besteht.</span><span class="sxs-lookup"><span data-stu-id="34014-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="34014-145">Die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaftsspalte ist für alle Tabellen erforderlich, und alle Implementierungen von **FindRow** sind erforderlich, um Aufrufe zu unterstützen, die eine Zeile basierend auf PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="34014-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="34014-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="34014-146">Notes to implementers</span></span>

<span data-ttu-id="34014-147">Der Typ der Präfixsuche, die **von FindRow** ausgeführt wird, ist nur hilfreich, wenn die Suche dieselbe Richtung wie die Tabellenorganisation hat.</span><span class="sxs-lookup"><span data-stu-id="34014-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="34014-148">Um das erforderliche Verhalten zu erreichen, sollte  die vergleichsfunktion, die von der RELOP_GE in der Eigenschaftseinschränkungsstruktur übergeben wird, dieselbe Vergleichsfunktion sein, auf der die Tabellensortierungsreihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="34014-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="34014-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="34014-149">Notes to callers</span></span>

<span data-ttu-id="34014-150">Sie können **FindRow verwenden,** um einen Bildlauf basierend auf vom Benutzer ein eingabebasierten Zeichenfolgen zu unterstützen, insbesondere in Listenfeldern innerhalb von Adressdialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="34014-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="34014-151">Bei dieser Art von Bildlauf geben Benutzer schrittweise längere Präfixe eines gewünschten Zeichenfolgenwerts ein, und Sie können regelmäßig einen **FindRow-Aufruf** durchführen, um zur ersten Zeile zu springen, die dem Präfix entspricht.</span><span class="sxs-lookup"><span data-stu-id="34014-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="34014-152">Welche Richtung der Cursor springt, hängt davon ab, in welche Richtung die Suche ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34014-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="34014-153">Um **FindRow verwenden zu** können, muss eine Textmarke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="34014-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="34014-154">Die Zeichenfolgensuche kann von beliebigen Textmarken stammen, einschließlich der vordefinierten Lesezeichen, die die aktuelle Position sowie den Anfang und das Ende der Tabelle angeben.</span><span class="sxs-lookup"><span data-stu-id="34014-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="34014-155">Wenn eine große Anzahl von Zeilen in der Tabelle vorhanden ist, kann der Suchvorgang langsam sein.</span><span class="sxs-lookup"><span data-stu-id="34014-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="34014-156">Verwenden Sie eine Einschränkung, um ein Zeichenfolgenpräfix für den Bildlauf wie folgt zu finden.</span><span class="sxs-lookup"><span data-stu-id="34014-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="34014-157">Übergeben Sie für die Vorwärtssuche für eine Spalte, die in aufsteigender Reihenfolge sortiert ist, und für die Rückwärtssuche in einer Spalte, die in absteigender Reihenfolge sortiert ist, eine Eigenschaftseinschränkungsstruktur im _lpRestriction-Parameter_ mit der Beziehung **RELOP_GE** und dem entsprechenden Eigenschaftentag und Präfix, indem Sie das _Formattag_ _GE-Präfix verwenden._ </span><span class="sxs-lookup"><span data-stu-id="34014-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="34014-158">Weitere Informationen zum Verwenden von Einschränkungsstrukturen zum Angeben eines Filters finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="34014-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="34014-159">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="34014-159">MFCMAPI reference</span></span>

<span data-ttu-id="34014-160">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="34014-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="34014-161">**Datei**</span><span class="sxs-lookup"><span data-stu-id="34014-161">**File**</span></span>|<span data-ttu-id="34014-162">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="34014-162">**Function**</span></span>|<span data-ttu-id="34014-163">**Comment**</span><span class="sxs-lookup"><span data-stu-id="34014-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34014-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="34014-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="34014-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="34014-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="34014-166">MFCMAPI verwendet die **IMAPITable::FindRow-Methode,** um Zeilen zu finden, die einer Einschränkung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="34014-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34014-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34014-167">See also</span></span>



[<span data-ttu-id="34014-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="34014-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="34014-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="34014-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="34014-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="34014-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="34014-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34014-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="34014-172">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="34014-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

