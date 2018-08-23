---
title: MAPI-Formularen Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 38011c02791688ce5b1c291a1355ccaececd43fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574734"
---
# <a name="mapi-forms-notifications"></a>MAPI-Formularen Benachrichtigungen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Registrieren für und zur Handhabung von Nachrichten aus dem Formularobjekte ist einem anderen Prozess als für andere MAPI-Objekte. Advise-Empfänger für Formular Benachrichtigungen implementieren entweder die **IMAPIViewAdviseSink** oder **IMAPIFormAdviseSink** Schnittstelle statt **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) und [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) jeweils verwendet mehrere Methoden, eine für jede der möglichen Ereignisse, dass das entsprechende-Quelle Advise ist generieren kann. Beispielsweise **IMAPIFormAdviseSink** verfügt über zwei Methoden: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) zum Verarbeiten von einer Änderung an des Formular-Viewers Status und [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) , um eine neue Nachricht im korrekten Format anzuzeigen. 
  
Ereignisbehandlung Strategie für Formulare ähnelt der Ereignisbehandlung in OLE implementierte Strategie. Wie für die meisten Objekte von MAPI-registrieren Clients nicht für bestimmte Ereignistypen. Davon ausgegangen wird, dass für die Benachrichtigung registrieren, können sie jede Art von Ereignis empfangen, die von bestimmten Advise-Quelle generiert werden können. Da **IMAPIAdviseSink::OnNotify** geschrieben werden muss, um alle registrierten Ereignisse behandeln, möglich implementieren sie komplexe für Clients, die für viele verschiedene Ereignisse registrieren. Da die Methoden in der Form-Empfänger Objekte Ziel Advise ist ein einzelnes Ereignis, Implementierung dieser Methoden einfacher. 
  

