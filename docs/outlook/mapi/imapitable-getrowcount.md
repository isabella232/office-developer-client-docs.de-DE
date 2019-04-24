---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328889"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="ff4b9-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="ff4b9-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="ff4b9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff4b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff4b9-105">Gibt die Gesamtanzahl der Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="ff4b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff4b9-106">Parameters</span></span>

 <span data-ttu-id="ff4b9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff4b9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ff4b9-108">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ff4b9-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="ff4b9-109">_lpulCount_</span></span>
  
> <span data-ttu-id="ff4b9-110">Out Zeiger auf die Anzahl der Zeilen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff4b9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff4b9-111">Return value</span></span>

<span data-ttu-id="ff4b9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff4b9-112">S_OK</span></span> 
  
> <span data-ttu-id="ff4b9-113">Die Zeilenanzahl wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="ff4b9-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ff4b9-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ff4b9-115">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Abrufvorgang für die Zeilenanzahl gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="ff4b9-116">Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="ff4b9-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ff4b9-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ff4b9-118">Die Tabelle kann die Anzahl der Zeilen nicht berechnen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="ff4b9-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="ff4b9-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="ff4b9-120">Der Aufruf war erfolgreich, aber eine ungefähre Zeilenanzahl wurde zurückgegeben, da die genaue Zeilenanzahl aufgrund von Arbeitsspeichereinschränkungen nicht bestimmt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="ff4b9-121">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ff4b9-122">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ff4b9-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff4b9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff4b9-123">Remarks</span></span>

<span data-ttu-id="ff4b9-124">Die **IMAPITable:: GetRowCount** -Methode ruft die Gesamtanzahl der Zeilen in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ff4b9-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ff4b9-125">Notes to implementers</span></span>

<span data-ttu-id="ff4b9-126">Wenn Sie die genaue Zeilenanzahl der Tabelle nicht bestimmen können, geben Sie MAPI_W_APPROX_COUNT und eine ungefähre Zeilenanzahl im Inhalt des _lpulCount_ -Parameters zurück.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff4b9-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ff4b9-127">Notes to callers</span></span>

<span data-ttu-id="ff4b9-128">Verwenden \*\*\*\* Sie GetRowCount, um herauszufinden, wie viele Zeilen eine Tabelle enthält, bevor Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode aufrufen, um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="ff4b9-129">Wenn die Tabelle weniger als zwanzig Zeilen enthält, können Sie **QueryPosition** aufrufen, um die gesamte Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="ff4b9-130">Wenn in der Tabelle mehr als zwanzig Zeilen vorhanden sind, sollten Sie mehrere Aufrufe an **QueryPosition** durchführen und die Anzahl der in jedem Aufruf abgerufenen Zeilen begrenzen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="ff4b9-131">Einige Tabellen unterstützen **GetRowCount** nicht und geben MAPI_E_NO_SUPPORT zurück.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="ff4b9-132">Wenn **GetRowCount** nicht unterstützt wird, können Sie [IMAPITable:: QueryPosition](imapitable-queryposition.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="ff4b9-133">Mit den Ergebnissen aus **QueryPosition**können Sie die Beziehung zwischen der aktuellen Zeile und der letzten Zeile bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="ff4b9-134">Wenn **GetRowCount** MAPI_E_BUSY zurückgibt, da es vorübergehend nicht in der Lage ist, eine Zeilenanzahl abzurufen, rufen Sie die [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="ff4b9-135">Wiederholen Sie den Aufruf von getRowCount, \*\*\*\* Wenn **WaitForCompletion** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="ff4b9-136">Sie können auch feststellen, ob eine asynchrone Operation ausgeführt wird, indem Sie die [IMAPITable:: GetStatus](imapitable-getstatus.md) -Methode aufrufen und den Inhalt des _lpulTableState_ -Parameters überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff4b9-137">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="ff4b9-137">MFCMAPI reference</span></span>

<span data-ttu-id="ff4b9-138">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff4b9-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ff4b9-139">**File**</span></span>|<span data-ttu-id="ff4b9-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ff4b9-140">**Function**</span></span>|<span data-ttu-id="ff4b9-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ff4b9-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff4b9-142">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="ff4b9-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ff4b9-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="ff4b9-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="ff4b9-144">MFCMAPI verwendet die **IMAPITable:: GetRowCount** -Methode, um zu bestimmen, wie viele Zeilen sich in der Quelltabelle befinden, damit der Arbeitsspeicher für die Kopie reserviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff4b9-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff4b9-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff4b9-145">See also</span></span>



[<span data-ttu-id="ff4b9-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="ff4b9-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="ff4b9-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="ff4b9-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="ff4b9-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ff4b9-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ff4b9-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ff4b9-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="ff4b9-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff4b9-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ff4b9-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ff4b9-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

