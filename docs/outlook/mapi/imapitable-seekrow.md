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
# <a name="imapitableseekrow"></a><span data-ttu-id="c43a1-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="c43a1-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="c43a1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c43a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c43a1-105">Verschiebt den Cursor an eine bestimmte Position in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c43a1-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="c43a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c43a1-106">Parameters</span></span>

 <span data-ttu-id="c43a1-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="c43a1-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="c43a1-108">in Die Textmarke, die die Anfangsposition für den Seek-Vorgang identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c43a1-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="c43a1-109">Eine Textmarke kann mit der [IMAPITable:: CreateBookMark](imapitable-createbookmark.md) -Methode oder einem der folgenden vordefinierten Werte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c43a1-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="c43a1-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="c43a1-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="c43a1-111">Startet den Seek-Vorgang vom Anfang der Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="c43a1-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="c43a1-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="c43a1-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="c43a1-113">Startet den Seek-Vorgang von der Zeile in der Tabelle, in der sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="c43a1-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="c43a1-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="c43a1-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="c43a1-115">Startet den Seek-Vorgang am Ende der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c43a1-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="c43a1-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="c43a1-116">_lRowCount_</span></span>
  
> <span data-ttu-id="c43a1-117">in Die signierte Anzahl der zu verschiebende Zeilen, beginnend mit der durch den _bkOrigin_ -Parameter angegebenen Textmarke.</span><span class="sxs-lookup"><span data-stu-id="c43a1-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="c43a1-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="c43a1-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="c43a1-119">Out Wenn _lRowCount_ ein gültiger Zeiger auf der Eingabe ist, zeigt _lplRowsSought_ auf die Anzahl der Zeilen, die in der Seek-Operation verarbeitet wurden, deren Vorzeichen die Richtung der Suche angibt, vorwärts oder rückwärts.</span><span class="sxs-lookup"><span data-stu-id="c43a1-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="c43a1-120">Wenn _lRowCount_ negativ ist, ist _lplRowsSought_ negativ.</span><span class="sxs-lookup"><span data-stu-id="c43a1-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c43a1-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c43a1-121">Return value</span></span>

<span data-ttu-id="c43a1-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c43a1-122">S_OK</span></span> 
  
> <span data-ttu-id="c43a1-123">Der Seek-Vorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c43a1-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="c43a1-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c43a1-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c43a1-125">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilen Suchvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c43a1-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="c43a1-126">Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="c43a1-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="c43a1-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="c43a1-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="c43a1-128">Die im _bkOrigin_ -Parameter angegebene Textmarke ist ungültig, da Sie entfernt wurde oder über die letzte angeforderte Zeile hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="c43a1-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="c43a1-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="c43a1-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="c43a1-130">Der Aufruf wurde erfolgreich ausgeführt, aber die im _bkOrigin_ -Parameter angegebene Textmarke wird nicht mehr in derselben Zeile festgelegt wie bei der letzten Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c43a1-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="c43a1-131">Wenn die Textmarke nicht verwendet wurde, befindet Sie sich nicht mehr in der gleichen Position wie bei ihrer Erstellung.</span><span class="sxs-lookup"><span data-stu-id="c43a1-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="c43a1-132">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c43a1-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c43a1-133">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="c43a1-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c43a1-134">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c43a1-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c43a1-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c43a1-135">Remarks</span></span>

<span data-ttu-id="c43a1-136">Die **IMAPITable:: SeekRow** -Methode richtet eine neue BOOKMARK_CURRENT-Position für den Cursor ein.</span><span class="sxs-lookup"><span data-stu-id="c43a1-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="c43a1-137">Der Parameter _lRowCount_ gibt die Anzahl der Zeilen an, die der Cursor verschiebt, und die Bewegungsrichtung.</span><span class="sxs-lookup"><span data-stu-id="c43a1-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="c43a1-138">Wenn sich die resultierende Position jenseits der letzten Zeile der Tabelle befindet, wird der Cursor nach der letzten Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="c43a1-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="c43a1-139">Wenn sich die resultierende Position vor der ersten Zeile der Tabelle befindet, wird der Cursor am Anfang der ersten Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="c43a1-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c43a1-140">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c43a1-140">Notes to implementers</span></span>

