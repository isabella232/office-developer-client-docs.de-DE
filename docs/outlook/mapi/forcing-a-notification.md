---
title: Erzwingen einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433283"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="2fb39-103">Erzwingen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2fb39-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="2fb39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fb39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fb39-105">Wenn Dienstanbieter die [IMAPISupport : IUnknown-Methoden](imapisupportiunknown.md) für die Benachrichtigung verwenden, stellt MAPI Benachrichtigungen mithilfe eines ausgeblendeten Fensters und der entsprechenden Fensterprozedur zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2fb39-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="2fb39-106">Damit jeder Prozess eine Benachrichtigung erhält, postet MAPI eine spezielle Nachricht an das ausgeblendete Fenster.</span><span class="sxs-lookup"><span data-stu-id="2fb39-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="2fb39-107">Diese Nachricht wird mit der konstante **szMAPINotificationMsg** benannt, die in MAPIDEFS.H definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2fb39-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="2fb39-108">Sie erhalten diese Benachrichtigungen, wenn die Fensterprozedur des ausgeblendeten Fensters die **szMAPINotificationMsg-Nachricht** verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2fb39-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="2fb39-109">Um zu gewährleisten, dass Benachrichtigungen zugestellt werden, müssen Sie auf diese **szMAPINotificationMsg-Nachricht** warten und diese senden.</span><span class="sxs-lookup"><span data-stu-id="2fb39-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="2fb39-110">Die Implementierung der Logik dazu kann relativ einfach durchgeführt werden, aber MAPI bietet einen Einstiegspunkt in die MAPI-DLL mit dem Namen [HrDispatchNotifications,](hrdispatchnotifications.md) um die Verarbeitung noch einfacher zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="2fb39-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="2fb39-111">Rufen **Sie HrDispatchNotifications** wie folgt auf, um Benachrichtigungen in Ihrem Client zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2fb39-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


