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
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407060"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="dfbf8-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="dfbf8-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="dfbf8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfbf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfbf8-105">Hält die Verarbeitung an, bis mindestens ein asynchroner Vorgang abgeschlossen ist, der in der Tabelle ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="dfbf8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfbf8-106">Parameters</span></span>

 <span data-ttu-id="dfbf8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfbf8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dfbf8-108">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="dfbf8-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="dfbf8-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="dfbf8-110">in Maximale Anzahl von Millisekunden, die gewartet werden soll, bis der asynchrone Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="dfbf8-111">Wenn auf unbestimmte Zeit gewartet werden soll, bis der Abschluss auftritt, legen Sie _ulTimeout_ auf 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="dfbf8-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="dfbf8-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="dfbf8-113">[in, out] Bei der Eingabe ein gültiger Zeiger oder NULL.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="dfbf8-114">Wenn _lpulTableStatus_ ein gültiger Zeiger ist, zeigt er auf den letzten Status der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="dfbf8-115">Wenn _lpulTableStatus_ ist, werden keine Statusinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="dfbf8-116">Wenn **WaitForCompletion** einen nicht erfolgreichen HRESULT-Wert zurückgibt, sind die Inhalte von _lpulTableStatus_ nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dfbf8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfbf8-117">Return value</span></span>

<span data-ttu-id="dfbf8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfbf8-118">S_OK</span></span> 
  
> <span data-ttu-id="dfbf8-119">Der Wartevorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="dfbf8-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dfbf8-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dfbf8-121">Die Tabelle unterstützt nicht das warten auf den Abschluss von asynchronen Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="dfbf8-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="dfbf8-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="dfbf8-123">Der asynchrone Vorgang oder die Vorgänge wurden nicht in der angegebenen Zeit abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfbf8-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfbf8-124">Remarks</span></span>

<span data-ttu-id="dfbf8-125">Mit der **IMAPITable:: WaitForCompletion** -Methode wird die Verarbeitung angehalten, bis alle asynchronen Vorgänge, die für die Tabelle ausgeführt werden, abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="dfbf8-126">**WaitForCompletion** kann die asynchrone Vorgänge vollständig abgeschlossen oder für eine bestimmte Anzahl von Millisekunden ausgeführt, wie durch _ulTimeout_, bevor Sie unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="dfbf8-127">Um asynchrone Vorgänge zu finden, die ausgeführt werden, rufen Sie die [IMAPITable:: GetStatus](imapitable-getstatus.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfbf8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfbf8-128">See also</span></span>



[<span data-ttu-id="dfbf8-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="dfbf8-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="dfbf8-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="dfbf8-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="dfbf8-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="dfbf8-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="dfbf8-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="dfbf8-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="dfbf8-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="dfbf8-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="dfbf8-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfbf8-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

