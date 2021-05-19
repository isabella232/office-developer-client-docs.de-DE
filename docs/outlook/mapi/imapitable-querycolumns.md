---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410105"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="1fc0e-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1fc0e-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="1fc0e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fc0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fc0e-105">Gibt eine Liste der Spalten für die Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="1fc0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fc0e-106">Parameters</span></span>

 <span data-ttu-id="1fc0e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1fc0e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1fc0e-108">[in] Bitmaske von Flags, die angibt, welcher Spaltensatz zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="1fc0e-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1fc0e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1fc0e-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="1fc0e-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="1fc0e-111">Die Tabelle sollte alle verfügbaren Spalten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="1fc0e-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="1fc0e-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="1fc0e-113">[out] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die die Eigenschaftstags für den Spaltensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1fc0e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fc0e-114">Return value</span></span>

<span data-ttu-id="1fc0e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fc0e-115">S_OK</span></span> 
  
> <span data-ttu-id="1fc0e-116">Der Spaltensatz wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="1fc0e-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1fc0e-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1fc0e-118">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Spaltensatzabrufvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="1fc0e-119">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1fc0e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fc0e-120">Remarks</span></span>

<span data-ttu-id="1fc0e-121">Die **IMAPITable::QueryColumns-Methode** kann aufgerufen werden, um:</span><span class="sxs-lookup"><span data-stu-id="1fc0e-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="1fc0e-122">Der Standardspaltensatz für eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="1fc0e-123">Die aktuelle Spalte, die für eine Tabelle festgelegt ist, wie sie durch einen Aufruf der [IMAPITable::SetColumns-Methode festgelegt](imapitable-setcolumns.md) wurde.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="1fc0e-124">Der vollständige Spaltensatz für eine Tabelle, die spalten, die verfügbar sind, aber nicht unbedingt Teil der aktuellen Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1fc0e-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1fc0e-125">Notes to callers</span></span>

<span data-ttu-id="1fc0e-126">Wenn Sie das flag TBL_ALL_COLUMNS nicht festlegen, gibt **IMAPITable::QueryColumns** entweder den Standard- oder aktuellen Spaltensatz einer Tabelle zurück, je nachdem, ob die Tabelle durch einen Aufruf von **IMAPITable::SetColumns** beeinflusst wurde.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="1fc0e-127">**SetColumns** ändert die Reihenfolge und Auswahl von Spalten im Spaltensatz einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="1fc0e-128">Wenn Sie das TBL_ALL_COLUMNS festlegen, gibt **QueryColumns** alle Spalten zurück, die im Spaltensatz der Tabelle enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="1fc0e-129">Gibt den Arbeitsspeicher für das Eigenschaftentagarray frei, auf das der  _lpPropTagArray-Parameter_ verweist, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1fc0e-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1fc0e-130">MFCMAPI reference</span></span>

<span data-ttu-id="1fc0e-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1fc0e-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1fc0e-132">**File**</span></span>|<span data-ttu-id="1fc0e-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1fc0e-133">**Function**</span></span>|<span data-ttu-id="1fc0e-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1fc0e-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1fc0e-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="1fc0e-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1fc0e-136">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="1fc0e-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="1fc0e-137">MFCMAPI verwendet die **IMAPITable::QueryColumns-Methode,** um den aktuellen Spaltensatz für eine Tabelle abzurufen, damit der Benutzer ihn bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="1fc0e-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fc0e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fc0e-138">See also</span></span>



[<span data-ttu-id="1fc0e-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1fc0e-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="1fc0e-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1fc0e-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1fc0e-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1fc0e-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1fc0e-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1fc0e-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="1fc0e-143">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1fc0e-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

