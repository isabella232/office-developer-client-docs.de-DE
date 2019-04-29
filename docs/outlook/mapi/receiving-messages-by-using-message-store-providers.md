---
title: Empfangen von Nachrichten mithilfe von Nachrichtenspeicher Anbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418729"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Empfangen von Nachrichten mithilfe von Nachrichtenspeicher Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicher Anbieter müssen keine eingehenden Nachrichten unterstützen (das heißt, Sie unterstützen die Möglichkeit, dass Transportanbieter und der MAPI-Spooler den Nachrichtenspeicher Anbieter als Zustellungs Punkt für e-Mails verwenden können). Wenn jedoch der Nachrichtenspeicher Anbieter eingehende Nachrichten nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.
  
Zur Unterstützung eingehender Nachrichtenübermittlungen muss der Nachrichtenspeicher Anbieter folgende Schritte ausführen:
  
- Unterstützen Sie die Methoden [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) und [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) , sodass Clientanwendungen eingehende Nachrichten finden können. 
    
- Unterstützen Sie die [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) -Methode, sodass der MAPI-Spooler den Nachrichtenspeicher Anbieter informieren kann, dass eine neue Nachricht eingegangen ist. 
    
- Implementieren Sie Benachrichtigungen, damit Clients sich für neue Nachrichten Benachrichtigungen anmelden können. Benachrichtigungen sind optional, aber Ihr Anbieter sollte Sie implementieren.
    
Die Reihenfolge der Methodenaufrufe, die auftreten, wenn eine eingehende Nachricht an einen Nachrichtenspeicher übermittelt wird, lautet wie folgt:
  
1. Der MAPI-Warteschlangen Aufruf [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit der Posteingangs- [Eingabe](entryid.md) Aufforderung, um eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle abzurufen. 
    
2. Der MAPI-Spooler ruft [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf, um ein neues Message-Objekt abzurufen. 
    
3. Der MAPI-Spooler übergibt das Nachrichtenobjekt an den Transportanbieter.
    
4. Der Transportanbieter füllt die Eigenschaften der Nachricht mit Daten aus dem zugrunde liegenden Messagingsystem aus und ruft die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des Nachrichtenobjekts auf. 
    
5. Der Nachrichtenspeicher Anbieter verwendet seine Benachrichtigungsmethode, um registrierte Clients darüber zu informieren, dass eine neue Nachricht eingegangen ist.
    
6. Die MAPI-Warteschlange ruft die [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) -Methode des Nachrichtenspeichers auf. 
    
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

