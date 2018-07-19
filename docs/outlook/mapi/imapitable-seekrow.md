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
ms.openlocfilehash: 143ca03a5e98d638d29394f5c0803e349ab4de25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792471"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="ade76-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="ade76-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="ade76-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ade76-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ade76-105">Verschiebt den Cursor an eine bestimmte Position in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="ade76-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="ade76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ade76-106">Parameters</span></span>

 <span data-ttu-id="ade76-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="ade76-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="ade76-108">[in] Die Textmarke, die die Anfangsposition für den Vorgang Seek identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ade76-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="ade76-109">Eine Textmarke kann mithilfe der [IMAPITable::CreateBookmark](imapitable-createbookmark.md) -Methode erstellt werden, oder eine der folgenden vordefinierten Werte übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ade76-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="ade76-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="ade76-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="ade76-111">Startet den Suchvorgang am Anfang der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ade76-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="ade76-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="ade76-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="ade76-113">Startet den Suchvorgang aus der Zeile in der Tabelle, in dem sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="ade76-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="ade76-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="ade76-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="ade76-115">Startet den Suchvorgang vom Ende der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="ade76-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="ade76-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="ade76-116">_lRowCount_</span></span>
  
> <span data-ttu-id="ade76-117">[in] Die Anzahl der Anzahl der zu verschiebenden Zeilen mit Vorzeichen, durch den Parameter _BkOrigin_ identifiziert die Textmarke ab.</span><span class="sxs-lookup"><span data-stu-id="ade76-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="ade76-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="ade76-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="ade76-119">[out] Ist _lRowCount_ ein gültiger Zeiger auf input _LplRowsSought_ verweist auf die Anzahl der Zeilen, die in den Suchvorgang verarbeitet wurden, gibt die Zeichen, von denen die Richtung der Suche, vorwärts oder rückwärts.</span><span class="sxs-lookup"><span data-stu-id="ade76-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="ade76-120">Wenn _lRowCount_ negativ ist, klicken Sie dann ist _LplRowsSought_ negativ.</span><span class="sxs-lookup"><span data-stu-id="ade76-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ade76-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ade76-121">Return value</span></span>

<span data-ttu-id="ade76-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ade76-122">S_OK</span></span> 
  
> <span data-ttu-id="ade76-123">Der Suchvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ade76-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="ade76-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ade76-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ade76-125">Ein anderer Vorgang wird ausgeführt, die den Vorgang Zeile Ansprechpartner bei einem Neustart verhindert.</span><span class="sxs-lookup"><span data-stu-id="ade76-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="ade76-126">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ade76-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="ade76-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="ade76-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="ade76-128">Die Textmarke im _BkOrigin_ -Parameter angegebene ist ungültig oder da sie entfernt wurde, da sie nach der letzten Zeile angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ade76-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="ade76-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="ade76-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="ade76-130">Der Aufruf war erfolgreich, aber im _BkOrigin_ -Parameter angegebene Textmarke wird nicht mehr in der gleichen Zeile festgelegt, wie bei der es zuletzt verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ade76-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="ade76-131">Wenn die Textmarke nicht verwendet wurden, ist es nicht mehr an derselben Position wie bei der es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ade76-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="ade76-132">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ade76-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ade76-133">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="ade76-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ade76-134">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ade76-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ade76-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ade76-135">Remarks</span></span>

<span data-ttu-id="ade76-136">Die **IMAPITable::SeekRow** -Methode stellt eine neue BOOKMARK_CURRENT Position für den Cursor her.</span><span class="sxs-lookup"><span data-stu-id="ade76-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="ade76-137">Der Parameter _lRowCount_ gibt die Anzahl der Zeilen, die der Cursor bewegt wird und die Richtung der Bewegung an.</span><span class="sxs-lookup"><span data-stu-id="ade76-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="ade76-138">Wenn die resultierende Position nach der letzten Zeile der Tabelle ist, wird der Cursor nach der letzten Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="ade76-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="ade76-139">Wenn die resultierende Position vor der ersten Zeile der Tabelle ist, wird der Cursor am Anfang der ersten Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="ade76-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ade76-140">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ade76-140">Notes to implementers</span></span>

