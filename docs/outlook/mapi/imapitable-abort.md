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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328949"
---
# <a name="imapitableabort"></a><span data-ttu-id="1dbeb-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="1dbeb-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="1dbeb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dbeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dbeb-105">Beendet alle asynchronen Vorgänge, die derzeit für die Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="1dbeb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dbeb-106">Parameters</span></span>

<span data-ttu-id="1dbeb-107">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbeb-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1dbeb-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dbeb-108">Return value</span></span>

<span data-ttu-id="1dbeb-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="1dbeb-109">S_OK</span></span> 
  
> <span data-ttu-id="1dbeb-110">Mindestens ein asynchroner Vorgang wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="1dbeb-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="1dbeb-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="1dbeb-112">Ein asynchroner Vorgang wird ausgeführt und kann nicht beendet oder bereits abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1dbeb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dbeb-113">Remarks</span></span>

<span data-ttu-id="1dbeb-114">Die **IMAPITable:: Abort** -Methode beendet alle asynchronen Vorgänge, die derzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1dbeb-115">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1dbeb-115">Notes to callers</span></span>

<span data-ttu-id="1dbeb-116">Wenn Sie herausfinden möchten, ob ein asynchroner Vorgang ausgeführt wird, rufen Sie die [IMAPITable:: GetStatus](imapitable-getstatus.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="1dbeb-117">Wenn **Abbruch** die Verarbeitung eines Aufrufs der [IMAPITable:: Restrict](imapitable-restrict.md) -Methode angehalten wird, ist der Status der Tabelle, wie zum Zeitpunkt der **Abbruch** Aufruf verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="1dbeb-118">Wenn **Abbruch** die Verarbeitung eines Aufrufs der [IMAPITable:: sortable](imapitable-sorttable.md) -Methode angehalten wird, ist die Sortierreihenfolge der Tabelle nicht betroffen und bleibt unverändert, wie es vor dem **sortable** -Aufruf war.</span><span class="sxs-lookup"><span data-stu-id="1dbeb-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1dbeb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dbeb-119">See also</span></span>



[<span data-ttu-id="1dbeb-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="1dbeb-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="1dbeb-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="1dbeb-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="1dbeb-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="1dbeb-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="1dbeb-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1dbeb-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

