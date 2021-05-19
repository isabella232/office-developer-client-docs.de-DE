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
# <a name="forcing-a-notification"></a>Erzwingen einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Dienstanbieter die [IMAPISupport : IUnknown-Methoden](imapisupportiunknown.md) für die Benachrichtigung verwenden, stellt MAPI Benachrichtigungen mithilfe eines ausgeblendeten Fensters und der entsprechenden Fensterprozedur zur Verfügung. Damit jeder Prozess eine Benachrichtigung erhält, postet MAPI eine spezielle Nachricht an das ausgeblendete Fenster. Diese Nachricht wird mit der konstante **szMAPINotificationMsg** benannt, die in MAPIDEFS.H definiert ist. 
  
Sie erhalten diese Benachrichtigungen, wenn die Fensterprozedur des ausgeblendeten Fensters die **szMAPINotificationMsg-Nachricht** verarbeitet. Um zu gewährleisten, dass Benachrichtigungen zugestellt werden, müssen Sie auf diese **szMAPINotificationMsg-Nachricht** warten und diese senden. Die Implementierung der Logik dazu kann relativ einfach durchgeführt werden, aber MAPI bietet einen Einstiegspunkt in die MAPI-DLL mit dem Namen [HrDispatchNotifications,](hrdispatchnotifications.md) um die Verarbeitung noch einfacher zu gestalten. Rufen **Sie HrDispatchNotifications** wie folgt auf, um Benachrichtigungen in Ihrem Client zu erhalten: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


