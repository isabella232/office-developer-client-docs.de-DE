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
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792455"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="303a1-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="303a1-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="303a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="303a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="303a1-105">Findet die nächste Zeile in einer Tabelle, die bestimmte Suchkriterien entspricht, und verschiebt den Cursor auf diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="303a1-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="303a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="303a1-106">Parameters</span></span>

 <span data-ttu-id="303a1-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="303a1-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="303a1-108">[in] Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die den Suchkriterien beschreibt.</span><span class="sxs-lookup"><span data-stu-id="303a1-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="303a1-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="303a1-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="303a1-110">[in] Eine Textmarke, identifiziert die Zeile, in dem **FindRow** die Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="303a1-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="303a1-111">Eine Textmarke kann mithilfe der [IMAPITable::CreateBookmark](imapitable-createbookmark.md) -Methode erstellt werden, oder eine der folgenden vordefinierten Werte übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="303a1-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="303a1-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="303a1-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="303a1-113">Sucht vom Beginn der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="303a1-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="303a1-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="303a1-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="303a1-115">Sucht aus der Zeile in der Tabelle, in dem sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="303a1-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="303a1-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="303a1-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="303a1-117">Sucht vom Ende der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="303a1-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="303a1-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="303a1-118">_ulFlags_</span></span>
  
> <span data-ttu-id="303a1-119">[in] Eine Bitmaske aus Flags, die die Richtung der Suche steuert.</span><span class="sxs-lookup"><span data-stu-id="303a1-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="303a1-120">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="303a1-120">The following flag can be set:</span></span>
    
<span data-ttu-id="303a1-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="303a1-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="303a1-122">Sucht rückwärts aus der Zeile, die durch die Textmarke identifiziert.</span><span class="sxs-lookup"><span data-stu-id="303a1-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="303a1-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="303a1-123">Return value</span></span>

<span data-ttu-id="303a1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="303a1-124">S_OK</span></span> 
  
> <span data-ttu-id="303a1-125">Der Suchvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="303a1-125">The find operation was successful.</span></span>
    
<span data-ttu-id="303a1-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="303a1-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="303a1-127">Die Textmarke im _BkOrigin_ -Parameter ist ungültig oder, da es entfernt wurde, da sie nach der letzten Zeile angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="303a1-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="303a1-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="303a1-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="303a1-129">Es wurden keine Zeilen gefunden, die mit die Einschränkung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="303a1-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="303a1-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="303a1-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="303a1-131">Der Aufruf war erfolgreich, aber die Textmarke, die in den Vorgang verwendet wird nicht mehr in der gleichen Zeile als bei der letzten Verwendung festgelegt; Wenn die Textmarke nicht verwendet wurden, ist es nicht mehr in derselben Position wie bei der es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="303a1-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="303a1-132">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="303a1-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="303a1-133">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="303a1-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="303a1-134">Finden Sie unter [Verwendung von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="303a1-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="303a1-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="303a1-135">Remarks</span></span>

<span data-ttu-id="303a1-136">Die **IMAPITable** -Methode sucht nach der ersten Zeile in der Tabelle auf eine Gruppe von in der auf das durch den Parameter _LpRestriction_ **SRestriction** -Struktur beschriebenen Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="303a1-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="303a1-137">In der Regel sucht **FindRow** weiterleiten aus der angegebenen Textmarke.</span><span class="sxs-lookup"><span data-stu-id="303a1-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="303a1-138">Der Aufrufer kann die Suche von der Bookmark rückwärts, indem das DIR_BACKWARD Flag im _UlFlags_ -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="303a1-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="303a1-139">Suche vorwärts wird von der aktuellen Bookmark gestartet. sucht rückwärts startet aus der Zeile vor der Textmarke.</span><span class="sxs-lookup"><span data-stu-id="303a1-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="303a1-140">Die Endposition der Suche wird unmittelbar vor die erste Zeile gefunden wird, dass die Einschränkung und sich vergewissert haben.</span><span class="sxs-lookup"><span data-stu-id="303a1-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="303a1-141">Wenn die Zeile, die auf das durch die Textmarke im _BkOrigin_ -Parameter in der Tabelle nicht mehr vorhanden ist und die Tabelle eine neue Position für das Lesezeichen kann nicht hergestellt werden, gibt **FindRow** MAPI_E_INVALID_BOOKMARK zurück.</span><span class="sxs-lookup"><span data-stu-id="303a1-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="303a1-142">Wenn die Zeile, die auf den _BkOrigin_ nicht mehr vorhanden ist und die Tabelle wird eine neue Position für das Lesezeichen herstellen, gibt **FindRow** MAPI_W_POSITION_CHANGED zurück.</span><span class="sxs-lookup"><span data-stu-id="303a1-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="303a1-143">Wenn die Textmarke _BkOrigin_ übergebenen BOOKMARK_BEGINNING oder BOOKMARK_END ist, gibt **FindRow** MAPI_E_NOT_FOUND, wenn keine entsprechende Zeile gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="303a1-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="303a1-144">Wenn die Textmarke in _BkOrigin_ verwendete BOOKMARK_CURRENT ist, können **FindRow** MAPI_W_POSITION_CHANGED, aber nicht MAPI_E_INVALID_BOOKMARK zurück, da immer eine aktuellen Cursorposition ist.</span><span class="sxs-lookup"><span data-stu-id="303a1-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="303a1-145">Die Spalte **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) ist erforderlich für alle Tabellen und alle Implementierungen von **FindRow** sind erforderlich, um eine Zeile basierend auf PR_INSTANCE_KEY Suchvorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="303a1-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="303a1-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="303a1-146">Notes to implementers</span></span>

