---
title: Empfangen von Nachrichten mithilfe von Store Anbietern
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
# <a name="receiving-messages-by-using-message-store-providers"></a>Empfangen von Nachrichten mithilfe von Store Anbietern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter müssen eingehende Nachrichtenübermittlungen nicht unterstützen (d. h. sie unterstützen die Möglichkeit für Transportanbieter und den MAPI-Spooler, den Nachrichtenspeicheranbieter als Zustellungspunkt für Nachrichten zu verwenden). Wenn ihr Nachrichtenspeicheranbieter eingehende Nachrichtenübermittlungen jedoch nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.
  
Um eingehende Nachrichtenübermittlungen zu unterstützen, muss Ihr Nachrichtenspeicheranbieter die folgenden Schritte unternehmen:
  
- Unterstützen Sie [die Methoden IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) und [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) damit Clientanwendungen eingehende Nachrichten finden können. 
    
- Unterstützen Sie [die IMsgStore::NotifyNewMail-Methode,](imsgstore-notifynewmail.md) damit der MAPI-Spooler den Nachrichtenspeicheranbieter darüber informieren kann, dass eine neue Nachricht eingetroffen ist. 
    
- Implementieren Sie Benachrichtigungen, damit Clients sich für neue Nachrichtenbenachrichtigungen registrieren können. Benachrichtigungen sind optional, aber Ihr Anbieter sollte sie implementieren.
    
Die Reihenfolge der Methodenaufrufe, die auftreten, wenn eine eingehende Nachricht an einen Nachrichtenspeicher zugestellt wird, lautet wie folgt:
  
1. Der MAPI-Spooler ruft [IMsgStore::OpenEntry](imsgstore-openentry.md) mit der Posteingangseintrags-ID auf, um eine [IMAPIFolder-Schnittstelle zu](imapifolderimapicontainer.md) erhalten. [](entryid.md) 
    
2. Der MAPI-Spooler ruft [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf, um ein neues Nachrichtenobjekt zu erhalten. 
    
3. Der MAPI-Spooler übergibt das Message-Objekt an den Transportanbieter.
    
4. Der Transportanbieter füllt die Eigenschaften der Nachricht mit Daten aus dem zugrunde liegenden Messagingsystem ein und ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des Nachrichtenobjekts auf. 
    
5. Der Nachrichtenspeicheranbieter verwendet seine Benachrichtigungsmethode, um registrierte Clients darüber zu informieren, dass eine neue Nachricht eingetroffen ist.
    
6. Der MAPI-Spooler ruft die [IMsgStore::NotifyNewMail-Methode des Nachrichtenspeichers](imsgstore-notifynewmail.md) auf. 
    
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

