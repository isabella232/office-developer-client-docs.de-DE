---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424077"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="61e22-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="61e22-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="61e22-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61e22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61e22-105">Benachrichtigungen, die zuvor mit einem Aufruf der [IABLogon::Advise-Methode eingerichtet wurden,](iablogon-advise.md) werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="61e22-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="61e22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="61e22-106">Parameters</span></span>

 <span data-ttu-id="61e22-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="61e22-107">_ulConnection_</span></span>
  
> <span data-ttu-id="61e22-108">[in] Die Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="61e22-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="61e22-109">Ein vorheriger Aufruf von **Advise** muss den Wert von _ulConnection zurückgegeben haben._</span><span class="sxs-lookup"><span data-stu-id="61e22-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61e22-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61e22-110">Return value</span></span>

<span data-ttu-id="61e22-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="61e22-111">S_OK</span></span> 
  
> <span data-ttu-id="61e22-112">Die Benachrichtigungsregistrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="61e22-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61e22-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61e22-113">Remarks</span></span>

<span data-ttu-id="61e22-114">MAPI ruft die **Unadvise-Methode** auf, um eine Benachrichtigungsregistrierung für ein Container-, Messagingbenutzer- oder Verteilerlistenobjekt abbricht.</span><span class="sxs-lookup"><span data-stu-id="61e22-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="61e22-115">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="61e22-115">Notes to implementers</span></span>

<span data-ttu-id="61e22-116">Ihre Implementierung von **Unadvise** hängt davon ab, ob Sie Benachrichtigungen mithilfe von MAPI oder manuell unterstützen.</span><span class="sxs-lookup"><span data-stu-id="61e22-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="61e22-117">Wenn MAPI Ihren Support bietet, rufen Sie die [IMAPISupport::Unsubscribe-Methode](imapisupport-unsubscribe.md) auf, um die Registrierung abbricht.</span><span class="sxs-lookup"><span data-stu-id="61e22-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="61e22-118">Wenn ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Ratensenke aufruft, kann er verzögert werden, bis **OnNotify** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="61e22-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="61e22-119">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="61e22-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="61e22-120">Informationen zur Verwendung der [IMAPISupport : IUnknown-Methoden](imapisupportiunknown.md) zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="61e22-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61e22-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61e22-121">See also</span></span>



[<span data-ttu-id="61e22-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="61e22-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="61e22-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="61e22-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="61e22-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61e22-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