<span data-ttu-id="303a1-147">Der Typ des Präfix suchen, die von **FindRow** durchgeführt ist nur nützlich, wenn die Suche die gleiche Richtung wie die Tabelle Organisation folgt.</span><span class="sxs-lookup"><span data-stu-id="303a1-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="303a1-148">Um das erforderliche Verhalten zu erzielen, sollte die Vergleichsfunktion, durch die in der Eigenschaft Einschränkung Struktur übergeben **RELOP_GE** impliziert die gleichen Vergleichsfunktion sein, auf der die Sortierreihenfolge für die Tabelle basiert.</span><span class="sxs-lookup"><span data-stu-id="303a1-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="303a1-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="303a1-149">Notes to callers</span></span>

<span data-ttu-id="303a1-150">**FindRow** können zur Unterstützung von Bildlauf basierend auf Zeichenfolgen vom Benutzer, insbesondere in Listenfeldern in Dialogfeldern Adresse eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="303a1-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="303a1-151">Bei dieser Art von Bildlauf geben die Benutzer ein stetig länger Präfixen einen gewünschten String-Wert, und Sie können in regelmäßigen Abständen Ausstellen eines Anrufs **FindRow** , auf die erste Zeile zu wechseln, die mit das Präfix übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="303a1-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="303a1-152">Die Richtung der Cursor springt welcher Richtung die Suche abhängt ist ausführen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="303a1-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="303a1-153">Um **FindRow**verwenden zu können, muss eine Textmarke festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="303a1-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="303a1-154">Die Zeichenfolgensuche kann von alle Textmarken, einschließlich aus der vordefinierten Lesezeichen zurück, die die aktuelle Position und Anfang und Ende der Tabelle stammen.</span><span class="sxs-lookup"><span data-stu-id="303a1-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="303a1-155">Wenn eine große Anzahl von Zeilen in der Tabelle vorhanden sind, kann der Suchvorgang langsam sein.</span><span class="sxs-lookup"><span data-stu-id="303a1-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="303a1-156">Verwenden Sie eine Einschränkung, um ein Präfix Zeichenfolge wie folgt einen Bildlauf zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="303a1-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="303a1-157">Übergeben Sie für die Suche nach vorne zu einer Spalte in aufsteigender Reihenfolge sortiert und für die Abwärtskompatibilität Suche auf eine Spalte in absteigender Reihenfolge sortiert eine Eigenschaft Einschränkung Struktur in der _LpRestriction_ -Parameter mit der Beziehung **RELOP_GE** und die entsprechenden Eigenschafts-Tag und Präfix, mit dem Format _Tag_ **GE** _Präfix_.</span><span class="sxs-lookup"><span data-stu-id="303a1-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="303a1-158">Weitere Informationen zur Verwendung von Strukturen Einschränkung zum Angeben eines Filters finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="303a1-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="303a1-159">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="303a1-159">MFCMAPI reference</span></span>

<span data-ttu-id="303a1-160">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="303a1-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="303a1-161">**Datei**</span><span class="sxs-lookup"><span data-stu-id="303a1-161">**File**</span></span>|<span data-ttu-id="303a1-162">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="303a1-162">**Function**</span></span>|<span data-ttu-id="303a1-163">**Comment**</span><span class="sxs-lookup"><span data-stu-id="303a1-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="303a1-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="303a1-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="303a1-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="303a1-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="303a1-166">MFCMAPI (engl.) wird die **IMAPITable** -Methode verwendet, um Zeilen zu finden, die eine Einschränkung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="303a1-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="303a1-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="303a1-167">See also</span></span>



[<span data-ttu-id="303a1-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="303a1-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="303a1-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="303a1-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="303a1-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="303a1-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="303a1-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="303a1-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="303a1-172">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="303a1-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

