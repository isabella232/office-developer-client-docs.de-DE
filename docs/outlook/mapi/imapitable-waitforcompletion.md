---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3343381709b7ce3370ba481ad8dbb935c7d4165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586949"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="17ae4-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="17ae4-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="17ae4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17ae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17ae4-105">Unterbricht die Verarbeitung, bis eine oder mehrere asynchrone Vorgänge in Bearbeitung in der Tabelle abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="17ae4-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="17ae4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17ae4-106">Parameters</span></span>

 <span data-ttu-id="17ae4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="17ae4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="17ae4-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="17ae4-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="17ae4-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="17ae4-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="17ae4-110">[in] Maximale Anzahl von Millisekunden zu warten, bis der asynchrone Vorgang oder Vorgänge abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="17ae4-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="17ae4-111">Legen Sie zum Warten auf unbestimmte Zeit, bis Abschluss auftritt, _UlTimeout_ auf 0xFFFFFFFF ein.</span><span class="sxs-lookup"><span data-stu-id="17ae4-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="17ae4-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="17ae4-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="17ae4-113">[in, out] Bei der Eingabe ein gültiger Zeiger oder NULL.</span><span class="sxs-lookup"><span data-stu-id="17ae4-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="17ae4-114">Bei der Ausgabe ist _LpulTableStatus_ gültiger Zeiger ist, zeigt es auf den aktuellen Status der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="17ae4-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="17ae4-115">Wenn _LpulTableStatus_ NULL ist, werden keine Statusinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17ae4-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="17ae4-116">Wenn **WaitForCompletion** nicht erfolgreichen HRESULT-Wert zurückgibt, sind der Inhalt der _LpulTableStatus_ nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="17ae4-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="17ae4-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="17ae4-117">Return value</span></span>

<span data-ttu-id="17ae4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="17ae4-118">S_OK</span></span> 
  
> <span data-ttu-id="17ae4-119">Der Wait-Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="17ae4-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="17ae4-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="17ae4-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="17ae4-121">Die Tabelle unterstützt keine Anzeige für wartende für den Abschluss der asynchronen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="17ae4-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="17ae4-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="17ae4-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="17ae4-123">Die asynchrone Operation oder Vorgänge wurde nicht in der angegebenen Zeit abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="17ae4-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17ae4-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="17ae4-124">Remarks</span></span>

<span data-ttu-id="17ae4-125">Die Methode **IMAPITable::WaitForCompletion** hält die Verarbeitung, bis alle derzeit asynchrone Vorgänge für die Tabelle abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="17ae4-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="17ae4-126">**WaitForCompletion** können die asynchrone Vorgänge entweder vollständig abgeschlossen oder für eine bestimmte Anzahl von Millisekunden auszuführen, wie _UlTimeout_, abgebrochen wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="17ae4-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="17ae4-127">Zum Erkennen von asynchrone Vorgänge in Bearbeitung rufen Sie die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="17ae4-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17ae4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17ae4-128">See also</span></span>



[<span data-ttu-id="17ae4-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="17ae4-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="17ae4-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="17ae4-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="17ae4-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="17ae4-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="17ae4-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="17ae4-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="17ae4-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="17ae4-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="17ae4-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17ae4-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

