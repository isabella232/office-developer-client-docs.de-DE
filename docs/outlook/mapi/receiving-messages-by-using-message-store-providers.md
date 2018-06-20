---
title: Empfangen von Nachrichten mithilfe von Nachrichtenspeicher Rollenanbietern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 94ea0fe7fba4e49c1f646d889f3727cf5ef4739d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795346"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Empfangen von Nachrichten mithilfe von Nachrichtenspeicher Rollenanbietern

  
  
**Betrifft**: Outlook 
  
Nachricht-Anbieter müssen keine eingehenden Nachrichtenübermittlungen unterstützen (d. h., unterstützen die Möglichkeit zu Nachrichten Transportanbieter und die Warteschlange MAPI-Anbieter als Ausgangspunkt Übermittlung von Nachrichten Filiale). Jedoch, wenn Ihre Nachricht Speicheranbieter eingehende Nachrichtenübermittlungen nicht unterstützt, kann es als Standard-Informationsspeicher verwendet werden.
  
Zur Unterstützung der eingehenden Nachrichtenübermittlungen muss ein Speicheranbieter Nachricht Folgendes ausführen:
  
- Unterstützt die Methoden [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) und [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) -Clientanwendungen eingehende Nachrichten suchen können. 
    
- Unterstützung für die [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) -Methode, damit die MAPI-Warteschlange den Nachricht Speicheranbieter informieren kann, den eine neue Nachricht empfangen hat. 
    
- Implementieren Sie Benachrichtigungen, damit Clients für die Benachrichtigung über eine neue Nachricht registrieren können. Benachrichtigungen sind optional, jedoch zu Ihrem Anbieter sollte implementieren.
    
Die Reihenfolge der Methodenaufrufe, die auftritt, wenn eine eingehende Nachricht an einen Nachrichtenspeicher übermittelt werden lautet wie folgt:
  
1. Die MAPI-Warteschlange ruft [IMsgStore::OpenEntry](imsgstore-openentry.md) mit der Posteingang [EntryID](entryid.md) eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle abrufen. 
    
2. Die MAPI-Warteschlange ruft [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) zum Abrufen einer neuen Nachricht-Objekts. 
    
3. Die MAPI-Warteschlange übergibt das Message-Objekt an der Adressbuchhierarchie.
    
4. Der Transportdienst füllt Nachrichteneigenschaften mit Daten aus dem zugrunde liegenden messaging-System und das Meldungsobjekt [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen. 
    
5. Der Nachricht Speicheranbieter verwendet seine Benachrichtigungsmethode registrierte Clients informiert, die eine neue Nachricht empfangen hat.
    
6. Der Nachrichtenspeicher [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) -Methode aufgerufen, die MAPI-Warteschlange. 
    
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

