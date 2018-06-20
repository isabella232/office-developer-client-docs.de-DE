---
title: MAPI-Formularen Benachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7064aee2ccd35b6b372bc6f911c7508113c26162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793003"
---
# <a name="mapi-forms-notifications"></a>MAPI-Formularen Benachrichtigungen

  
  
**Betrifft**: Outlook 
  
Registrieren für und zur Handhabung von Nachrichten aus dem Formularobjekte ist einem anderen Prozess als für andere MAPI-Objekte. Advise-Empfänger für Formular Benachrichtigungen implementieren entweder die **IMAPIViewAdviseSink** oder **IMAPIFormAdviseSink** Schnittstelle statt **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) und [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) jeweils verwendet mehrere Methoden, eine für jede der möglichen Ereignisse, dass das entsprechende-Quelle Advise ist generieren kann. Beispielsweise **IMAPIFormAdviseSink** verfügt über zwei Methoden: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) zum Verarbeiten von einer Änderung an des Formular-Viewers Status und [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) , um eine neue Nachricht im korrekten Format anzuzeigen. 
  
Ereignisbehandlung Strategie für Formulare ähnelt der Ereignisbehandlung in OLE implementierte Strategie. Wie für die meisten Objekte von MAPI-registrieren Clients nicht für bestimmte Ereignistypen. Davon ausgegangen wird, dass für die Benachrichtigung registrieren, können sie jede Art von Ereignis empfangen, die von bestimmten Advise-Quelle generiert werden können. Da **IMAPIAdviseSink::OnNotify** geschrieben werden muss, um alle registrierten Ereignisse behandeln, möglich implementieren sie komplexe für Clients, die für viele verschiedene Ereignisse registrieren. Da die Methoden in der Form-Empfänger Objekte Ziel Advise ist ein einzelnes Ereignis, Implementierung dieser Methoden einfacher. 
  

