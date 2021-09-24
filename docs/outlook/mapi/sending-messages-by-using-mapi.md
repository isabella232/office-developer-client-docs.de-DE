---
title: Senden von Nachrichten mithilfe von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c54271a24f149ef459b5646022b23823e4fbc1c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550057"
---
# <a name="sending-messages-by-using-mapi"></a>Senden von Nachrichten mithilfe von MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen rufen die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um eine Nachricht zu senden. **SubmitMessage** ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf, um die Nachricht zu speichern, bevor die Steuerung an den MAPI-Spooler oder direkt an einen Transportanbieter übertragen wird. 
  
Der MAPI-Spooler empfängt die Nachricht, wenn einer der folgenden Auftritte auftritt:
  
- Der Nachrichtenspeicheranbieter und der Transportanbieter sind nicht eng miteinander verbunden.
    
- Die Nachricht muss vorverarbeitet werden.
    
- Der eng gekoppelte Nachrichtenspeicher und -transport kann nicht alle Empfänger verarbeiten, an die die Nachricht adressiert ist.
    
Ein eng gekoppelter Nachrichtenspeicher muss den Status einer Nachricht berücksichtigen, bevor er dem MAPI-Spooler angezeigt wird, um auf einen Transportanbieter heruntergeladen zu werden. Es gibt Situationen, in denen eine Nachricht möglicherweise den MAPI-Spooler erfordert, aber der MAPI-Spooler wirklich nicht beteiligt sein sollte.
  
Stellen Sie sich beispielsweise die Situation vor, in der ein Benutzer eine Nachricht aus dem Posteingang sendet. Der Client verwendet einen eng gekoppelten Speicher und Transport. Wenn der eng gekoppelte Nachrichtenspeicher den Speicherort der Nachricht als einziges Kriterium für die Entscheidung verwendet, ob der MAPI-Spooler die Verarbeitung der Nachricht zulassen soll, empfängt der MAPI-Spooler immer die Nachricht. Um diese Art von Problem zu vermeiden, muss ein eng gekoppelter Nachrichtenspeicher den Nachrichtenstatus zusätzlich zum Nachrichtenspeicherort überprüfen. Insbesondere sollte der Transportanbieter nicht anfordern, dass der MAPI-Spooler eine Nachricht herunterlädt, die aktiv übermittelt wird.
  
Der Nachrichtenübertragungsprozess umfasst den Nachrichtenspeicheranbieter, einen oder mehrere Transportanbieter und die MAPI. Die Themen in diesem Abschnitt enthalten ausführliche Informationen zu bestimmten Rollen im Nachrichtenübertragungsprozess.
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

