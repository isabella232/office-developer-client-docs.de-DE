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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792468"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="e4f1a-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="e4f1a-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="e4f1a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4f1a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4f1a-105">Gibt die Gesamtzahl der Zeilen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="e4f1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4f1a-106">Parameters</span></span>

 <span data-ttu-id="e4f1a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4f1a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e4f1a-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e4f1a-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="e4f1a-109">_lpulCount_</span></span>
  
> <span data-ttu-id="e4f1a-110">[out] Zeiger auf die Anzahl der Zeilen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4f1a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4f1a-111">Return value</span></span>

<span data-ttu-id="e4f1a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4f1a-112">S_OK</span></span> 
  
> <span data-ttu-id="e4f1a-113">Die Anzahl der Zeilen wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="e4f1a-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e4f1a-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e4f1a-115">Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang Count Zeile nicht gestartet dass.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="e4f1a-116">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="e4f1a-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e4f1a-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e4f1a-118">Die Tabelle kann die Anzahl der Zeilen nicht berechnen.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="e4f1a-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="e4f1a-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="e4f1a-120">Der Aufruf war erfolgreich, aber eine ungefähre Zeilenanzahl wurde zurückgegeben, da die genaue Zeilenanzahl nicht möglicherweise aufgrund der Speicherkapazität ermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="e4f1a-121">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e4f1a-122">Finden Sie unter [Verwendung von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e4f1a-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4f1a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4f1a-123">Remarks</span></span>

<span data-ttu-id="e4f1a-124">Die **IMAPITable::GetRowCount** -Methode ruft die Gesamtzahl der Zeilen in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e4f1a-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e4f1a-125">Notes to implementers</span></span>

<span data-ttu-id="e4f1a-126">Wenn Sie die Tabelle genauen Zeilenanzahl ermitteln können, zählen return MAPI_W_APPROX_COUNT und eine ungefähre Zeile in den Inhalt des Parameters _LpulCount_ .</span><span class="sxs-lookup"><span data-stu-id="e4f1a-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e4f1a-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e4f1a-127">Notes to callers</span></span>

<span data-ttu-id="e4f1a-128">Verwendung **GetRowCount** um zu erfahren, wie viele Zeilen eine Tabelle enthält vor dem tätigen eines Anrufs auf [die QueryRows](imapitable-queryrows.md) zum Abrufen der Daten.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="e4f1a-129">Wenn weniger als 20 Zeilen in der Tabelle vorhanden sind, ist es sicherer **QueryPosition** zum Abrufen der gesamten Tabelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="e4f1a-130">Wenn mehr als 20 Zeilen in der Tabelle vorhanden sind, sollten Sie mehrere Aufrufe von **QueryPosition** und die Anzahl der Zeilen, die in jedem Aufruf abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="e4f1a-131">Einige Tabellen nicht unterstützen **GetRowCount** und MAPI_E_NO_SUPPORT zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="e4f1a-132">Wenn **GetRowCount** nicht unterstützt wird, möglicherweise eine Alternative [IMAPITable::QueryPosition](imapitable-queryposition.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="e4f1a-133">Mit den Ergebnissen von **QueryPosition**können Sie die Beziehung zwischen der aktuellen Zeile und die letzte Zeile bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="e4f1a-134">Wenn **GetRowCount** MAPI_E_BUSY zurückgegeben, da es vorübergehend nicht zum Abrufen der Zeilenanzahl ist, rufen Sie die [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="e4f1a-135">Wenn **WaitForCompletion** zurückgegeben wird, wiederholen Sie den Anruf an **GetRowCount**.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="e4f1a-136">Eine andere Möglichkeit, erkennen, ob eine asynchrone Operation ausgeführt wird, ist die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode aufrufen, und überprüfen Sie den Inhalt des Parameters _LpulTableState_ .</span><span class="sxs-lookup"><span data-stu-id="e4f1a-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e4f1a-137">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="e4f1a-137">MFCMAPI reference</span></span>

<span data-ttu-id="e4f1a-138">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e4f1a-139">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e4f1a-139">**File**</span></span>|<span data-ttu-id="e4f1a-140">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e4f1a-140">**Function**</span></span>|<span data-ttu-id="e4f1a-141">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e4f1a-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4f1a-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e4f1a-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e4f1a-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="e4f1a-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="e4f1a-144">MFCMAPI (engl.) verwendet die **IMAPITable::GetRowCount** -Methode, um zu bestimmen, wie viele Zeilen in der Quelltabelle werden, damit Speicher zugewiesen werden kann, um den Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="e4f1a-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4f1a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4f1a-145">See also</span></span>



[<span data-ttu-id="e4f1a-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="e4f1a-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="e4f1a-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="e4f1a-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="e4f1a-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e4f1a-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e4f1a-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e4f1a-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="e4f1a-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4f1a-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e4f1a-151">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e4f1a-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

