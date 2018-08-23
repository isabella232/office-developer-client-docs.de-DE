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
ms.openlocfilehash: 3fbf8b423cfd4206a0143b5639c85dbcacce2fae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570982"
---
# <a name="iablogonunadvise"></a><span data-ttu-id="7aad6-103">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7aad6-103">IABLogon::Unadvise</span></span>

  
  
<span data-ttu-id="7aad6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aad6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aad6-105">Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IABLogon::Advise](iablogon-advise.md) eingerichtet wurden, werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7aad6-105">Cancels notifications that were previously set up with a call to the [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7aad6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7aad6-106">Parameters</span></span>

 <span data-ttu-id="7aad6-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="7aad6-107">_ulConnection_</span></span>
  
> <span data-ttu-id="7aad6-108">[in] Die Nummer eines aktiven benachrichtigungsregistrierung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7aad6-108">[in] The connection number associated with an active notification registration.</span></span> <span data-ttu-id="7aad6-109">Ein vorherigen Aufruf von **Advise** muss den Wert der _UlConnection_zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7aad6-109">A previous call to **Advise** must have returned the value of  _ulConnection_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7aad6-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7aad6-110">Return value</span></span>

<span data-ttu-id="7aad6-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7aad6-111">S_OK</span></span> 
  
> <span data-ttu-id="7aad6-112">Die benachrichtigungsregistrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7aad6-112">The notification registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7aad6-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7aad6-113">Remarks</span></span>

<span data-ttu-id="7aad6-114">MAPI-Aufrufen die **Unadvise** -Methode, um die benachrichtigungsregistrierung eines für einen Container abzubrechen messaging-Benutzer oder Verteilung List-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7aad6-114">MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7aad6-115">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7aad6-115">Notes to implementers</span></span>

<span data-ttu-id="7aad6-116">Die Implementierung von **Unadvise** hängt davon ab, ob Sie die Benachrichtigung mithilfe des MAPI-Hilfe oder manuell zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7aad6-116">Your implementation of **Unadvise** will depend on whether you support notification with MAPI's help or manually.</span></span> <span data-ttu-id="7aad6-117">Wenn MAPI Ihrer unterstützt, rufen Sie die [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) -Methode, um die Registrierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="7aad6-117">If MAPI provides your support, call the [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) method to cancel the registration.</span></span> <span data-ttu-id="7aad6-118">Ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, kann verzögert werden, bis **OnNotify** zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7aad6-118">If another thread is in the process of calling the advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method, it can be delayed until **OnNotify** has returned.</span></span> 
  
<span data-ttu-id="7aad6-119">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7aad6-119">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="7aad6-120">Informationen zur Verwendung der [IMAPISupport: IUnknown](imapisupportiunknown.md) Methoden verwenden, um die Benachrichtigung, zu unterstützen, finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="7aad6-120">For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7aad6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aad6-121">See also</span></span>



[<span data-ttu-id="7aad6-122">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="7aad6-122">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="7aad6-123">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7aad6-123">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7aad6-124">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7aad6-124">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

