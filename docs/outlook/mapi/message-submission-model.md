---
title: Nachrichten Übermittlungs Modell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356875"
---
# <a name="message-submission-model"></a>Nachrichten Übermittlungs Modell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtenübermittlung erfolgt über eine Reihe von Anrufen vom MAPI-Spooler an den Transportanbieter. Die Anrufe werden wie folgt sequenziert:
  
1. Der MAPI-Spooler ruft [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md)auf und übergibt eine [IMessage: IMAPIProp](imessageimapiprop.md) -Instanz, um den Prozess zu beginnen. 
    
2. Der Transportanbieter platziert dann einen Verweiswert – einen Transport definierten Bezeichner, der in zukünftigen verweisen auf diese Nachricht verwendet wird – an dem Speicherort, auf den in **SubmitMessage**verwiesen wird.
    
3. Der Transportanbieter greift mithilfe der übergebenen **IMessage** -Instanz auf die Nachrichtendaten zu. Für jeden Empfänger im übergebenen **IMessage** , für den er die Verantwortung übernimmt, legt der Transportanbieter die **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft fest und gibt dann zurück.
    
4. Der Transportanbieter kann die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode verwenden, um anzugeben, ob Empfänger erkannt werden, an die nicht übermittelt werden kann, oder einen Standard Zustellungsbericht zu erstellen. **StatusRecips** ist eine Bequemlichkeit für Transportanbieter, die festgestellt haben, dass einige der Empfänger nicht zugestellt werden können oder die Zustellungsinformationen aus dem zugrunde liegenden Messagingsystem erhalten haben, das der Benutzer oder die Clientanwendung möglicherweise hilfreich. 
    
5. Der Aufruf des MAPI-Spoolers an [IXPLogon:: EndMessage](ixplogon-endmessage.md) ist die abschließende Verantwortlichkeit für die Nachricht vom MAPI-Spooler an den Transportanbieter. 
    
6. Der MAPI-Spooler kann [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) verwenden, um die Nachrichtenverarbeitung während der **SubmitMessage** -oder **EndMessage** -Aufrufe abzubrechen. 
    

