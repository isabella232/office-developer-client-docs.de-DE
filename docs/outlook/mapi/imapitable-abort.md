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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792443"
---
# <a name="imapitableabort"></a><span data-ttu-id="17703-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="17703-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="17703-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17703-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17703-105">Beendet die asynchrone Vorgänge derzeit in Arbeit für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="17703-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="17703-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17703-106">Parameters</span></span>

<span data-ttu-id="17703-107">Keine</span><span class="sxs-lookup"><span data-stu-id="17703-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="17703-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="17703-108">Return value</span></span>

<span data-ttu-id="17703-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="17703-109">S_OK</span></span> 
  
> <span data-ttu-id="17703-110">Eine oder mehrere asynchrone Vorgänge wurden angehalten.</span><span class="sxs-lookup"><span data-stu-id="17703-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="17703-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="17703-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="17703-112">Ein asynchroner Vorgang ist in Arbeit und kann nicht beendet werden oder wurde bereits abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="17703-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17703-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="17703-113">Remarks</span></span>

<span data-ttu-id="17703-114">Die **IMAPITable::Abort** -Methode beendet jede asynchrone Operation, die derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17703-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="17703-115">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="17703-115">Notes to callers</span></span>

<span data-ttu-id="17703-116">Um herauszufinden, ob eine asynchrone Operation ausgeführt wird, rufen Sie die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="17703-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="17703-117">**Abbrechen** die Verarbeitung von einem Aufruf der [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode wird angehalten, werden der Status der Tabelle zum Zeitpunkt wurde, die der Anruf **Abbrechen** verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="17703-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="17703-118">Wenn die Verarbeitung von einem Aufruf der [SortTable](imapitable-sorttable.md) -Methode **abgebrochen** wird angehalten, Sortierreihenfolge für die Tabelle nicht betroffenen und bleibt wie vor dem Aufruf der **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="17703-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17703-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17703-119">See also</span></span>



[<span data-ttu-id="17703-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="17703-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="17703-121">Methode IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="17703-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="17703-122">SortTable</span><span class="sxs-lookup"><span data-stu-id="17703-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="17703-123">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="17703-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
