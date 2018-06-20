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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792446"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="31c81-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="31c81-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="31c81-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31c81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31c81-105">Erweitert eine reduzierte Tabellenkategorie, Hinzufügen von Endknoten oder auf niedrigerer Ebene Überschriftenzeilen der Kategorie auf die Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="31c81-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="31c81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31c81-106">Parameters</span></span>

 <span data-ttu-id="31c81-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="31c81-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="31c81-108">[in] Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft auf den durch den Parameter _PbInstanceKey_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="31c81-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="31c81-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="31c81-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="31c81-110">[in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die Zeile mit der Spaltenüberschrift für die Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="31c81-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="31c81-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="31c81-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="31c81-112">[in] Die maximale Anzahl der Zeilen, die im Parameter _LppRows_ zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="31c81-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="31c81-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31c81-113">_ulFlags_</span></span>
  
> <span data-ttu-id="31c81-114">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="31c81-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="31c81-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="31c81-115">_lppRows_</span></span>
  
> <span data-ttu-id="31c81-116">[out] Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur empfangen die ersten (bis zum _UlRowCount_) Zeilen, die in der Tabellenansicht als Ergebnis der Erweiterung eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="31c81-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="31c81-117">Diese Zeilen werden nach der Zeile mit der Spaltenüberschrift identifiziert durch den Parameter _PbInstanceKey_ eingefügt.</span><span class="sxs-lookup"><span data-stu-id="31c81-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="31c81-118">Wenn der Parameter _UlRowCount_ gleich NULL ist, kann der Parameter _LppRows_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="31c81-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="31c81-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="31c81-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="31c81-120">[out] Ein Zeiger auf die Gesamtzahl der Zeilen, die die Tabellenansicht hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="31c81-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31c81-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="31c81-121">Return value</span></span>

<span data-ttu-id="31c81-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="31c81-122">S_OK</span></span> 
  
> <span data-ttu-id="31c81-123">Die Kategorie wurde erfolgreich erweitert.</span><span class="sxs-lookup"><span data-stu-id="31c81-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="31c81-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="31c81-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="31c81-125">Die Zeile, die vom _PbInstanceKey_ -Parameter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="31c81-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31c81-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31c81-126">Remarks</span></span>

<span data-ttu-id="31c81-127">Die **IMAPITable::ExpandRow** -Methode erweitert eine reduzierte Tabellenkategorie, Hinzufügen von Endknoten oder auf niedrigerer Ebene Überschriftenzeilen, die die Tabelle-Ansicht der Kategorie angehören.</span><span class="sxs-lookup"><span data-stu-id="31c81-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="31c81-128">Beschränkt die Anzahl der Zeilen im _LppRows_ -Parameter zurückgegeben werden soll, kann in der _UlRowCount_ -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="31c81-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="31c81-129">Wenn _UlRowCount_ auf einen Wert größer als 0 (null) festgelegt wird, und eine oder mehrere Zeilen in der Zeile auf den _LppRows_zurückgegeben werden, legen Sie die Position der Textmarke, die bookmark_current in die Zeile unmittelbar nach der letzten Zeile in der Zeile verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="31c81-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="31c81-130">Wenn _UlRowCount_ auf NULL festgelegt ist, für die Kategorie hinzugefügt werden, die Endknoten NULL oder auf niedrigerer Ebene Überschriftenzeilen anfordern oder keine Zeilen zurückgegeben werden, da keine Endknoten oder auf niedrigerer Ebene Überschriftenzeilen in der Kategorie vorhanden sind, wird die Position des BOOKMARK_CURRENT in die Zeile festgelegt. nach der Zeile, die durch _PbInstanceKey_identifiziert.</span><span class="sxs-lookup"><span data-stu-id="31c81-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="31c81-131">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="31c81-131">Notes to implementers</span></span>

<span data-ttu-id="31c81-132">Generieren Sie keine Benachrichtigungen auf Zeilen, die aufgrund der Kategorie die Erweiterung einer Tabellenansicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="31c81-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="31c81-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="31c81-133">Notes to callers</span></span>

<span data-ttu-id="31c81-134">Die Anzahl der Zeilen in der Zeile durch den Parameter _LppRows_ auf zeigt möglicherweise nicht gleich der Anzahl der Zeilen, die tatsächlich zur Tabelle hinzugefügt wurden, die gesamte Satz von Endknoten oder auf niedrigerer Ebene Überschriftenzeilen für die Kategorie.</span><span class="sxs-lookup"><span data-stu-id="31c81-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="31c81-135">Fehler können auftreten, wie nicht genügend Arbeitsspeicher oder die Anzahl der Zeilen in der Kategorie überschreiten im _UlRowCount_ -Parameter angegebene Nummer getestet werden.</span><span class="sxs-lookup"><span data-stu-id="31c81-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="31c81-136">In beiden Fällen wird in der letzten Zeile zurückgegeben BOOKMARK_CURRENT positioniert.</span><span class="sxs-lookup"><span data-stu-id="31c81-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="31c81-137">Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md), um den Rest der Zeilen in der Kategorie sofort abzurufen.</span><span class="sxs-lookup"><span data-stu-id="31c81-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="31c81-138">Davon ausgehen, dass eine Tabelle Benachrichtigung zu erhalten, wenn eine Kategorie den Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="31c81-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="31c81-139">Sie können einen lokalen Cache der Zeilen verwalten, die bei jedem Anruf **ExpandRow** oder **CollapseRow** aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="31c81-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="31c81-140">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="31c81-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="31c81-141">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="31c81-141">MFCMAPI reference</span></span>

<span data-ttu-id="31c81-142">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="31c81-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="31c81-143">**Datei**</span><span class="sxs-lookup"><span data-stu-id="31c81-143">**File**</span></span>|<span data-ttu-id="31c81-144">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="31c81-144">**Function**</span></span>|<span data-ttu-id="31c81-145">**Comment**</span><span class="sxs-lookup"><span data-stu-id="31c81-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31c81-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="31c81-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="31c81-147">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="31c81-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="31c81-148">MFCMAPI (engl.) wird die **IMAPITable::ExpandRow** -Methode verwendet, um eine reduzierte Tabellenkategorie zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="31c81-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31c81-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31c81-149">See also</span></span>



[<span data-ttu-id="31c81-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="31c81-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="31c81-151">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="31c81-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="31c81-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="31c81-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

