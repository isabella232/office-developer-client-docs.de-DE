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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329080"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="a7020-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="a7020-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="a7020-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7020-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7020-105">Sucht die nächste Zeile in einer Tabelle, die bestimmten Suchkriterien entspricht, und verschiebt den Cursor zu dieser Zeile.</span><span class="sxs-lookup"><span data-stu-id="a7020-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a7020-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7020-106">Parameters</span></span>

 <span data-ttu-id="a7020-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="a7020-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="a7020-108">in Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a7020-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="a7020-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="a7020-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="a7020-110">in Eine Textmarke, die die Zeile identifiziert, in der **FindRow** Ihre Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="a7020-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="a7020-111">Eine Textmarke kann mit der [IMAPITable:: CreateBookMark](imapitable-createbookmark.md) -Methode oder einem der folgenden vordefinierten Werte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a7020-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="a7020-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="a7020-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="a7020-113">Sucht vom Anfang der Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a7020-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="a7020-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="a7020-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="a7020-115">Sucht aus der Zeile in der Tabelle, in der sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="a7020-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="a7020-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="a7020-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="a7020-117">Sucht am Ende der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a7020-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="a7020-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7020-118">_ulFlags_</span></span>
  
> <span data-ttu-id="a7020-119">in Eine Bitmaske von Flags, die die Richtung der Suche steuert.</span><span class="sxs-lookup"><span data-stu-id="a7020-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="a7020-120">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a7020-120">The following flag can be set:</span></span>
    
<span data-ttu-id="a7020-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="a7020-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="a7020-122">Sucht aus der durch die Textmarke identifizierten Zeile rückwärts.</span><span class="sxs-lookup"><span data-stu-id="a7020-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7020-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7020-123">Return value</span></span>

<span data-ttu-id="a7020-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7020-124">S_OK</span></span> 
  
> <span data-ttu-id="a7020-125">Der Suchvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a7020-125">The find operation was successful.</span></span>
    
<span data-ttu-id="a7020-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="a7020-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="a7020-127">Die Textmarke im _BkOrigin_ -Parameter ist ungültig, da Sie entfernt wurde oder über die letzte angeforderte Zeile hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="a7020-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="a7020-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a7020-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a7020-129">Es wurden keine Zeilen gefunden, die mit der Einschränkung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7020-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="a7020-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="a7020-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="a7020-131">Der Aufruf wurde erfolgreich ausgeführt, aber die im Vorgang verwendete Textmarke wird nicht mehr in derselben Zeile festgelegt wie bei der letzten Verwendung; Wenn die Textmarke nicht verwendet wurde, befindet Sie sich nicht mehr in derselben Position wie bei ihrer Erstellung.</span><span class="sxs-lookup"><span data-stu-id="a7020-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="a7020-132">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a7020-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a7020-133">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="a7020-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a7020-134">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a7020-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7020-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7020-135">Remarks</span></span>

<span data-ttu-id="a7020-136">Die **IMAPITable:: FindRow** -Methode sucht die erste Zeile in der Tabelle, die einer Reihe von Suchkriterien entspricht, die in der **SRestriction** -Struktur beschrieben ist, auf die durch den _lpRestriction_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a7020-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="a7020-137">In der Regel sucht **FindRow** nach vorn aus der angegebenen Textmarke.</span><span class="sxs-lookup"><span data-stu-id="a7020-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="a7020-138">Der Anrufer kann festlegen, dass die Suche rückwärts aus der Textmarke verschoben wird, indem das DIR_BACKWARD-Flag im _ulFlags_ -Parameter festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a7020-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a7020-139">Die Vorwärtssuche beginnt mit der aktuellen Textmarke; die Rückwärtssuche beginnt von der Zeile vor der Textmarke.</span><span class="sxs-lookup"><span data-stu-id="a7020-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="a7020-140">Die Endposition der Suche ist unmittelbar vor der ersten gefundenen Zeile, die die Einschränkung erfüllt hat.</span><span class="sxs-lookup"><span data-stu-id="a7020-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="a7020-141">Wenn die Zeile, auf die durch die Textmarke im _BkOrigin_ -Parameter verwiesen wird, in der Tabelle nicht mehr vorhanden ist und die Tabelle keine neue Position für die Textmarke festlegen kann, gibt **FindRow** MAPI_E_INVALID_BOOKMARK zurück.</span><span class="sxs-lookup"><span data-stu-id="a7020-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="a7020-142">Wenn die Zeile, auf die durch _BkOrigin_ verwiesen wird, nicht mehr vorhanden ist und die Tabelle eine neue Position für die Textmarke festlegen kann, gibt **FindRow** MAPI_W_POSITION_CHANGED zurück.</span><span class="sxs-lookup"><span data-stu-id="a7020-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="a7020-143">Wenn die in _BkOrigin_ übergebene Textmarke entweder BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND zurück, wenn keine übereinstimmende Zeile gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="a7020-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="a7020-144">Wenn die in _BkOrigin_ verwendete Textmarke BOOKMARK_CURRENT ist, kann **FindRow** MAPI_W_POSITION_CHANGED zurückgeben, aber nicht MAPI_E_INVALID_BOOKMARK, da immer eine aktuelle Cursor Position vorliegt.</span><span class="sxs-lookup"><span data-stu-id="a7020-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="a7020-145">Die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaftsspalte ist für alle Tabellen erforderlich, und alle Implementierungen von **FindRow** sind erforderlich, um Aufrufe zu unterstützen, die eine Zeile auf der Grundlage von PR_INSTANCE_KEY suchen.</span><span class="sxs-lookup"><span data-stu-id="a7020-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a7020-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="a7020-146">Notes to implementers</span></span>

