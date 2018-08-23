---
title: Nachrichtenübermittlungsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8cb34360f5a0a3e67aca1ac53fe639724135f594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584541"
---
# <a name="message-submission-model"></a>Nachrichtenübermittlungsmodell

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Nachrichtenübermittlung wird durch eine Reihe von Aufrufen aus die MAPI-Warteschlange der Adressbuchhierarchie erreicht. Die Anrufe sind wie folgt berechnet:
  
1. Die MAPI-Warteschlange ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), und übergeben eine [IMessage: IMAPIProp](imessageimapiprop.md) -Instanz, um den zu starten. 
    
2. Der Transportdienst anschließend wird der Verweiswert – ein Transport-definierten Bezeichner verwendet in Zukunft Verweise auf diese Meldung – am Speicherort in **SubmitMessage**verwiesen wird.
    
3. Der Transportdienst greift auf die Nachrichtendaten mithilfe der übergebenen **IMessage** -Instanz. Für jeden Empfänger in übergebenen **IMessage** für die Verantwortung zulässt, der Adressbuchhierarchie wird die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft, und gibt dann zurück.
    
4. Der Transportdienst kann die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode verwenden, um anzugeben, ob er erkennt alle Empfänger, die nicht zugestellt werden können, oder erstellen Sie einen standard-Delivery Report. **StatusRecips** ist eine Vereinfachung für Transportanbieter, die bestimmt haben, dass einige Empfänger an übermittelt werden kann oder, von deren zugrunde liegenden messaging-System, die die Benutzer oder eine Client-Anwendung kann die Übermittlungsinformationen empfangen hilfreich sein. 
    
5. Die MAPI-Warteschlange Aufruf von [IXPLogon::EndMessage](ixplogon-endmessage.md) ist die endgültige Verantwortung Übergabe für eine Nachricht aus der Warteschlange MAPI an der Adressbuchhierarchie. 
    
6. Die MAPI-Warteschlange kann [IXPLogon::TransportNotify](ixplogon-transportnotify.md) verwenden, um Nachrichten, die während der **SubmitMessage** oder **EndMessage** Anrufe abzubrechen. 
    

