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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328896"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="37473-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="37473-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="37473-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37473-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37473-105">Gibt den Status und den Typ der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="37473-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="37473-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37473-106">Parameters</span></span>

 <span data-ttu-id="37473-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="37473-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="37473-108">Out Zeiger auf einen Wert, der den Status der Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="37473-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="37473-109">Einer der folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="37473-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="37473-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="37473-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="37473-111">Es werden keine Vorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37473-111">No operations are in progress.</span></span>
    
<span data-ttu-id="37473-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="37473-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="37473-113">Der Inhalt der Tabelle wurde erwartungsvoll geändert.</span><span class="sxs-lookup"><span data-stu-id="37473-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="37473-114">Dieser Statuswert wird nicht für Änderungen zurückgegeben, die aus Sortier-oder Einschränkungs Vorgängen resultieren.</span><span class="sxs-lookup"><span data-stu-id="37473-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="37473-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="37473-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="37473-116">Während eines [IMAPITable:: Restrict](imapitable-restrict.md) -Vorgangs ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37473-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="37473-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="37473-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="37473-118">Ein **IMAPITable:: Restrict** -Vorgang wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37473-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="37473-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="37473-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="37473-120">Während eines [IMAPITable::](imapitable-setcolumns.md) SetColumns-Vorgangs ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37473-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="37473-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="37473-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="37473-122">Ein **IMAPITable::** SetColumns-Vorgang wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37473-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="37473-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="37473-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="37473-124">Während eines [IMAPITable:: sortable](imapitable-sorttable.md) -Vorgangs ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37473-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="37473-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="37473-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="37473-126">Ein **IMAPITable:: sortable** -Vorgang wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37473-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="37473-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="37473-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="37473-128">Out Zeiger auf einen Wert, der den Typ der Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="37473-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="37473-129">Einer der folgenden drei Tabellentypen kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="37473-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="37473-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="37473-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="37473-131">Der Inhalt der Tabelle ist dynamisch; die Zeilen-und Spaltenwerte können sich ändern, wenn die zugrunde liegenden Daten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37473-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="37473-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="37473-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="37473-133">Die Zeilen in der Tabelle sind festgelegt, aber die Werte der Spalten innerhalb dieser Zeilen sind dynamisch und können geändert werden, wenn die zugrunde liegenden Daten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37473-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="37473-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="37473-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="37473-135">Die Tabelle ist statisch, und ihr Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="37473-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37473-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37473-136">Return value</span></span>

<span data-ttu-id="37473-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="37473-137">S_OK</span></span> 
  
> <span data-ttu-id="37473-138">Der Status der Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37473-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37473-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37473-139">Remarks</span></span>

<span data-ttu-id="37473-140">Die **imapable:: GetStatus** -Methode ruft Informationen über den Typ einer Tabelle und den aktuellen Status ab.</span><span class="sxs-lookup"><span data-stu-id="37473-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="37473-141">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="37473-141">Notes to callers</span></span>

<span data-ttu-id="37473-142">Sie können **GetStatus** in Verbindung mit drei anderen **IMAPITable** -Methoden verwenden, um den Status dieser Vorgänge zu überwachen und die Auswirkungen auf die Tabelle zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="37473-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="37473-143">Rufen \*\*\*\* Sie GetStatus auf, nachdem Sie einen der folgenden **IMAPITable** -Aufrufe durchführen:</span><span class="sxs-lookup"><span data-stu-id="37473-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="37473-144">[IMAPITable:: einschränken](imapitable-restrict.md) , um eine Einschränkung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="37473-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="37473-145">[IMAPITable:: sortable](imapitable-sorttable.md) , um eine Sortierreihenfolge einzurichten.</span><span class="sxs-lookup"><span data-stu-id="37473-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="37473-146">[IMAPITable::](imapitable-setcolumns.md) SetColumns zum Definieren eines Spaltensatzes.</span><span class="sxs-lookup"><span data-stu-id="37473-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="37473-147">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="37473-147">MFCMAPI reference</span></span>

<span data-ttu-id="37473-148">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="37473-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37473-149">**Datei**</span><span class="sxs-lookup"><span data-stu-id="37473-149">**File**</span></span>|<span data-ttu-id="37473-150">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="37473-150">**Function**</span></span>|<span data-ttu-id="37473-151">**Comment**</span><span class="sxs-lookup"><span data-stu-id="37473-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37473-152">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="37473-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="37473-153">CContentsTableListCtrl:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="37473-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="37473-154">MFCMAPI verwendet die **IMAPITable:: GetStatus** -Methode, um den Status einer Tabelle zu melden.</span><span class="sxs-lookup"><span data-stu-id="37473-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37473-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37473-155">See also</span></span>



[<span data-ttu-id="37473-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="37473-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="37473-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="37473-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="37473-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="37473-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="37473-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37473-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="37473-160">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="37473-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

