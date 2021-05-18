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
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422348"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="9c74b-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="9c74b-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="9c74b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c74b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9c74b-105">Informiert Microsoft Outlook, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9c74b-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="9c74b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c74b-106">Parameters</span></span>

 <span data-ttu-id="9c74b-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="9c74b-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="9c74b-108">Ein Ereignis, das übergeben wird, damit Microsoft Outlook handle schließen kann.</span><span class="sxs-lookup"><span data-stu-id="9c74b-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="9c74b-109">Er kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9c74b-109">It can be NULL.</span></span>
    
 <span data-ttu-id="9c74b-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="9c74b-110">**hResult**</span></span>
  
> <span data-ttu-id="9c74b-111">Ein HRESULT, das den endgültigen Status des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="9c74b-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c74b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c74b-112">Return value</span></span>

<span data-ttu-id="9c74b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c74b-113">S_OK</span></span> 
  
> <span data-ttu-id="9c74b-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9c74b-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c74b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c74b-115">See also</span></span>



[<span data-ttu-id="9c74b-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c74b-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

