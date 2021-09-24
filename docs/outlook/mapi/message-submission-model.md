---
title: Nachrichtenübermittlungsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4862fca03df1f152c757becc7f6c9e56b3e92363
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551058"
---
# <a name="message-submission-model"></a>Nachrichtenübermittlungsmodell

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Nachrichtenübermittlung erfolgt durch eine Reihe von Aufrufen des MAPI-Spoolers an den Transportanbieter. Die Aufrufe werden wie folgt sequenziert:
  
1. Der MAPI-Spooler ruft [IXPLogon::SubmitMessage auf](ixplogon-submitmessage.md)und übergibt eine [IMessage : IMAPIProp-Instanz,](imessageimapiprop.md) um den Prozess zu starten. 
    
2. Der Transportanbieter platziert dann einen Verweiswert – einen transportdefinierten Bezeichner, der in zukünftigen Verweisen auf diese Nachricht verwendet wird – an dem Speicherort, auf den in **SubmitMessage** verwiesen wird.
    
3. Der Transportanbieter greift mithilfe der übergebenen **IMessage-Instanz** auf die Nachrichtendaten zu. Für jeden Empfänger in der übergebenen **IMessage,** für die er verantwortlich ist, legt der Transportanbieter die **Eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) fest und gibt dann zurück.
    
4. Der Transportanbieter kann die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) verwenden, um anzugeben, ob Empfänger erkannt werden, an die nicht übermittelt werden kann, oder um einen Standardzustellungsbericht zu erstellen. **StatusRecips** ist ein Komfort für Transportanbieter, die festgestellt haben, dass einige der Empfänger nicht zugestellt werden können oder die Übermittlungsinformationen von ihrem zugrunde liegenden Messagingsystem erhalten haben, die der Benutzer oder die Clientanwendung möglicherweise hilfreich finden. 
    
5. Der Aufruf des MAPI-Spoolers an [IXPLogon::EndMessage](ixplogon-endmessage.md) ist die letzte Aufgabe für die Nachricht vom MAPI-Spooler an den Transportanbieter. 
    
6. Der MAPI-Spooler kann [IXPLogon::TransportNotify](ixplogon-transportnotify.md) verwenden, um die Nachrichtenverarbeitung während der **SubmitMessage-** oder **EndMessage-Aufrufe** abzubrechen. 
    

