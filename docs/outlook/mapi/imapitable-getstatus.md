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
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792472"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="6fc2a-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="6fc2a-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="6fc2a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fc2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fc2a-105">Status und Typ der Tabelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="6fc2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fc2a-106">Parameters</span></span>

 <span data-ttu-id="6fc2a-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="6fc2a-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="6fc2a-108">[out] Zeiger auf einen Wert, der den Status der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="6fc2a-109">Die folgenden Werte kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6fc2a-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="6fc2a-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="6fc2a-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="6fc2a-111">Keine Vorgänge werden durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-111">No operations are in progress.</span></span>
    
<span data-ttu-id="6fc2a-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="6fc2a-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="6fc2a-113">Der Inhalt der Tabelle haben expectantly geändert.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="6fc2a-114">Dieser Statuswert wird nicht für Änderungen zurückgegeben, die aus sortieren oder Einschränkung Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="6fc2a-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="6fc2a-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="6fc2a-116">Während eines Vorgangs [Methode IMAPITable:: Restrict](imapitable-restrict.md) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="6fc2a-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="6fc2a-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="6fc2a-118">Ein **Methode IMAPITable:: Restrict** -Vorgang wird gerade durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="6fc2a-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="6fc2a-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="6fc2a-120">Während eines Vorgangs [IMAPITable::SetColumns](imapitable-setcolumns.md) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="6fc2a-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="6fc2a-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="6fc2a-122">Ein **IMAPITable::SetColumns** Vorgang ist in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="6fc2a-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="6fc2a-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="6fc2a-124">Während eines Vorgangs [SortTable](imapitable-sorttable.md) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="6fc2a-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="6fc2a-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="6fc2a-126">Ein Vorgang **SortTable** wird gerade durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="6fc2a-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="6fc2a-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="6fc2a-128">[out] Zeiger auf einen Wert vom Typ der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="6fc2a-129">Eine der folgenden drei Tabelle kann zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="6fc2a-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="6fc2a-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="6fc2a-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="6fc2a-131">Die Tabelle Inhalt sind dynamisch; die Zeilen und Spaltenwerte können die zugrunde liegenden Daten geändert ändern.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="6fc2a-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="6fc2a-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="6fc2a-133">Die Zeilen innerhalb der Tabelle behoben werden, aber die Werte der Spalten in diesen Zeilen sind dynamisch und ändern können, als die zugrunde liegenden Daten geändert.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="6fc2a-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="6fc2a-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="6fc2a-135">Die Tabelle sind statisch, und dessen Inhalt nicht ändern, wenn die zugrunde liegenden Daten geändert.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fc2a-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fc2a-136">Return value</span></span>

<span data-ttu-id="6fc2a-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fc2a-137">S_OK</span></span> 
  
> <span data-ttu-id="6fc2a-138">Die Tabelle Status wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fc2a-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fc2a-139">Remarks</span></span>

<span data-ttu-id="6fc2a-140">Die **IMAPTable::GetStatus** -Methode ruft Informationen über den Typ und den aktuellen Status einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6fc2a-141">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6fc2a-141">Notes to callers</span></span>

<span data-ttu-id="6fc2a-142">Sie können **GetStatus** in Verbindung mit drei **IMAPITable** -Methoden verwenden, den Status von Vorgängen überwachen und bestimmen die Auswirkung auf die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="6fc2a-143">Rufen Sie nach dem Ändern eines der folgenden **IMAPITable** Aufrufe **GetStatus** :</span><span class="sxs-lookup"><span data-stu-id="6fc2a-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="6fc2a-144">[Methode IMAPITable:: Restrict](imapitable-restrict.md) eine Einschränkung festlegen.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="6fc2a-145">[SortTable](imapitable-sorttable.md) keine Sortierreihenfolge herstellen.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="6fc2a-146">Legen Sie [IMAPITable::SetColumns](imapitable-setcolumns.md) für eine Spalte definieren.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6fc2a-147">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6fc2a-147">MFCMAPI reference</span></span>

<span data-ttu-id="6fc2a-148">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6fc2a-149">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6fc2a-149">**File**</span></span>|<span data-ttu-id="6fc2a-150">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6fc2a-150">**Function**</span></span>|<span data-ttu-id="6fc2a-151">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6fc2a-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fc2a-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="6fc2a-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="6fc2a-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="6fc2a-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="6fc2a-154">MFCMAPI (engl.) wird die **IMAPITable::GetStatus** -Methode verwendet, um den Status einer Tabelle Berichten.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fc2a-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc2a-155">See also</span></span>



[<span data-ttu-id="6fc2a-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="6fc2a-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="6fc2a-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6fc2a-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6fc2a-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="6fc2a-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="6fc2a-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fc2a-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="6fc2a-160">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6fc2a-160">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

