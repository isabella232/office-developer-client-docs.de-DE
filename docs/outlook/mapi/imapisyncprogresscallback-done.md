---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792431"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="84c5a-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="84c5a-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="84c5a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84c5a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="84c5a-105">Microsoft Outlook informiert, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="84c5a-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="84c5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84c5a-106">Parameters</span></span>

 <span data-ttu-id="84c5a-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="84c5a-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="84c5a-108">Ein Ereignis, das zurück, um Microsoft Outlook können Sie das Handle Schließen zulassen übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="84c5a-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="84c5a-109">Es kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="84c5a-109">It can be NULL.</span></span>
    
 <span data-ttu-id="84c5a-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="84c5a-110">**hResult**</span></span>
  
> <span data-ttu-id="84c5a-111">Ein HRESULT Endstatus des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="84c5a-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84c5a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84c5a-112">Return value</span></span>

<span data-ttu-id="84c5a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="84c5a-113">S_OK</span></span> 
  
> <span data-ttu-id="84c5a-114">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="84c5a-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84c5a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c5a-115">See also</span></span>



[<span data-ttu-id="84c5a-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84c5a-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

