---
title: MAPI-Formular Benachrichtigungen
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
# <a name="mapi-forms-notifications"></a>MAPI-Formular Benachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Registrierung für und die Behandlung von Benachrichtigungen von Formularobjekten ist ein anderer Prozess als bei anderen MAPI-Objekten. Advise-Senken für Formular Benachrichtigungen implementieren Sie die **IMAPIViewAdviseSink** -oder **IMAPIFormAdviseSink** -Schnittstelle anstelle von **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) und [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) haben jeweils mehrere Methoden, eine für jedes der möglichen Ereignisse, die die entsprechende Advise-Quelle generieren kann. **IMAPIFormAdviseSink** verfügt beispielsweise über zwei Methoden: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) , um eine Änderung am Status des Formular Viewers und [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md) zu behandeln, um eine neue Nachricht mit dem richtigen Formular anzuzeigen. 
  
Die Ereignisbehandlungsstrategie für Formulare ähnelt der in OLE implementierten Ereignisbehandlungsstrategie. Clients registrieren nicht für bestimmte Ereignistypen, wie für die meisten MAPI-Objekte. Es wird davon ausgegangen, dass Sie bei der Registrierung für die Benachrichtigung jede Art von Ereignis empfangen können, das von der jeweiligen Advise-Quelle generiert werden kann. Da **IMAPIAdviseSink:: OnNotify** so geschrieben werden muss, dass alle registrierten Ereignisse verarbeitet werden können, kann es für Clients, die sich für viele verschiedene Ereignisse registrieren, eine komplexe Implementierung geben. Da die Methoden im Formularempfänger Objekte für ein einzelnes Ereignis beraten, ist die Implementierung dieser Methoden einfacher. 
  