<span data-ttu-id="c43a1-141">Wenn die Zeile, auf die durch _bkOrigin_ verwiesen wird, in der Tabelle nicht mehr vorhanden ist und Sie keine neue Position für die Textmarke festlegen können, geben Sie MAPI_E_INVALID_BOOKMARK zurück.</span><span class="sxs-lookup"><span data-stu-id="c43a1-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="c43a1-142">Wenn die Zeile, auf die durch _bkOrigin_ verwiesen wird, nicht mehr vorhanden ist und Sie eine neue Position für die Textmarke festlegen können, geben Sie MAPI_W_POSITION_CHANGED zurück.</span><span class="sxs-lookup"><span data-stu-id="c43a1-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="c43a1-143">Eine Textmarke, die auf eine Zeile zeigt, die aus der Tabellenansicht ausgeblendet ist, kann weiterhin verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c43a1-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="c43a1-144">Wenn der Aufrufer versucht, den Cursor auf eine solche Textmarke zu verschieben, bewegen Sie den Cursor zur nächsten sichtbaren Zeile, und geben Sie MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="c43a1-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="c43a1-145">Sie können Lesezeichen für Positionen verschieben, die aus der Ansicht ausgeblendet wurden, entweder zum Zeitpunkt der Verwendung oder zum Zeitpunkt, zu dem die Zeile reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="c43a1-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="c43a1-146">Wenn eine Textmarke zu dem Zeitpunkt verschoben wird, zu dem die Zeile reduziert wird, behalten Sie ein Bit in der Textmarke, die angibt, ob die Textmarke seit der letzten Verwendung verschoben wurde, oder, falls Sie noch nie verwendet wurde, seit ihrer Erstellung.</span><span class="sxs-lookup"><span data-stu-id="c43a1-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c43a1-147">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c43a1-147">Notes to callers</span></span>

<span data-ttu-id="c43a1-148">Um eine Rückwärtsbewegung für **SeekRow**anzugeben, geben Sie einen negativen Wert in _lRowCount_an.</span><span class="sxs-lookup"><span data-stu-id="c43a1-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="c43a1-149">Um am Anfang der Tabelle zu suchen, überschreiten Sie NULL in _lRowCount_ und den Wert BOOKMARK_BEGINNING in _bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="c43a1-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="c43a1-150">Wenn in der Tabelle viele Zeilen vorhanden sind, kann der **SeekRow** -Vorgang langsam sein.</span><span class="sxs-lookup"><span data-stu-id="c43a1-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="c43a1-151">Die Leistung kann auch beeinträchtigt werden, wenn eine Zeilenanzahl im Inhalt des _lplRowsSought_ -Parameters zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="c43a1-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="c43a1-152">**SeekRow** gibt die Anzahl der Zeilen zurück, die tatsächlich durchsucht wurden, positiv oder negativ in der Variablen, auf die durch _lRowCount_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c43a1-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="c43a1-153">Im gewöhnlichen Vorgang sollte es den gleichen Wert für _lplRowsSought_ zurückgeben, wie er für _lRowCount_übergeben wird, es sei denn, die Suche hat den Anfang oder das Ende der Tabelle erreicht.</span><span class="sxs-lookup"><span data-stu-id="c43a1-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="c43a1-154">Legen Sie _lRowCount_ nicht auf eine Zahl größer als 50.</span><span class="sxs-lookup"><span data-stu-id="c43a1-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="c43a1-155">Verwenden Sie die [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) -Methode, um eine größere Anzahl von Zeilen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c43a1-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c43a1-156">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c43a1-156">MFCMAPI reference</span></span>

<span data-ttu-id="c43a1-157">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c43a1-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c43a1-158">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c43a1-158">**File**</span></span>|<span data-ttu-id="c43a1-159">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c43a1-159">**Function**</span></span>|<span data-ttu-id="c43a1-160">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c43a1-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c43a1-161">MAPIProcessor. cpp</span><span class="sxs-lookup"><span data-stu-id="c43a1-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="c43a1-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="c43a1-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="c43a1-163">MFCMAPI verwendet die **IMAPITable:: SeekRow** -Methode, um den Anfang der Tabelle vor der Verarbeitung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c43a1-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c43a1-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c43a1-164">See also</span></span>



[<span data-ttu-id="c43a1-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="c43a1-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="c43a1-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="c43a1-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="c43a1-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="c43a1-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="c43a1-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="c43a1-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="c43a1-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c43a1-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c43a1-170">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c43a1-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

