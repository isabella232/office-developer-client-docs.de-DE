---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434333"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="d7e1d-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="d7e1d-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="d7e1d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7e1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7e1d-105">Gibt den Status und Typ der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="d7e1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7e1d-106">Parameters</span></span>

 <span data-ttu-id="d7e1d-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="d7e1d-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="d7e1d-108">[out] Zeiger auf einen Wert, der den Status der Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="d7e1d-109">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="d7e1d-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="d7e1d-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="d7e1d-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="d7e1d-111">Es werden keine Vorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-111">No operations are in progress.</span></span>
    
<span data-ttu-id="d7e1d-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="d7e1d-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="d7e1d-113">Der Inhalt der Tabelle hat sich erwartungslich geändert.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="d7e1d-114">Dieser Statuswert wird nicht für Änderungen zurückgegeben, die aus Sortier- oder Einschränkungsvorgängen resulten.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="d7e1d-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="d7e1d-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="d7e1d-116">Bei einem [IMAPITable::Restrict-Vorgang](imapitable-restrict.md) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="d7e1d-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="d7e1d-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="d7e1d-118">Ein **IMAPITable::Restrict-Vorgang** wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="d7e1d-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="d7e1d-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="d7e1d-120">Bei einem [IMAPITable::SetColumns-Vorgang](imapitable-setcolumns.md) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="d7e1d-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="d7e1d-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="d7e1d-122">Ein **IMAPITable::SetColumns-Vorgang** wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="d7e1d-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="d7e1d-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="d7e1d-124">Bei einem [IMAPITable::SortTable-Vorgang](imapitable-sorttable.md) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="d7e1d-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="d7e1d-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="d7e1d-126">Ein **IMAPITable::SortTable-Vorgang** wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="d7e1d-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="d7e1d-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="d7e1d-128">[out] Zeiger auf einen Wert, der den Typ der Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="d7e1d-129">Einer der folgenden drei Tabellentypen kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="d7e1d-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="d7e1d-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="d7e1d-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="d7e1d-131">Der Inhalt der Tabelle ist dynamisch. Die Zeilen- und Spaltenwerte können sich ändern, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="d7e1d-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="d7e1d-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="d7e1d-133">Die Zeilen in der Tabelle sind fest, aber die Werte der Spalten in diesen Zeilen sind dynamisch und können sich ändern, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="d7e1d-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="d7e1d-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="d7e1d-135">Die Tabelle ist statisch, und ihr Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7e1d-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7e1d-136">Return value</span></span>

<span data-ttu-id="d7e1d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7e1d-137">S_OK</span></span> 
  
> <span data-ttu-id="d7e1d-138">Der Status der Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7e1d-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7e1d-139">Remarks</span></span>

<span data-ttu-id="d7e1d-140">Die **IMAPTable::GetStatus-Methode** ruft Informationen zum Typ und aktuellen Status einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d7e1d-141">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d7e1d-141">Notes to callers</span></span>

<span data-ttu-id="d7e1d-142">Sie können **GetStatus** zusammen mit drei anderen **IMAPITable-Methoden** verwenden, um den Status dieser Vorgänge zu überwachen und die Auswirkungen auf die Tabelle zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="d7e1d-143">Rufen **Sie GetStatus** nach einem der folgenden **IMAPITable-Aufrufe** auf:</span><span class="sxs-lookup"><span data-stu-id="d7e1d-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="d7e1d-144">[IMAPITable::Restrict,](imapitable-restrict.md) um eine Einschränkung festlegen.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="d7e1d-145">[IMAPITable::SortTable](imapitable-sorttable.md) zum Einrichten einer Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="d7e1d-146">[IMAPITable::SetColumns,](imapitable-setcolumns.md) um einen Spaltensatz zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7e1d-147">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d7e1d-147">MFCMAPI reference</span></span>

<span data-ttu-id="d7e1d-148">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7e1d-149">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d7e1d-149">**File**</span></span>|<span data-ttu-id="d7e1d-150">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d7e1d-150">**Function**</span></span>|<span data-ttu-id="d7e1d-151">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d7e1d-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7e1d-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d7e1d-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d7e1d-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="d7e1d-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="d7e1d-154">MFCMAPI verwendet die **IMAPITable::GetStatus-Methode,** um den Status einer Tabelle zu melden.</span><span class="sxs-lookup"><span data-stu-id="d7e1d-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7e1d-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7e1d-155">See also</span></span>



[<span data-ttu-id="d7e1d-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="d7e1d-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="d7e1d-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d7e1d-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="d7e1d-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d7e1d-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="d7e1d-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7e1d-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d7e1d-160">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d7e1d-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

