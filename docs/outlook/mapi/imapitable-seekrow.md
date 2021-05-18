---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413045"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="b2fea-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="b2fea-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="b2fea-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2fea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2fea-105">Verschiebt den Cursor an eine bestimmte Position in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b2fea-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="b2fea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2fea-106">Parameters</span></span>

 <span data-ttu-id="b2fea-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="b2fea-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="b2fea-108">[in] Die Textmarke, die die Startposition für den Suchvorgang identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b2fea-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="b2fea-109">Eine Textmarke kann mit der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt werden, oder einer der folgenden vordefinierten Werte kann übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="b2fea-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="b2fea-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="b2fea-111">Startet den Suchvorgang am Anfang der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b2fea-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="b2fea-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="b2fea-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="b2fea-113">Startet den Suchvorgang aus der Zeile in der Tabelle, in der sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="b2fea-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="b2fea-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="b2fea-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="b2fea-115">Startet den Suchvorgang am Ende der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b2fea-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="b2fea-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="b2fea-116">_lRowCount_</span></span>
  
> <span data-ttu-id="b2fea-117">[in] Die signierte Anzahl der zu verschiebende Zeilen, beginnend mit der textmarke, die durch den  _bkOrigin-Parameter identifiziert_ wird.</span><span class="sxs-lookup"><span data-stu-id="b2fea-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="b2fea-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="b2fea-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="b2fea-119">[out] Wenn  _lRowCount_ ein gültiger Zeiger für die Eingabe ist, zeigt  _lplRowsSought_ auf die Anzahl der Zeilen, die im Suchvorgang verarbeitet wurden, deren Vorzeichen die Richtung der Suche angibt, vorwärts oder rückwärts.</span><span class="sxs-lookup"><span data-stu-id="b2fea-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="b2fea-120">Wenn  _lRowCount_ negativ ist, ist  _lplRowsSought_ negativ.</span><span class="sxs-lookup"><span data-stu-id="b2fea-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2fea-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2fea-121">Return value</span></span>

<span data-ttu-id="b2fea-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2fea-122">S_OK</span></span> 
  
> <span data-ttu-id="b2fea-123">Der Suchvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b2fea-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="b2fea-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b2fea-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b2fea-125">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilensuchenvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b2fea-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="b2fea-126">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="b2fea-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="b2fea-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="b2fea-128">Die im  _bkOrigin-Parameter_ angegebene Textmarke ist ungültig, weil sie entfernt wurde oder weil sie über die letzte angeforderte Zeile hinaus liegt.</span><span class="sxs-lookup"><span data-stu-id="b2fea-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="b2fea-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="b2fea-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="b2fea-130">Der Aufruf ist erfolgreich, aber die im  _bkOrigin-Parameter_ angegebene Textmarke wird nicht mehr in derselben Zeile wie bei der letzten Verwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2fea-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="b2fea-131">Wenn die Textmarke nicht verwendet wurde, befindet sie sich nicht mehr an derselben Position wie beim Erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2fea-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="b2fea-132">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b2fea-133">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="b2fea-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b2fea-134">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b2fea-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2fea-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b2fea-135">Remarks</span></span>

<span data-ttu-id="b2fea-136">Die **IMAPITable::SeekRow-Methode** richtet eine neue BOOKMARK_CURRENT position für den Cursor ein.</span><span class="sxs-lookup"><span data-stu-id="b2fea-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="b2fea-137">Der  _lRowCount-Parameter_ gibt die Anzahl der Zeilen an, die der Cursor bewegt, und die Bewegungsrichtung.</span><span class="sxs-lookup"><span data-stu-id="b2fea-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="b2fea-138">Wenn die resultierende Position über der letzten Zeile der Tabelle liegt, wird der Cursor hinter der letzten Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="b2fea-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="b2fea-139">Wenn sich die resultierende Position vor der ersten Zeile der Tabelle befindet, wird der Cursor am Anfang der ersten Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="b2fea-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2fea-140">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b2fea-140">Notes to implementers</span></span>

