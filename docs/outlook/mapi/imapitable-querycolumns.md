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
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792467"
---
# <a name="imapitablequerycolumns"></a><span data-ttu-id="48797-103">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="48797-103">IMAPITable::QueryColumns</span></span>

  
  
<span data-ttu-id="48797-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48797-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48797-105">Gibt eine Liste mit Spalten für die Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="48797-105">Returns a list of columns for the table.</span></span>
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="48797-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48797-106">Parameters</span></span>

 <span data-ttu-id="48797-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48797-107">_ulFlags_</span></span>
  
> <span data-ttu-id="48797-108">[in] Bitmaske aus Flags, die angibt, welche Spalte festlegen sollten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="48797-108">[in] Bitmask of flags that indicates which column set should be returned.</span></span> <span data-ttu-id="48797-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="48797-109">The following flag can be set:</span></span>
    
<span data-ttu-id="48797-110">TBL_ALL_COLUMNS</span><span class="sxs-lookup"><span data-stu-id="48797-110">TBL_ALL_COLUMNS</span></span> 
  
> <span data-ttu-id="48797-111">Die Tabelle sollte alle Verfügbare Spalten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48797-111">The table should return all available columns.</span></span>
    
 <span data-ttu-id="48797-112">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="48797-112">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="48797-113">[out] Legen Sie den Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die die Eigenschaftentags für die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="48797-113">[out] Pointer to an [SPropTagArray](sproptagarray.md) structure containing the property tags for the column set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48797-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48797-114">Return value</span></span>

<span data-ttu-id="48797-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="48797-115">S_OK</span></span> 
  
> <span data-ttu-id="48797-116">Die Spalte wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48797-116">The column set was successfully returned.</span></span>
    
<span data-ttu-id="48797-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="48797-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="48797-118">Ein anderer Vorgang wird ausgeführt, die verhindert, die Spalte dass Abrufvorgang starten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48797-118">Another operation is in progress that prevents the column set retrieval operation from starting.</span></span> <span data-ttu-id="48797-119">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="48797-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48797-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48797-120">Remarks</span></span>

<span data-ttu-id="48797-121">Die **IMAPITable::QueryColumns** -Methode kann EntityInstances abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="48797-121">The **IMAPITable::QueryColumns** method can be called to retrieve:</span></span> 
  
- <span data-ttu-id="48797-122">Die Standardspalte für eine Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="48797-122">The default column set for a table.</span></span>
    
- <span data-ttu-id="48797-123">Der aktuellen Spalte für eine Tabelle festlegen, wie durch einen Aufruf an die [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48797-123">The current column set for a table, as established by a call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="48797-124">Die vollständige Spalte für eine Tabelle, die Spalten, die verfügbar sind, aber nicht unbedingt Teil der aktuellen Gruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48797-124">The complete column set for a table, the columns that are available, but not necessarily part of the current set.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="48797-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="48797-125">Notes to callers</span></span>

<span data-ttu-id="48797-126">Wenn Sie nicht das TBL_ALL_COLUMNS-Flag festlegen, gibt **IMAPITable::QueryColumns** eine Tabelle Standard oder aktuellen Spalte festgelegt, je nachdem, ob die Tabelle durch einen Aufruf von **IMAPITable::SetColumns**betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="48797-126">If you do not set the TBL_ALL_COLUMNS flag, **IMAPITable::QueryColumns** returns either a table's default or current column set, depending on whether the table has been affected by a call to **IMAPITable::SetColumns**.</span></span> <span data-ttu-id="48797-127">**SetColumns** ändert die Reihenfolge und Auswahl von Spalten in einer Tabelle Spalte festlegen.</span><span class="sxs-lookup"><span data-stu-id="48797-127">**SetColumns** changes the order and selection of columns in a table's column set.</span></span> 
  
<span data-ttu-id="48797-128">Wenn Sie das TBL_ALL_COLUMNS-Flag festlegen, gibt **QueryColumns** alle Spalten, die in der Tabelle Spalte festlegen, sondern können.</span><span class="sxs-lookup"><span data-stu-id="48797-128">If you set the TBL_ALL_COLUMNS flag, **QueryColumns** returns all of the columns that are capable of being in the table's column set.</span></span> 
  
<span data-ttu-id="48797-129">Freigeben des Speichers für die Array-Tag-Eigenschaft durch den Parameter _LpPropTagArray_ auf das durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="48797-129">Free the memory for the property tag array pointed to by the  _lpPropTagArray_ parameter by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="48797-130">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="48797-130">MFCMAPI reference</span></span>

<span data-ttu-id="48797-131">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="48797-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="48797-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="48797-132">**File**</span></span>|<span data-ttu-id="48797-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="48797-133">**Function**</span></span>|<span data-ttu-id="48797-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="48797-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48797-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="48797-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="48797-136">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="48797-136">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="48797-137">MFCMAPI (engl.) verwendet die **IMAPITable::QueryColumns** -Methode zum Abrufen der aktuellen Spalte für eine Tabelle festlegen, sodass der Benutzer bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="48797-137">MFCMAPI uses the **IMAPITable::QueryColumns** method to retrieve the current column set for a table so the user can edit it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48797-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48797-138">See also</span></span>



[<span data-ttu-id="48797-139">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="48797-139">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="48797-140">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="48797-140">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="48797-141">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="48797-141">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="48797-142">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48797-142">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="48797-143">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="48797-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

