---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062018"
---
# <a name="imapiinitmonitorbeginwait"></a><span data-ttu-id="8aec1-103">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="8aec1-103">IMAPIInitMonitor::BeginWait</span></span>
  
<span data-ttu-id="8aec1-104">**Gilt für**: Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="8aec1-104">**Applies to**: Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="8aec1-105">Starten Sie eine Wartezeit auf die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden bis zum Verstreichen.</span><span class="sxs-lookup"><span data-stu-id="8aec1-105">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="8aec1-106">Dadurch wird eine IMAPIWaitResult-Schnittstelle zurückgegeben, auf die **IMAPIWaitResult::End** aufgerufen werden sollte, um das Warten zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="8aec1-106">This returns an IMAPIWaitResult interface which should have **IMAPIWaitResult::End** called in order initiate the wait.</span></span> <span data-ttu-id="8aec1-107">Dadurch kann der Aufrufer steuern, welcher Thread während der Wartezeit blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="8aec1-107">This allows the caller to control which thread is blocked while we are waiting.</span></span>

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a><span data-ttu-id="8aec1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8aec1-108">Parameters</span></span>
<span data-ttu-id="8aec1-109">_timeout_</span><span class="sxs-lookup"><span data-stu-id="8aec1-109">_timeout_</span></span>
><span data-ttu-id="8aec1-110">[in] Die Anzahl der Millisekunden, die auf die MAPI-Initialisierung gewartet werden müssen, kann auf INFINITE festgelegt werden, um für immer auf die Initialisierung zu warten.</span><span class="sxs-lookup"><span data-stu-id="8aec1-110">[in] The number of millisecond to wait for MAPI initialization, this can set to INFINITE to wait forever for the initialization to happen.</span></span>

<span data-ttu-id="8aec1-111">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="8aec1-111">_ppResult_</span></span>
><span data-ttu-id="8aec1-112">[out] Ein Zeiger zum Empfangen der neu erstellten Warteschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8aec1-112">[out] A pointer to recieve the newly create wait interface.</span></span>

## <a name="return-value"></a><span data-ttu-id="8aec1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8aec1-113">Return value</span></span>
<span data-ttu-id="8aec1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8aec1-114">S_OK</span></span>
><span data-ttu-id="8aec1-115">Ein Wartevorgang wurde erfolgreich gestartet.</span><span class="sxs-lookup"><span data-stu-id="8aec1-115">A wait operation was successfully started.</span></span>

<span data-ttu-id="8aec1-116">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8aec1-116">E_OUTOFMEMORY</span></span>
><span data-ttu-id="8aec1-117">Es war nicht genügend Arbeitsspeicher vorhanden, um ein neues Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8aec1-117">There was not enough memory to create a new object</span></span>

## <a name="remarks"></a><span data-ttu-id="8aec1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8aec1-118">Remarks</span></span>
<span data-ttu-id="8aec1-119">Diese API hat dem Aufrufer eine Schnittstelle (threadsicher) bereitgestellt, die verwendet werden kann, um eine Blockierungswarte warten auf die MAPI-Initialisierung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="8aec1-119">This API provided the caller with an interface (which is thread-safe) which can be used initiate a blocking wait for MAPI initialization.</span></span> <span data-ttu-id="8aec1-120">Auf diese Weise kann der Verbraucher am besten auf die Anwendung warten.</span><span class="sxs-lookup"><span data-stu-id="8aec1-120">This allows the consumer to deterime the best wait to wait for thier application.</span></span>   <span data-ttu-id="8aec1-121">Das Verhalten des Aufrufens von IMAPIWaitResult::End ist identisch mit dem Aufrufen von IMAPIInitMonitor::Wait.</span><span class="sxs-lookup"><span data-stu-id="8aec1-121">The behavior of calling IMAPIWaitResult::End is identical to calling IMAPIInitMonitor::Wait.</span></span>

## <a name="see-also"></a><span data-ttu-id="8aec1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aec1-122">See also</span></span>

[<span data-ttu-id="8aec1-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="8aec1-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="8aec1-124">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="8aec1-124">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="8aec1-125">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="8aec1-125">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="8aec1-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="8aec1-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="8aec1-127">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="8aec1-127">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
