---
title: Empfangen von Nachrichten mithilfe von Nachrichtenanbietern Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8b93327dd95ae24d69ec633ff12252bac8744c87
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550169"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Empfangen von Nachrichten mithilfe von Nachrichtenanbietern Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter müssen eingehende Nachrichtenübermittlungen nicht unterstützen (d. a. die Möglichkeit für Transportanbieter und den MAPI-Spooler, den Nachrichtenspeicheranbieter als Übermittlungspunkt für Nachrichten zu verwenden). Wenn Ihr Nachrichtenspeicheranbieter eingehende Nachrichtenübermittlungen jedoch nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.
  
Um eingehende Nachrichtenübermittlungen zu unterstützen, muss Ihr Nachrichtenspeicheranbieter Folgendes tun:
  
- Unterstützen Sie die Methoden [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) und [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) damit Clientanwendungen eingehende Nachrichten finden können. 
    
- Unterstützen Sie die [IMsgStore::NotifyNewMail-Methode,](imsgstore-notifynewmail.md) damit der MAPI-Spooler den Nachrichtenspeicheranbieter darüber informieren kann, dass eine neue Nachricht eingetroffen ist. 
    
- Implementieren Sie Benachrichtigungen, damit Clients sich für neue Nachrichtenbenachrichtigungen registrieren können. Benachrichtigungen sind optional, aber Ihr Anbieter sollte sie implementieren.
    
Die Abfolge der Methodenaufrufe, die beim Zugestellt einer eingehenden Nachricht an einen Nachrichtenspeicher ausgeführt werden, lautet wie folgt:
  
1. Der MAPI-Spooler ruft [IMsgStore::OpenEntry](imsgstore-openentry.md) mit der [Posteingangs-EntryID](entryid.md) auf, um eine [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) abzurufen. 
    
2. Der MAPI-Spooler ruft [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf, um ein neues Nachrichtenobjekt abzurufen. 
    
3. Der MAPI-Spooler übergibt das Nachrichtenobjekt an den Transportanbieter.
    
4. Der Transportanbieter füllt die Nachrichteneigenschaften mit Daten aus dem zugrunde liegenden Messagingsystem aus und ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des Nachrichtenobjekts auf. 
    
5. Der Nachrichtenspeicheranbieter verwendet seine Benachrichtigungsmethode, um registrierte Clients darüber zu informieren, dass eine neue Nachricht eingetroffen ist.
    
6. Der MAPI-Spooler ruft die [IMsgStore::NotifyNewMail-Methode](imsgstore-notifynewmail.md) des Nachrichtenspeichers auf. 
    
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

