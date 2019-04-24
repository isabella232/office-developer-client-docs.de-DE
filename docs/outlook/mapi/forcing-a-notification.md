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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328098"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="3dd55-103">Erzwingen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="3dd55-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="3dd55-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dd55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dd55-105">Wenn Dienstanbieter die [IMAPISupport: IUnknown](imapisupportiunknown.md) -Methoden für die Benachrichtigung verwenden, übermittelt MAPI Benachrichtigungen mithilfe eines ausgeblendeten Fensters und der entsprechenden Fensterprozedur.</span><span class="sxs-lookup"><span data-stu-id="3dd55-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="3dd55-106">Für jeden Prozess, der eine Benachrichtigung empfängt, sendet MAPI eine spezielle Nachricht an das ausgeblendete Fenster.</span><span class="sxs-lookup"><span data-stu-id="3dd55-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="3dd55-107">Diese Nachricht wird mit der Konstanten **szMAPINotificationMsg** benannt, die in MAPIDEFS definiert ist. H.</span><span class="sxs-lookup"><span data-stu-id="3dd55-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="3dd55-108">Sie erhalten diese Benachrichtigungen, wenn die Fensterprozedur des ausgeblendeten Fensters die **szMAPINotificationMsg** -Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3dd55-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="3dd55-109">Um sicherzustellen, dass Benachrichtigungen zugestellt werden, ist es erforderlich, diese **szMAPINotificationMsg** -Nachricht zu warten und zu senden.</span><span class="sxs-lookup"><span data-stu-id="3dd55-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="3dd55-110">Die Implementierung der Logik, um dies zu erreichen, kann relativ einfach erfolgen, aber MAPI bietet einen Einstiegspunkt in die MAPI-DLL namens [HrDispatchNotifications](hrdispatchnotifications.md) , um die Verarbeitung noch einfacher zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="3dd55-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="3dd55-111">Rufen Sie **HrDispatchNotifications** wie folgt auf, um Benachrichtigungen in Ihrem Client zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="3dd55-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


