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
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421123"
---
# <a name="message-submission-model"></a>Nachrichtenübermittlungsmodell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtenübermittlung erfolgt durch eine Reihe von Anrufen vom MAPI-Spooler an den Transportanbieter. Die Aufrufe werden wie folgt sequenziert:
  
1. Der MAPI-Spooler ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)auf und übertrumpft eine [IMessage : IMAPIProp-Instanz,](imessageimapiprop.md) um den Prozess zu beginnen. 
    
2. Der Transportanbieter platziert dann einen Referenzwert – einen transportdefinierten Bezeichner, der in zukünftigen Verweisen auf diese Nachricht verwendet wird – an dem Speicherort, auf den in **SubmitMessage verwiesen wird.**
    
3. Der Transportanbieter zugrifft mithilfe der übergebenen **IMessage-Instanz** auf die Nachrichtendaten. Für jeden Empfänger in der übergebenen **IMessage,** für die er die Verantwortung übernimmt, legt der Transportanbieter die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) fest und gibt dann zurück.
    
4. Der Transportanbieter kann die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) verwenden, um anzugeben, ob Empfänger erkannt werden, die nicht zugestellt werden können, oder um einen Standardzustellungsbericht zu erstellen. **StatusRecips** ist ein Komfort für Transportanbieter, die festgestellt haben, dass einige empfänger nicht zugestellt werden können oder Übermittlungsinformationen von ihrem zugrunde liegenden Messagingsystem erhalten haben, die der Benutzer oder die Clientanwendung möglicherweise nützlich finden. 
    
5. Der Aufruf des MAPI-Spoolers bei [IXPLogon::EndMessage](ixplogon-endmessage.md) ist die endgültige Übergabe der Verantwortung für die Nachricht vom MAPI-Spooler an den Transportanbieter. 
    
6. Der MAPI-Spooler kann [IXPLogon::TransportNotify](ixplogon-transportnotify.md) verwenden, um die Nachrichtenverarbeitung während der **SubmitMessage-** oder **EndMessage-Aufrufe abbricht.** 
    

