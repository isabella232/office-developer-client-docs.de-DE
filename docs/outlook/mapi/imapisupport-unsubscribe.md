---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341265"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="1fba8-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1fba8-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="1fba8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fba8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fba8-105">Bricht die Zuständigkeit für das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPISupport:: subscribe](imapisupport-subscribe.md) -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="1fba8-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="1fba8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fba8-106">Parameters</span></span>

 <span data-ttu-id="1fba8-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="1fba8-107">_ulConnection_</span></span>
  
> <span data-ttu-id="1fba8-108">in Die ungleich NULL-Verbindungsnummer, die die Benachrichtigungs Registrierung darstellt, die zuvor über **IMAPISupport:: subscribe**eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="1fba8-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1fba8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fba8-109">Return value</span></span>

<span data-ttu-id="1fba8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fba8-110">S_OK</span></span> 
  
> <span data-ttu-id="1fba8-111">Die Benachrichtigungs Registrierung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1fba8-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="1fba8-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1fba8-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1fba8-113">Die im _ulConnection_ -Parameter übergebene Verbindungsnummer ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1fba8-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1fba8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fba8-114">Remarks</span></span>

<span data-ttu-id="1fba8-115">Die **IMAPISupport:: unsubscribe** -Methode wird für alle Support Objekte des Dienstanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="1fba8-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="1fba8-116">Dienstanbieter rufen das **Abonnement** ab, um eine zuvor von **subscribe**eingestellte Benachrichtigungs Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="1fba8-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="1fba8-117">Kündigen Sie das **Abonnement** , indem Sie den Zeiger für die Advise-Senke freigeben, der im **subscribe** -Aufruf übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1fba8-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="1fba8-118">Im Allgemeinen wird die **IUnknown:: Release** -Methode der Advise-Senke \*\*\*\* während des unsubscribe-Aufrufs aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1fba8-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="1fba8-119">Wenn jedoch ein anderer Thread die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das Advise-Senke-Objekt aufruft, wird der **Freigabe** Aufruf verzögert, bis \*\*\*\* die OnNotify-Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fba8-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1fba8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fba8-120">See also</span></span>



[<span data-ttu-id="1fba8-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="1fba8-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="1fba8-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="1fba8-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="1fba8-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1fba8-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

