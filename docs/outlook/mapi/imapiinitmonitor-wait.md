---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062011"
---
# <a name="imapiinitmonitorwait"></a><span data-ttu-id="140c8-103">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="140c8-103">IMAPIInitMonitor::Wait</span></span>
  
<span data-ttu-id="140c8-104">**Gilt für**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="140c8-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="140c8-105">Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="140c8-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="140c8-106">INFINITE kann für unendliche Wartezeiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="140c8-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="140c8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="140c8-107">Parameters</span></span>
<span data-ttu-id="140c8-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="140c8-108">_timeout_</span></span>
> <span data-ttu-id="140c8-109">[in] Die Anzahl der Millisekunden, die auf die Initialisierung von MAPI gewartet werden müssen, können Sie INFINITE (0xFFFFFFFF) übergeben, um für immer zu warten.</span><span class="sxs-lookup"><span data-stu-id="140c8-109">[in] The number of milliseconds to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="140c8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="140c8-110">Return value</span></span>

<span data-ttu-id="140c8-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="140c8-111">S_OK</span></span>
> <span data-ttu-id="140c8-112">MAPI wurde erfolgreich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="140c8-112">MAPI has been initialized successfully.</span></span>

<span data-ttu-id="140c8-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="140c8-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="140c8-114">Bei einem nicht unendlichen Timeout bedeutet dies, dass MAPI während dieses Zeitraums nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="140c8-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="140c8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="140c8-115">Remarks</span></span>
  
## <a name="see-also"></a><span data-ttu-id="140c8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="140c8-116">See also</span></span>

[<span data-ttu-id="140c8-117">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="140c8-117">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="140c8-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="140c8-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="140c8-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="140c8-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="140c8-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="140c8-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="140c8-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="140c8-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
