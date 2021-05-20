---
title: Senden von Nachrichten mithilfe von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438722"
---
# <a name="sending-messages-by-using-mapi"></a>Senden von Nachrichten mithilfe von MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen rufen die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um eine Nachricht zu senden. **SubmitMessage ruft** [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern, bevor die Steuerung an den MAPI-Spooler oder direkt an einen Transportanbieter übertragen wird. 
  
Der MAPI-Spooler empfängt die Nachricht, wenn eine der folgenden Fehler auftritt:
  
- Der Nachrichtenspeicheranbieter und der Transportanbieter sind nicht eng gekoppelt.
    
- Die Nachricht erfordert eine Vorverarbeitung.
    
- Der eng gekoppelte Nachrichtenspeicher und -transport kann nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.
    
Ein eng gekoppelter Nachrichtenspeicher muss den Status einer Nachricht berücksichtigen, bevor er sie dem MAPI-Spooler zum Herunterladen an einen Transportanbieter präsentiert. Es gibt Situationen, in denen eine Nachricht möglicherweise den MAPI-Spooler erfordert, aber der MAPI-Spooler sollte wirklich nicht beteiligt sein.
  
Betrachten Sie beispielsweise die Situation, in der ein Benutzer eine Nachricht aus dem Posteingang sendet. Der Client verwendet einen eng gekoppelten Speicher und Transport. Wenn der eng gekoppelte Nachrichtenspeicher den Speicherort der Nachricht als einziges Kriterium für die Entscheidung verwendet, ob der MAPI-Spooler die Nachricht verarbeiten soll, erhält der MAPI-Spooler immer die Nachricht. Um diese Art von Problem zu vermeiden, muss ein eng gekoppelter Nachrichtenspeicher zusätzlich zum Nachrichtenspeicherort den Nachrichtenstatus überprüfen. Insbesondere sollte der Transportanbieter nicht anfordern, dass der MAPI-Spooler aktiv übermittelte Nachrichten herunterloaden muss.
  
Der Nachrichtenübermittlungsprozess umfasst den Nachrichtenspeicheranbieter, einen oder mehrere Transportanbieter und MAPI. Die Themen in diesem Abschnitt enthalten detaillierte Informationen zu bestimmten Rollen im Nachrichtenübermittlungsprozess.
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

