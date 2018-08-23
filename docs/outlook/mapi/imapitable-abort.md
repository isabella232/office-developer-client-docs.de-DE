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
ms.openlocfilehash: 68d40a6e152698554fcb88c6f7e5bfd4a7ff0ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574006"
---
# <a name="imapitableabort"></a><span data-ttu-id="0a330-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="0a330-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="0a330-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a330-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a330-105">Beendet die asynchrone Vorgänge derzeit in Arbeit für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0a330-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="0a330-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a330-106">Parameters</span></span>

<span data-ttu-id="0a330-107">Keine</span><span class="sxs-lookup"><span data-stu-id="0a330-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0a330-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0a330-108">Return value</span></span>

<span data-ttu-id="0a330-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a330-109">S_OK</span></span> 
  
> <span data-ttu-id="0a330-110">Eine oder mehrere asynchrone Vorgänge wurden angehalten.</span><span class="sxs-lookup"><span data-stu-id="0a330-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="0a330-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="0a330-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="0a330-112">Ein asynchroner Vorgang ist in Arbeit und kann nicht beendet werden oder wurde bereits abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0a330-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a330-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0a330-113">Remarks</span></span>

<span data-ttu-id="0a330-114">Die **IMAPITable::Abort** -Methode beendet jede asynchrone Operation, die derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a330-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0a330-115">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0a330-115">Notes to callers</span></span>

<span data-ttu-id="0a330-116">Um herauszufinden, ob eine asynchrone Operation ausgeführt wird, rufen Sie die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0a330-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="0a330-117">**Abbrechen** die Verarbeitung von einem Aufruf der [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode wird angehalten, werden der Status der Tabelle zum Zeitpunkt wurde, die der Anruf **Abbrechen** verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0a330-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="0a330-118">Wenn die Verarbeitung von einem Aufruf der [SortTable](imapitable-sorttable.md) -Methode **abgebrochen** wird angehalten, Sortierreihenfolge für die Tabelle nicht betroffenen und bleibt wie vor dem Aufruf der **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="0a330-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a330-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a330-119">See also</span></span>



[<span data-ttu-id="0a330-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="0a330-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="0a330-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="0a330-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="0a330-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="0a330-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="0a330-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a330-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

