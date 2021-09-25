---
title: MAPI-Formularbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b0d5ffeb6aee30966f12e13a82ef7e345a86ab3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556175"
---
# <a name="mapi-forms-notifications"></a>MAPI-Formularbenachrichtigungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Registrieren und Verarbeiten von Benachrichtigungen von Formularobjekten unterscheidet sich von anderen MAPI-Objekten. Empfehlen Sie Senken für Formularbenachrichtigungen, entweder die **IMAPIViewAdviseSink-** oder **IMAPIFormAdviseSink-Schnittstelle** anstelle von **IMAPIAdviseSink** zu implementieren. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) und [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) verfügen jeweils über mehrere Methoden, eine für jedes der möglichen Ereignisse, die die entsprechende Empfehlungsquelle generieren kann. Beispielsweise verfügt **IMAPIFormAdviseSink** über zwei Methoden: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) zum Behandeln einer Änderung des Status der Formularanzeige und [IMAPIFormAdviseSink::OnActivateNext,](imapiformadvisesink-onactivatenext.md) um eine neue Nachricht mit dem richtigen Formular anzuzeigen. 
  
Die Ereignisbehandlungsstrategie für Formulare ähnelt der in OLE implementierten Ereignisbehandlungsstrategie. Clients registrieren sich nicht für bestimmte Ereignistypen wie für die meisten MAPI-Objekte. Es wird davon ausgegangen, dass die Registrierung für Benachrichtigungen es ihnen ermöglicht, alle Arten von Ereignissen zu empfangen, die von der jeweiligen Empfehlungsquelle generiert werden können. Da **IMAPIAdviseSink::OnNotify** so geschrieben werden muss, dass alle registrierten Ereignisse behandelt werden können, kann die Implementierung für Clients, die sich für viele verschiedene Ereignisse registrieren, komplex sein. Da die Methoden im Formular Senkenobjekte als Ziel eines einzelnen Ereignisses empfehlen, ist die Implementierung dieser Methoden einfacher. 
  

