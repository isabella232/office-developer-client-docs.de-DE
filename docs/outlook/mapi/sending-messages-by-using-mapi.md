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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339753"
---
# <a name="sending-messages-by-using-mapi"></a>Senden von Nachrichten mithilfe von MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Client Anwendungen rufen die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf, um eine Nachricht zu senden. **SubmitMessage** ruft [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern, bevor die Steuerung an den MAPI-Spooler oder direkt an einen Transportanbieter übertragen wird. 
  
Der MAPI-Spooler empfängt die Nachricht, wenn eine der folgenden Aktionen Eintritt:
  
- Der Nachrichtenspeicher Anbieter und der Transportanbieter sind nicht eng gekoppelt.
    
- Die Nachricht erfordert die Vorverarbeitung.
    
- Der eng gekoppelte Nachrichtenspeicher und der Transport können nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.
    
Bei einem eng gekoppelten Nachrichtenspeicher muss der Status einer Nachricht berücksichtigt werden, bevor Sie dem MAPI-Spooler zum Herunterladen an einen Transportanbieter präsentiert wird. Es gibt Situationen, in denen eine Nachricht möglicherweise die MAPI-Spooler erfordert, aber die MAPI-Spooler sollte wirklich nicht beteiligt sein.
  
Betrachten Sie beispielsweise die Situation, in der ein Benutzer eine Nachricht aus dem Posteingang übermittelt. Der Client verwendet einen eng gekoppelten Speicher und Transport. Wenn der eng gekoppelte Nachrichtenspeicher den Speicherort der Nachricht als alleiniges Kriterium verwendet, um zu entscheiden, ob der MAPI-Spooler die Nachricht verarbeiten darf, wird die Nachricht vom MAPI-Spooler immer angezeigt. Um diese Art von Problem zu vermeiden, muss ein eng gekoppelter Nachrichtenspeicher zusätzlich zum Nachrichten Speicherort den Nachrichtenstatus überprüfen. Insbesondere sollte der Transportanbieter nicht anfordern, dass der MAPI-Spooler eine Nachricht herunterlädt, die aktiv übermittelt wird.
  
Der Nachrichtenübertragungsprozess umfasst den Nachrichtenspeicher Anbieter, einen oder mehrere Transportanbieter und MAPI. Die Themen in diesem Abschnitt enthalten detaillierte Informationen zu bestimmten Rollen im Nachrichtenübertragungsprozess.
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

