---
title: Erzwingen einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 878a4372b4fe017fce001ddb3322f1d044151134
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621080"
---
# <a name="forcing-a-notification"></a>Erzwingen einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Dienstanbieter die [IMAPISupport : IUnknown-Methoden](imapisupportiunknown.md) für Benachrichtigungen verwenden, übermittelt MAPI Benachrichtigungen mithilfe eines ausgeblendeten Fensters und der zugehörigen Fensterprozedur. Damit jeder Prozess eine Benachrichtigung erhält, sendet MAPI eine spezielle Nachricht an das ausgeblendete Fenster. Diese Nachricht wird mit der Konstanten **szMAPINotificationMsg** benannt, die in MAPIDEFS.H definiert ist. 
  
Sie erhalten diese Benachrichtigungen, wenn die Fensterprozedur des ausgeblendeten Fensters die **szMAPINotificationMsg-Nachricht** verarbeitet. Um zu gewährleisten, dass Benachrichtigungen zugestellt werden, müssen Sie warten und diese **szMAPINotificationMsg-Nachricht** senden. Die Implementierung der logik zu diesem Zweck kann relativ einfach erfolgen, aber MAPI bietet einen Einstiegspunkt in die MAPI-DLL mit dem Namen [HrDispatchNotifications,](hrdispatchnotifications.md) um die Verarbeitung noch einfacher zu machen. Rufen Sie **HrDispatchNotifications** wie folgt auf, um Benachrichtigungen in Ihrem Client zu erhalten: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


