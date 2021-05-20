---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062032"
---
# <a name="imapiwaitresultend"></a><span data-ttu-id="fc73c-103">IMAPIWaitResult::End</span><span class="sxs-lookup"><span data-stu-id="fc73c-103">IMAPIWaitResult::End</span></span>
  
<span data-ttu-id="fc73c-104">**Gilt für**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="fc73c-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>

<span data-ttu-id="fc73c-105">Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fc73c-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="fc73c-106">INFINITE kann für unendliche Wartezeiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc73c-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="fc73c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc73c-107">Parameters</span></span>

<span data-ttu-id="fc73c-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="fc73c-108">_timeout_</span></span>
> <span data-ttu-id="fc73c-109">[in] Die Anzahl der Millisekunden, die auf die Initialisierung von MAPI gewartet werden sollen, können Sie INFINITE (0xFFFFFFFF) übergeben, um für immer zu warten.</span><span class="sxs-lookup"><span data-stu-id="fc73c-109">[in] The number of millisecond to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc73c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc73c-110">Return value</span></span>

<span data-ttu-id="fc73c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc73c-111">S_OK</span></span>
> <span data-ttu-id="fc73c-112">MAPI wurde erfolgreich initialisiert</span><span class="sxs-lookup"><span data-stu-id="fc73c-112">MAPI has been initialized successfully</span></span>

<span data-ttu-id="fc73c-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="fc73c-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="fc73c-114">Bei einem nicht unendlichen Timeout bedeutet dies, dass MAPI während dieses Zeitraums nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fc73c-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc73c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc73c-115">Remarks</span></span>
<span data-ttu-id="fc73c-116">Diese API verhält sich genauso wie [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span><span class="sxs-lookup"><span data-stu-id="fc73c-116">This API behaves exactly the same as [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc73c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc73c-117">See also</span></span>

[<span data-ttu-id="fc73c-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="fc73c-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="fc73c-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="fc73c-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="fc73c-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="fc73c-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="fc73c-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="fc73c-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
