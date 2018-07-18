---
title: Erzwingen einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 40fc763071f7113e222c6987dfd70fb7d89bab4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791714"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="579f3-103">Erzwingen einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="579f3-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="579f3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="579f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="579f3-105">Wenn Dienst Dienstanbieter verwenden die [IMAPISupport: IUnknown](imapisupportiunknown.md) Methoden für die Benachrichtigung, MAPI bietet Benachrichtigungen mit einem ausgeblendeten Fenster und ihrer entsprechenden Fensterprozedur.</span><span class="sxs-lookup"><span data-stu-id="579f3-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="579f3-106">Für jeden Prozess eine Benachrichtigung erhalten sendet die MAPI eine spezielle Nachricht an das ausgeblendete Fenster.</span><span class="sxs-lookup"><span data-stu-id="579f3-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="579f3-107">Diese Meldung wird mit der Konstante **SzMAPINotificationMsg** mit dem Namen der in MAPIDEFS definiert ist. H.</span><span class="sxs-lookup"><span data-stu-id="579f3-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="579f3-108">Sie erhalten diese Benachrichtigungen, wenn das ausgeblendete Fenster Fenster Verfahren **SzMAPINotificationMsg** Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="579f3-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="579f3-109">Um sicherzustellen, dass Benachrichtigungen gesendet werden, ist es erforderlich, warten und diese Meldung **SzMAPINotificationMsg** versenden.</span><span class="sxs-lookup"><span data-stu-id="579f3-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="579f3-110">Implementieren die Logik zu diesem Zweck kann erfolgen relativ einfach, aber MAPI bietet ein Einstiegspunkt in die MAPI-DLL [HrDispatchNotifications](hrdispatchnotifications.md) damit Verarbeitung sogar noch einfacher wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="579f3-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="579f3-111">Rufen Sie **HrDispatchNotifications** wie folgt Erhalt von Benachrichtigungen in Ihrem Client:</span><span class="sxs-lookup"><span data-stu-id="579f3-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