<span data-ttu-id="b2fea-141">Wenn die zeile, auf die  _von bkOrigin_ verwiesen wird, nicht mehr in der Tabelle vorhanden ist und Sie keine neue Position für die Textmarke einrichten können, geben Sie MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="b2fea-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="b2fea-142">Wenn die Zeile, auf die  _von bkOrigin_ verwiesen wird, nicht mehr vorhanden ist und Sie eine neue Position für die Textmarke einrichten können, geben Sie MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="b2fea-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="b2fea-143">Eine Textmarke, die auf eine Zeile zeigt, die aus der Tabellenansicht reduziert ist, kann weiterhin verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="b2fea-144">Wenn der Aufrufer versucht, den Cursor zu einer solchen Textmarke zu verschieben, verschieben Sie den Cursor zur nächsten sichtbaren Zeile, und geben Sie MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="b2fea-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="b2fea-145">Sie können Lesezeichen für Positionen verschieben, die zum Zeitpunkt der Verwendung oder zum Zeitpunkt des Reduzierens der Zeile aus der Ansicht reduziert wurden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="b2fea-146">Wenn eine Textmarke zu dem Zeitpunkt verschoben wird, zu dem die Zeile reduziert wird, behalten Sie ein Bit in der Textmarke bei, das angibt, ob die Textmarke seit der letzten Verwendung verschoben wurde oder, falls sie nie verwendet wurde, seit ihrer Erstellung.</span><span class="sxs-lookup"><span data-stu-id="b2fea-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b2fea-147">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b2fea-147">Notes to callers</span></span>

<span data-ttu-id="b2fea-148">Um eine Rückwärtsbewegung für **SeekRow** anzugeben, übergeben Sie einen negativen Wert in  _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="b2fea-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="b2fea-149">Um an den Anfang der Tabelle zu suchen, übergeben Sie null in  _lRowCount_ und den Wert BOOKMARK_BEGINNING in  _bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="b2fea-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="b2fea-150">Wenn die Tabelle viele Zeilen enthält, kann **der SeekRow-Vorgang** langsam sein.</span><span class="sxs-lookup"><span data-stu-id="b2fea-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="b2fea-151">Die Leistung kann auch beeinträchtigt werden, wenn eine Zeilenanzahl im Inhalt des  _lplRowsSought-Parameters zurückgegeben werden_ muss.</span><span class="sxs-lookup"><span data-stu-id="b2fea-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="b2fea-152">**SeekRow** gibt die Anzahl der Zeilen zurück, die tatsächlich in der variablen, auf die von  _lRowCount_ verwiesen wird, positiv oder negativ durchsucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="b2fea-153">Im normalen Vorgang sollte derselbe Wert für  _lplRowsSought_ wie für  _lRowCount_ übergeben werden, es sei denn, die Suche hat den Anfang oder das Ende der Tabelle erreicht.</span><span class="sxs-lookup"><span data-stu-id="b2fea-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="b2fea-154">Legen Sie  _lRowCount nicht_ auf eine Zahl größer als 50.</span><span class="sxs-lookup"><span data-stu-id="b2fea-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="b2fea-155">Verwenden Sie zum Durchsuchen einer größeren Anzahl von Zeilen die [IMAPITable::SeekRowApprox-Methode.](imapitable-seekrowapprox.md)</span><span class="sxs-lookup"><span data-stu-id="b2fea-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b2fea-156">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b2fea-156">MFCMAPI reference</span></span>

<span data-ttu-id="b2fea-157">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b2fea-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b2fea-158">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b2fea-158">**File**</span></span>|<span data-ttu-id="b2fea-159">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b2fea-159">**Function**</span></span>|<span data-ttu-id="b2fea-160">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b2fea-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2fea-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="b2fea-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="b2fea-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="b2fea-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="b2fea-163">MFCMAPI verwendet die **IMAPITable::SeekRow-Methode,** um den Anfang der Tabelle vor der Verarbeitung zu finden.</span><span class="sxs-lookup"><span data-stu-id="b2fea-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2fea-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2fea-164">See also</span></span>



[<span data-ttu-id="b2fea-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="b2fea-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="b2fea-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="b2fea-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="b2fea-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b2fea-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="b2fea-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="b2fea-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="b2fea-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2fea-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="b2fea-170">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b2fea-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

