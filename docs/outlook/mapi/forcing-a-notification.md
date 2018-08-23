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
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578773"
---
# <a name="forcing-a-notification"></a>Erzwingen einer Benachrichtigung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Dienst Dienstanbieter verwenden die [IMAPISupport: IUnknown](imapisupportiunknown.md) Methoden für die Benachrichtigung, MAPI bietet Benachrichtigungen mit einem ausgeblendeten Fenster und ihrer entsprechenden Fensterprozedur. Für jeden Prozess eine Benachrichtigung erhalten sendet die MAPI eine spezielle Nachricht an das ausgeblendete Fenster. Diese Meldung wird mit der Konstante **SzMAPINotificationMsg** mit dem Namen der in MAPIDEFS definiert ist. H. 
  
Sie erhalten diese Benachrichtigungen, wenn das ausgeblendete Fenster Fenster Verfahren **SzMAPINotificationMsg** Nachricht verarbeitet. Um sicherzustellen, dass Benachrichtigungen gesendet werden, ist es erforderlich, warten und diese Meldung **SzMAPINotificationMsg** versenden. Implementieren die Logik zu diesem Zweck kann erfolgen relativ einfach, aber MAPI bietet ein Einstiegspunkt in die MAPI-DLL [HrDispatchNotifications](hrdispatchnotifications.md) damit Verarbeitung sogar noch einfacher wird aufgerufen. Rufen Sie **HrDispatchNotifications** wie folgt Erhalt von Benachrichtigungen in Ihrem Client: 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


