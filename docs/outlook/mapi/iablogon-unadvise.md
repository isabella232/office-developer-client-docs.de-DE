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
# <a name="iablogonunadvise"></a><span data-ttu-id="79daa-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="79daa-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="79daa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79daa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79daa-105">Bricht Benachrichtigungen ab, die zuvor mit einem Aufruf der [IABLogon:: Advise](iablogon-advise.md) -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="79daa-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="79daa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79daa-106">Parameters</span></span>

 <span data-ttu-id="79daa-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="79daa-107">_ulConnection_</span></span>
  
> <span data-ttu-id="79daa-108">in Die Verbindungsnummer, die mit einer aktiven Benachrichtigungs Registrierung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="79daa-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="79daa-109">Ein vorheriger Anruf an **Advise** muss den Wert von _ulConnection_zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="79daa-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79daa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79daa-110">Return value</span></span>

<span data-ttu-id="79daa-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="79daa-111">S_OK</span></span> 
  
> <span data-ttu-id="79daa-112">Die Benachrichtigungs Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="79daa-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79daa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79daa-113">Remarks</span></span>

<span data-ttu-id="79daa-114">MAPI Ruft die **Unadvise** -Methode auf, um eine Benachrichtigungs Registrierung für ein Container-, Messaging-oder Verteilerlistenobjekt abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="79daa-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="79daa-115">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="79daa-115">Notes to implementers</span></span>

<span data-ttu-id="79daa-116">Die Implementierung von **Unadvise** hängt davon ab, ob Sie die Benachrichtigung mit der MAPI-Hilfe oder manuell unterstützen.</span><span class="sxs-lookup"><span data-stu-id="79daa-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="79daa-117">Wenn MAPI ihre Unterstützung bereitstellt, rufen Sie die [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) -Methode auf, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="79daa-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="79daa-118">Wenn in einem anderen Thread die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der Advise-Senke aufgerufen wird, kann Sie verzögert werden \*\*\*\* , bis OnNotify zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="79daa-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="79daa-119">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="79daa-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="79daa-120">Informationen zur Verwendung der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="79daa-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79daa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79daa-121">See also</span></span>



[<span data-ttu-id="79daa-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="79daa-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="79daa-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="79daa-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="79daa-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79daa-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

