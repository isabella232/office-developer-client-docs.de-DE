---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594985"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="d8bc6-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="d8bc6-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="d8bc6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8bc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8bc6-105">Ausführliche Informationen, die im Dialogfeld Senden/Empfangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="d8bc6-106">Wenn während der Synchronisierung Fehler auftreten, ruft der Anbieter diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="d8bc6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8bc6-107">Parameters</span></span>

 <span data-ttu-id="d8bc6-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="d8bc6-108">**hResult**</span></span>
  
> <span data-ttu-id="d8bc6-109">Das HRESULT des Fehlers oder der Warnung.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="d8bc6-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="d8bc6-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="d8bc6-111">Ein Zeiger auf die Zeichenfolge, die die anzuzeigende Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8bc6-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d8bc6-112">Return value</span></span>

<span data-ttu-id="d8bc6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8bc6-113">S_OK</span></span> 
  
> <span data-ttu-id="d8bc6-114">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d8bc6-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8bc6-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8bc6-115">See also</span></span>



[<span data-ttu-id="d8bc6-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8bc6-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

