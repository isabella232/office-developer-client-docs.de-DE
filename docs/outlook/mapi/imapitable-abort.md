---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406150"
---
# <a name="imapitableabort"></a><span data-ttu-id="3fb3d-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="3fb3d-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="3fb3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fb3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fb3d-105">Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="3fb3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fb3d-106">Parameters</span></span>

<span data-ttu-id="3fb3d-107">Keine</span><span class="sxs-lookup"><span data-stu-id="3fb3d-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3fb3d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fb3d-108">Return value</span></span>

<span data-ttu-id="3fb3d-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fb3d-109">S_OK</span></span> 
  
> <span data-ttu-id="3fb3d-110">Mindestens ein asynchroner Vorgang wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="3fb3d-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="3fb3d-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="3fb3d-112">Ein asynchroner Vorgang wird ausgeführt und kann nicht beendet oder bereits abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fb3d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3fb3d-113">Remarks</span></span>

<span data-ttu-id="3fb3d-114">Die **IMAPITable::Abort-Methode** beendet alle asynchronen Vorgänge, die derzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3fb3d-115">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3fb3d-115">Notes to callers</span></span>

<span data-ttu-id="3fb3d-116">Um herauszufinden, ob ein asynchroner Vorgang ausgeführt wird, rufen Sie die [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) auf.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="3fb3d-117">Wenn **Abort** die Verarbeitung eines Aufrufs der [IMAPITable::Restrict-Methode](imapitable-restrict.md) beendet, ist der Zustand der Tabelle so wie zum Zeitpunkt der Verarbeitung des **Abbruchaufrufs.**</span><span class="sxs-lookup"><span data-stu-id="3fb3d-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="3fb3d-118">Wenn **Abort** die Verarbeitung eines Aufrufs der [IMAPITable::SortTable-Methode](imapitable-sorttable.md) beendet, ist die Sortierreihenfolge der Tabelle nicht betroffen und bleibt unverändert wie vor dem **SortTable-Aufruf.**</span><span class="sxs-lookup"><span data-stu-id="3fb3d-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3fb3d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fb3d-119">See also</span></span>



[<span data-ttu-id="3fb3d-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="3fb3d-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="3fb3d-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3fb3d-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="3fb3d-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3fb3d-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="3fb3d-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fb3d-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

