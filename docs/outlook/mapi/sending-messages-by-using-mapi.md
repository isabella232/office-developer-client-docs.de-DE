---
title: Senden von Nachrichten mithilfe von MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795489"
---
# <a name="sending-messages-by-using-mapi"></a>Senden von Nachrichten mithilfe von MAPI

  
  
**Betrifft**: Outlook 
  
Clientanwendungen rufen Sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode, um eine Nachricht senden. **SubmitMessage** ruft [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , um die Nachricht vor der Weiterleitung Steuerelement entweder der MAPI-Warteschlange oder direkt an eines Transportdienstes zu speichern. 
  
Die MAPI-Warteschlange empfängt die Nachricht, wenn eines der folgenden auftreten:
  
- Die Nachrichtenanbieter und Adressbuchhierarchie sind nicht eng verknüpft.
    
- Die Nachricht muss der vorverarbeitung.
    
- Die eng gekoppelten Nachrichtenspeicher und Transport können nicht alle Empfänger behandeln, die an die Nachricht adressiert ist.
    
Ein eng gekoppelten Nachrichtenspeicher muss eine Nachricht den Status berücksichtigen, bevor sie es für die MAPI-Warteschlange auf eines Transportdienstes heruntergeladen werden anzeigt. Es gibt Situationen, in dem möglicherweise eine Meldung angezeigt, die MAPI-Warteschlange erforderlich ist, aber die MAPI-Warteschlange sollte wirklich nicht einbezogen werden.
  
Betrachten Sie beispielsweise die Situation, in dem ein Benutzer eine Nachricht aus dem Posteingang übermittelt. Der Client ist eng gekoppelten Speicher und Transport verwendet. Wenn der eng gekoppelten Nachrichtenspeicher Speicherort der Nachricht als einzige Kriterium für um dazu, ob die MAPI-Warteschlange zu entscheiden verwendet, um die Nachricht zu verarbeiten, erhält die MAPI-Warteschlange immer die Nachricht. Um diese Art des Problems zu vermeiden, muss ein eng gekoppelten Nachrichtenspeicher neben den Speicherort für Nachrichten die Nachricht den Status überprüfen. Der Transportdienst sollten insbesondere nicht anfordern, dass die MAPI-Warteschlange eine beliebige Nachricht herunterladen, die aktiv übermittelt wird.
  
Die Übertragung Nachricht umfasst die Nachricht Speicheranbieter, mindestens einen Transportanbieter und MAPI. Die Themen in diesem Abschnitt enthalten ausführliche Informationen zu speziellen Positionen bei der Übertragung.
  
## <a name="see-also"></a>Siehe auch



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

