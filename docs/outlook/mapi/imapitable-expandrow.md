---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415166"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="aa0f7-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="aa0f7-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="aa0f7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa0f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa0f7-105">Erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Überschriftenzeilen auf Blatt- oder Unterebene hinzu, die der Kategorie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a><span data-ttu-id="aa0f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa0f7-106">Parameters</span></span>

 <span data-ttu-id="aa0f7-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="aa0f7-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="aa0f7-108">[in] Die Anzahl der Bytes in der PR_INSTANCE_KEY, auf die der  _pbInstanceKey-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="aa0f7-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="aa0f7-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="aa0f7-110">[in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="aa0f7-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="aa0f7-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="aa0f7-112">[in] Die maximale Anzahl von Zeilen, die im  _lppRows-Parameter zurückgegeben werden_ sollen.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="aa0f7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa0f7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="aa0f7-114">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="aa0f7-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="aa0f7-115">_lppRows_</span></span>
  
> <span data-ttu-id="aa0f7-116">[out] Ein Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die ersten Zeilen (bis  _ulRowCount)_ empfängt, die als Ergebnis der Erweiterung in die Tabellenansicht eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="aa0f7-117">Diese Zeilen werden nach der überschriftenzeile eingefügt, die durch den  _pbInstanceKey-Parameter identifiziert_ wurde.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="aa0f7-118">Der  _lppRows-Parameter_ kann NULL sein, wenn  _der ulRowCount-Parameter_ null ist.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="aa0f7-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="aa0f7-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="aa0f7-120">[out] Ein Zeiger auf die Gesamtanzahl der Zeilen, die der Tabellenansicht hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa0f7-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa0f7-121">Return value</span></span>

<span data-ttu-id="aa0f7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa0f7-122">S_OK</span></span> 
  
> <span data-ttu-id="aa0f7-123">Die Kategorie wurde erfolgreich erweitert.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="aa0f7-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aa0f7-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="aa0f7-125">Die vom  _pbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa0f7-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa0f7-126">Remarks</span></span>

<span data-ttu-id="aa0f7-127">Die **IMAPITable::ExpandRow-Methode** erweitert eine reduzierte Tabellenkategorie und fügt der Tabellenansicht die Überschriftenzeilen auf Blatt- oder unterer Ebene hinzu, die zur Kategorie gehören.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="aa0f7-128">Ein Grenzwert für die Anzahl der Zeilen, die im  _lppRows-Parameter_ zurückgegeben werden sollen, kann im  _ulRowCount-Parameter angegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="aa0f7-129">Wenn  _ulRowCount_ auf einen Wert festgelegt ist, der größer als Null ist und eine oder mehrere Zeilen in dem Zeilensatz zurückgegeben werden, auf den  _lppRows_ verweist, wird die Position der Textmarke BOOKMARK_CURRENT in die Zeile unmittelbar nach der letzten Zeile im Zeilensatz verschoben.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="aa0f7-130">Wenn  _ulRowCount_ auf Null festgelegt ist und fordert, dass der Kategorie Keine Blattzeilen oder Zeilen auf unterer Ebene hinzugefügt werden, oder null Zeilen zurückgegeben werden, da keine Zeilen auf Blatt- oder unterer Ebene in der Kategorie vorhanden sind, wird die Position von BOOKMARK_CURRENT auf die Zeile festgelegt, die der zeile folgt, die durch  _pbInstanceKey_ identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aa0f7-131">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="aa0f7-131">Notes to implementers</span></span>

<span data-ttu-id="aa0f7-132">Generieren Sie keine Benachrichtigungen für Zeilen, die aufgrund der Kategorieerweiterung einer Tabellenansicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa0f7-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="aa0f7-133">Notes to callers</span></span>

<span data-ttu-id="aa0f7-134">Die Anzahl der Zeilen im Zeilensatz, auf die der  _lppRows-Parameter_ verweist, entspricht möglicherweise nicht der Anzahl der Zeilen, die der Tabelle hinzugefügt wurden, dem gesamten Satz von Blatt- oder Unterzeilen für die Kategorie.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="aa0f7-135">Fehler können auftreten, z. B. unzureichender Arbeitsspeicher oder die Anzahl der Zeilen in der Kategorie, die die im  _ulRowCount-Parameter_ angegebene Anzahl überschreitet.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="aa0f7-136">In beiden Fällen wird BOOKMARK_CURRENT an der letzten zurückgegebenen Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="aa0f7-137">Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md)auf, um die restlichen Zeilen in der Kategorie sofort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="aa0f7-138">Erwarten Sie keine Tabellenbenachrichtigung, wenn eine Kategorie ihren Status ändert.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="aa0f7-139">Sie können einen lokalen Cache von Zeilen verwalten, der mit jedem **ExpandRow-** oder **CollapseRow-Aufruf aktualisiert werden** kann.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="aa0f7-140">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="aa0f7-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa0f7-141">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="aa0f7-141">MFCMAPI reference</span></span>

<span data-ttu-id="aa0f7-142">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa0f7-143">**Datei**</span><span class="sxs-lookup"><span data-stu-id="aa0f7-143">**File**</span></span>|<span data-ttu-id="aa0f7-144">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="aa0f7-144">**Function**</span></span>|<span data-ttu-id="aa0f7-145">**Comment**</span><span class="sxs-lookup"><span data-stu-id="aa0f7-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa0f7-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="aa0f7-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="aa0f7-147">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="aa0f7-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="aa0f7-148">MFCMAPI verwendet die **IMAPITable::ExpandRow-Methode,** um eine reduzierte Tabellenkategorie zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aa0f7-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa0f7-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa0f7-149">See also</span></span>



[<span data-ttu-id="aa0f7-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="aa0f7-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="aa0f7-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa0f7-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="aa0f7-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="aa0f7-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

