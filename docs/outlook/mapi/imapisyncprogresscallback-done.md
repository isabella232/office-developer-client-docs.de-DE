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
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573208"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="924fa-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="924fa-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="924fa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="924fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="924fa-105">Microsoft Outlook informiert, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="924fa-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="924fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="924fa-106">Parameters</span></span>

 <span data-ttu-id="924fa-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="924fa-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="924fa-108">Ein Ereignis, das zurück, um Microsoft Outlook können Sie das Handle Schließen zulassen übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="924fa-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="924fa-109">Es kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="924fa-109">It can be NULL.</span></span>
    
 <span data-ttu-id="924fa-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="924fa-110">**hResult**</span></span>
  
> <span data-ttu-id="924fa-111">Ein HRESULT Endstatus des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="924fa-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="924fa-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="924fa-112">Return value</span></span>

<span data-ttu-id="924fa-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="924fa-113">S_OK</span></span> 
  
> <span data-ttu-id="924fa-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="924fa-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="924fa-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="924fa-115">See also</span></span>



[<span data-ttu-id="924fa-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="924fa-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

