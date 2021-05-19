---
title: MAPI Forms Notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9c10f78af6dff2e0d0c59d0bfe59be07dccd4b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418610"
---
# <a name="mapi-forms-notifications"></a>MAPI Forms Notifications

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Registrieren und Behandeln von Benachrichtigungen von Formularobjekten ist ein anderer Prozess als bei anderen MAPI-Objekten. Ratenken für Formularbenachrichtigungen implementieren entweder die **IMAPIViewAdviseSink-** oder **DIEAPIFormAdviseSink-Schnittstelle** anstelle von **IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) und [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) verfügen jeweils über mehrere Methoden, eine für jedes der möglichen Ereignisse, die die entsprechende Informationsquelle generieren kann. **ImAPIFormAdviseSink** verfügt beispielsweise über zwei Methoden: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) zum Behandeln einer Änderung am Status der Formularanzeige und [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) zum Anzeigen einer neuen Nachricht mit dem richtigen Formular. 
  
Die Ereignisbehandlungsstrategie für Formulare ähnelt der in OLE implementierten Ereignisbehandlungsstrategie. Clients registrieren sich nicht für bestimmte Ereignistypen wie für die meisten MAPI-Objekte. Die Annahme ist, dass die Registrierung für Benachrichtigungen es ihnen ermöglicht, alle Arten von Ereignis zu empfangen, die von der jeweiligen Ratenquelle generiert werden können. Da **IMAPIAdviseSink::OnNotify** so geschrieben werden muss, dass alle registrierten Ereignisse umgangen werden, kann die Implementierung für Clients, die sich für viele verschiedene Ereignisse registrieren, komplex sein. Da die Methoden im Formular Senkenobjekte für ein einzelnes Ereignis empfehlen, ist die Implementierung dieser Methoden einfacher. 
  