<span data-ttu-id="a7020-147">Der Typ der durch **FindRow** durchgeführten Präfixsuche ist nur nützlich, wenn die Suche dieselbe Richtung hat wie die Tabellenorganisation.</span><span class="sxs-lookup"><span data-stu-id="a7020-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="a7020-148">Um das erforderliche Verhalten zu erreichen, sollte die Vergleichsfunktion, die von der **RELOP_GE** , die in der Eigenschafts Einschränkungs Struktur übergeben wird, die gleiche Vergleichsfunktion sein, auf der die Tabellen Sortierreihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="a7020-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a7020-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a7020-149">Notes to callers</span></span>

<span data-ttu-id="a7020-150">Sie können **FindRow** verwenden, um den Bildlauf basierend auf vom Benutzer eingegebenen Zeichenfolgen zu unterstützen, insbesondere in Listenfeldern in Adress Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="a7020-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="a7020-151">Bei diesem Bildlauftyp geben Benutzer progressiv längere Präfixe eines gewünschten Zeichenfolgenwerts ein, und Sie können in regelmäßigen Abständen einen **FindRow** -Aufruf ausgeben, um zur ersten Zeile zu wechseln, die mit dem Präfix übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a7020-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="a7020-152">Welche Richtung der Cursor springt, hängt davon ab, in welcher Richtung die Suche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7020-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="a7020-153">Um **FindRow**zu verwenden, muss eine Textmarke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7020-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="a7020-154">Die Zeichenfolgensuche kann von einer beliebigen Textmarke stammen, einschließlich der vordefinierten Lesezeichen, die die aktuelle Position und den Anfang und das Ende der Tabelle angeben.</span><span class="sxs-lookup"><span data-stu-id="a7020-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="a7020-155">Wenn eine hohe Anzahl von Zeilen in der Tabelle vorhanden ist, kann der Suchvorgang langsam sein.</span><span class="sxs-lookup"><span data-stu-id="a7020-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="a7020-156">Verwenden Sie eine Einschränkung, um nach einem Zeichenfolgen Präfix zum Scrollen wie folgt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a7020-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="a7020-157">Zum Weiterleiten der Suche in einer Spalte in aufsteigender Reihenfolge und zur Rückwärtssuche für eine in absteigender Reihenfolge sortierte Spalte übergeben Sie eine Eigenschafts Einschränkungs Struktur im _lpRestriction_ -Parameter mit der Relation **RELOP_GE** und dem entsprechenden Property-Tag und Prefix, wobei das Format- _Tag_ **ge** - _Präfix_verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7020-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="a7020-158">Weitere Informationen zur Verwendung von Einschränkungs Strukturen zum Angeben eines Filters finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a7020-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a7020-159">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a7020-159">MFCMAPI reference</span></span>

<span data-ttu-id="a7020-160">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a7020-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a7020-161">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a7020-161">**File**</span></span>|<span data-ttu-id="a7020-162">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a7020-162">**Function**</span></span>|<span data-ttu-id="a7020-163">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a7020-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7020-164">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="a7020-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="a7020-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="a7020-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="a7020-166">MFCMAPI verwendet die **IMAPITable:: FindRow** -Methode, um Zeilen zu finden, die mit einer Einschränkung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7020-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7020-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7020-167">See also</span></span>



[<span data-ttu-id="a7020-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="a7020-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="a7020-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="a7020-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="a7020-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a7020-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="a7020-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7020-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="a7020-172">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a7020-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

