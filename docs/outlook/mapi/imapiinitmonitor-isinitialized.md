---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062025"
---
# <a name="imapiinitmonitorisinitialized"></a><span data-ttu-id="2cbcb-103">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="2cbcb-103">IMAPIInitMonitor::IsInitialized</span></span>
  
<span data-ttu-id="2cbcb-104">**Gilt für**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="2cbcb-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="2cbcb-105">Fragt MAPI ab, um zu ermitteln, ob es derzeit im aufrufenden Prozess initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbcb-105">Queries MAPI to determine if it currently initialized in the calling process.</span></span>

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a><span data-ttu-id="2cbcb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cbcb-106">Parameters</span></span>
<span data-ttu-id="2cbcb-107">Keine</span><span class="sxs-lookup"><span data-stu-id="2cbcb-107">None</span></span>

## <a name="return-value"></a><span data-ttu-id="2cbcb-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cbcb-108">Return value</span></span>
<span data-ttu-id="2cbcb-109">Ein BOOL, der den aktuellen Zustand der MAPI-Initialisierung angibt, ein Wert von TRUE bedeutet, dass MAPI initialisiert wurde und zur Verwendung verfügbar ist, während der Wert FALSE bedeutet, dass MAPI aktuell nicht initialisiert ist und nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2cbcb-109">A BOOL indicating the current state of MAPI initialization, a value of TRUE means MAPI has been initialized and is available for use, while a value of FALSE means MAPI is currenty uninitialized and is not ready be consumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbcb-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2cbcb-110">Remarks</span></span>
<span data-ttu-id="2cbcb-111">Dies kann verwendet werden, um zu ermitteln, ob MAPI einsatzbereit ist, z. B. wenn Ihre Anwendung nur dann etwas tun wollte, wenn MAPI bereits initialisiert wurde, könnte dies eine nützliche Überprüfung einer Hintergrundaufgabe sein, um die Kosten für das Drehen von MAPI für optionale Arbeit zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="2cbcb-111">This can be used to determine if MAPI is ready to be used, for example, if your application wanted to do something only if MAPI has already be initialized, this could be a useful check in a background task to prevent the cost of spinning up MAPI for optional work.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cbcb-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cbcb-112">See also</span></span>

[<span data-ttu-id="2cbcb-113">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="2cbcb-113">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="2cbcb-114">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="2cbcb-114">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
