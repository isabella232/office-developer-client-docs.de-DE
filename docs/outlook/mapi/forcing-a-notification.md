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
# <a name="forcing-a-notification"></a>Erzwingen einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Dienstanbieter die [IMAPISupport: IUnknown](imapisupportiunknown.md) -Methoden für die Benachrichtigung verwenden, übermittelt MAPI Benachrichtigungen mithilfe eines ausgeblendeten Fensters und der entsprechenden Fensterprozedur. Für jeden Prozess, der eine Benachrichtigung empfängt, sendet MAPI eine spezielle Nachricht an das ausgeblendete Fenster. Diese Nachricht wird mit der Konstanten **szMAPINotificationMsg** benannt, die in MAPIDEFS definiert ist. H. 
  
Sie erhalten diese Benachrichtigungen, wenn die Fensterprozedur des ausgeblendeten Fensters die **szMAPINotificationMsg** -Nachricht verarbeitet. Um sicherzustellen, dass Benachrichtigungen zugestellt werden, ist es erforderlich, diese **szMAPINotificationMsg** -Nachricht zu warten und zu senden. Die Implementierung der Logik, um dies zu erreichen, kann relativ einfach erfolgen, aber MAPI bietet einen Einstiegspunkt in die MAPI-DLL namens [HrDispatchNotifications](hrdispatchnotifications.md) , um die Verarbeitung noch einfacher zu gestalten. Rufen Sie **HrDispatchNotifications** wie folgt auf, um Benachrichtigungen in Ihrem Client zu erhalten: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


