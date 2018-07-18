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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792433"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="10559-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="10559-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="10559-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10559-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10559-105">Hebt die Verantwortung für Benachrichtigungen gesendet werden, die zuvor mit einem Aufruf der [IMAPISupport::Subscribe](imapisupport-subscribe.md) -Methode festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="10559-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="10559-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10559-106">Parameters</span></span>

 <span data-ttu-id="10559-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="10559-107">_ulConnection_</span></span>
  
> <span data-ttu-id="10559-108">[in] Die Zahl ungleich NULL Verbindung der zuvor über **IMAPISupport::Subscribe**hergestellt benachrichtigungsregistrierung zurück.</span><span class="sxs-lookup"><span data-stu-id="10559-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10559-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="10559-109">Return value</span></span>

<span data-ttu-id="10559-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="10559-110">S_OK</span></span> 
  
> <span data-ttu-id="10559-111">Die benachrichtigungsregistrierung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="10559-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="10559-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="10559-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="10559-113">Die Nummer im _UlConnection_ -Parameter übergeben, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="10559-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="10559-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10559-114">Remarks</span></span>

<span data-ttu-id="10559-115">Die **IMAPISupport::Unsubscribe** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="10559-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="10559-116">Dienstanbieter rufen Sie **kündigen** , um eine zuvor vom **Subscribe**eingerichteten benachrichtigungsregistrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="10559-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="10559-117">**Zum Abmelden** hebt die Registrierung durch den Anruf **Subscribe** übergebene Advise Empfängerzeiger freigeben.</span><span class="sxs-lookup"><span data-stu-id="10559-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="10559-118">Im Allgemeinen der Advise-Empfänger **IUnknown** -Methode aufgerufen wird während des Anrufs **zum Abmelden** .</span><span class="sxs-lookup"><span data-stu-id="10559-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="10559-119">Ist ein anderer Thread die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für das Empfängerobjekt Advise aufruft, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="10559-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10559-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10559-120">See also</span></span>



[<span data-ttu-id="10559-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="10559-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="10559-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="10559-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="10559-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="10559-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