<span data-ttu-id="ade76-141">Wenn die Zeile, die auf den _BkOrigin_ in der Tabelle nicht mehr vorhanden ist und Sie keine neue Position für das Lesezeichen, geben Sie MAPI_E_INVALID_BOOKMARK zurück.</span><span class="sxs-lookup"><span data-stu-id="ade76-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="ade76-142">Wenn die Zeile, die auf den _BkOrigin_ nicht mehr vorhanden ist und Sie können eine neue Position für das Lesezeichen einrichten, geben Sie MAPI_W_POSITION_CHANGED zurück.</span><span class="sxs-lookup"><span data-stu-id="ade76-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="ade76-143">Eine Textmarke verweisen auf eine Zeile, die aus der Tabellenansicht reduziert ist kann immer noch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ade76-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="ade76-144">Wenn der Aufrufer versucht, den Cursor in solchen ein Lesezeichen zu verschieben, bewegen Sie den Cursor in die nächste Zeile sichtbar und zurückzugeben Sie MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="ade76-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="ade76-145">Sie können verschieben Lesezeichen für Positionen reduziert aus der Ansicht, die zum Zeitpunkt der Verwendung oder zur Zeit, die die Zeile reduziert ist.</span><span class="sxs-lookup"><span data-stu-id="ade76-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="ade76-146">Wenn eine Textmarke Zeitpunkt verschoben wird, die die Zeile reduziert ist, lassen Sie etwas in die Textmarke, die angibt, ob die Textmarke wurde seit der letzten Verwendung verschoben oder, hat es nie, seit seiner Erstellung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ade76-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ade76-147">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ade76-147">Notes to callers</span></span>

<span data-ttu-id="ade76-148">Um eine Ebene nach hinten Verschiebung für **SeekRow**angegeben haben, übergeben Sie einen negativen Wert _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="ade76-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="ade76-149">Um an den Anfang der Tabelle zu suchen, übergeben Sie NULL in _lRowCount_ und der Wert BOOKMARK_BEGINNING in _BkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="ade76-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="ade76-150">Wenn viele Zeilen in der Tabelle vorhanden sind, kann der Vorgang **SeekRow** langsam sein.</span><span class="sxs-lookup"><span data-stu-id="ade76-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="ade76-151">Leistung kann auch beeinflusst werden, wenn Sie benötigen eine Zeilenanzahl in den Inhalt des Parameters _LplRowsSought_ zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ade76-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="ade76-152">**SeekRow** gibt die Anzahl der Zeilen tatsächlich über gesucht, positiven oder negativen, in der Variablen, die auf den _lRowCount_zurück.</span><span class="sxs-lookup"><span data-stu-id="ade76-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="ade76-153">Im normalen Betrieb sollten sie den gleichen Wert für _LplRowsSought_ zurückgeben, wie für _lRowCount_, übergeben, sofern die Suche der Anfang oder das Ende der Tabelle erreicht.</span><span class="sxs-lookup"><span data-stu-id="ade76-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="ade76-154">Legen Sie nicht _lRowCount_ auf eine Zahl größer als 50.</span><span class="sxs-lookup"><span data-stu-id="ade76-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="ade76-155">Um eine größere Anzahl von Zeilen zu suchen, verwenden Sie [die SeekRowApprox](imapitable-seekrowapprox.md) .</span><span class="sxs-lookup"><span data-stu-id="ade76-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ade76-156">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="ade76-156">MFCMAPI reference</span></span>

<span data-ttu-id="ade76-157">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ade76-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ade76-158">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ade76-158">**File**</span></span>|<span data-ttu-id="ade76-159">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ade76-159">**Function**</span></span>|<span data-ttu-id="ade76-160">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ade76-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ade76-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="ade76-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="ade76-162">CMAPIProcessor::ProcessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="ade76-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="ade76-163">MFCMAPI (engl.) verwendet die **IMAPITable::SeekRow** -Methode, um den Anfang der Tabelle vor der Verarbeitung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ade76-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ade76-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ade76-164">See also</span></span>



[<span data-ttu-id="ade76-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ade76-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="ade76-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="ade76-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="ade76-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ade76-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ade76-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ade76-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="ade76-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ade76-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ade76-170">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ade76-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

