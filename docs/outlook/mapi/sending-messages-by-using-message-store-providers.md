---
title: Senden von Nachrichten durch Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6469f039b9a70eb12c4dd137aefbdbd1472fdee2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598997"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Senden von Nachrichten durch Nachrichtenspeicheranbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter müssen ausgehende Nachrichtenübermittlungen nicht unterstützen (d. a. die Möglichkeit für Clientanwendungen, den Nachrichtenspeicheranbieter zum Senden von Nachrichten zu verwenden). Clientanwendungen müssen beim Senden von Nachrichten einen Nachrichtenspeicher verwenden, da die Daten der Nachricht zwischen dem Zeitpunkt, zu dem der Benutzer die Erstellung abgeschlossen hat, und dem Zeitpunkt, zu dem der MAPI-Spooler die Nachricht an einen Transportanbieter zur Übermittlung an das zugrunde liegende Messagingsystem übergibt, gespeichert werden müssen. Wenn Ihr Nachrichtenspeicheranbieter ausgehende Nachrichtenübermittlungen nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.
  
Um das Senden von Nachrichten zu unterstützen, muss Ihr Nachrichtenspeicheranbieter Folgendes tun:
  
- Implementieren sie eine Warteschlange für ausgehende Nachrichten.
    
- Unterstützen Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) für Nachrichtenobjekte, die im Nachrichtenspeicher erstellt wurden. 
    
- Unterstützen Sie die für den MAPI-Spooler spezifischen **IMsgStore-Methoden:** [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)und [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
Die **SetLockState-Methode** ist wichtig für die ordnungsgemäße Interoperabilität zwischen dem MAPI-Spooler und den Clients. Wenn der MAPI-Spooler **SetLockState** für eine ausgehende Nachricht aufruft, darf der Nachrichtenspeicheranbieter clients nicht zulassen, die Nachricht zu öffnen. Wenn ein Client versucht, eine Nachricht zu öffnen, die durch den MAPI-Spooler gesperrt ist, sollte der Nachrichtenspeicheranbieter MAPI_E_NO_ACCESS zurückgeben. Der Sperrstatus einer Nachricht muss nicht dauerhaft sein, falls der Speicher heruntergefahren wird, während die Nachricht durch den MAPI-Spooler gesperrt wird. 
  
Unabhängig davon, ob der MAPI-Spooler eine ausgehende Nachricht gesperrt hat, sollte der Nachrichtenspeicheranbieter nicht zulassen, dass eine Nachricht in der Warteschlange für ausgehende Nachrichten zum Schreiben geöffnet wird. Wenn ein Client die [IMSgStore::OpenEntry-Methode](imsgstore-openentry.md) für eine ausgehende Nachricht mit dem Flag MAPI_MODIFY aufruft, sollte der Aufruf fehlschlagen und MAPI_E_SUBMITTED zurückgeben. Wenn eine Clientanwendung **OpenEntry** für eine ausgehende Nachricht mit dem Flag MAPI_BEST_ACCESS aufruft, sollte der Nachrichtenspeicheranbieter schreibgeschützten Zugriff auf die Nachricht zulassen. 
  
Wenn eine Nachricht vom MAPI-Spooler verarbeitet werden soll, legt der Nachrichtenspeicheranbieter die **Eigenschaft PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) der Nachricht auf SUBMITFLAG_LOCKED fest. Der wert SUBMITFLAG_LOCKED gibt an, dass der MAPI-Spooler die Nachricht für die ausschließliche Verwendung gesperrt hat. Der andere Wert für **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht eine Vorverarbeitung durch eine oder mehrere von einem Transportanbieter registrierte Präprozessorfunktionen erfordert.
  
In den folgenden Verfahren wird beschrieben, wie der Nachrichtenspeicher, der Transport und der MAPI-Spooler interagieren, um eine Nachricht von einem Client an einen oder mehrere Empfänger zu senden. 
  
Die Clientanwendung ruft die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf. In **SubmitMessage** führt der Nachrichtenspeicheranbieter Folgendes aus:
  
1. Ruft [IMAPISupport::P repareSubmit auf.](imapisupport-preparesubmit.md) Wenn die MAPI einen Fehler zurückgibt, gibt der Nachrichtenspeicheranbieter diesen Fehler an den Client zurück.
    
2. Legt das MSGFLAG_SUBMIT Bit in der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht fest.
    
3. Stellt sicher, dass eine Spalte für die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) in der Empfängertabelle vorhanden ist, und legt sie auf FALSE fest, um anzugeben, dass noch kein Transport die Verantwortung für die Übertragung der Nachricht übernommen hat.
    
4. Legt das Datum und die Uhrzeit des Ursprungs in der **eigenschaft PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) fest.
    
5. Ruft [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) auf, um Folgendes zu tun: 
    
    1. Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
        
    2. Entfernen von Duplikaten.
        
    3. Überprüfen Sie, ob eine erforderliche Vorverarbeitung erforderlich ist, und legen Sie, falls die Vorverarbeitung erforderlich ist, das flag NEEDS_PREPROCESSING und die **eigenschaft PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) fest, die für die MAPI reserviert ist. 
        
    4. Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
    1. Versetzt die Nachricht in die ausgehende Warteschlange, wobei das SUBMITFLAG_PREPROCESS Bit in der **eigenschaft PR_SUBMIT_FLAGS** festgelegt ist. 
        
    2. Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
        
    3. Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. Die MAPI-Warteschlange f�hrt die folgenden Aufgaben: 
    
       1. Sperrt die Nachricht, indem [IMsgStore::SetLockState](imsgstore-setlockstate.md)aufgerufen wird.
            
       2. Führt die erforderliche Vorverarbeitung durch, indem alle Vorverarbeitungsfunktionen in der Reihenfolge der Registrierung aufgerufen werden. Transportanbieter rufen [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) auf, um Vorverarbeitungsfunktionen zu registrieren. 
            
       3. Ruft [IMessage::SubmitMessage](imessage-submitmessage.md) in der geöffneten Nachricht auf, um dem Nachrichtenspeicher anzugeben, dass die Vorverarbeitung abgeschlossen ist. 
    
Wenn keine Vorverarbeitung oder eine Vorverarbeitung vorhanden war und der MAPI-Spooler **"SubmitMessage"** aufgerufen wurde, führt der Nachrichtenspeicheranbieter im Clientprozess Folgendes aus: 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
    
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
    
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind: 
    
     - Ruft [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) auf, wenn die Nachricht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abschließt. Der Nachrichtenfluss wird mit dem MAPI-Spooler fortgesetzt. 
    
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter nicht möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abschließt:
    
       1. Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der **Eigenschaft PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) identifiziert wird, sofern festgelegt.
            
       2. Löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) -Eigenschaft auf TRUE festgelegt wurde.
            
       3. Entsperrt die Nachricht, wenn sie gesperrt ist.
            
       4. Gibt an den Client zurück. Der Nachrichtenfluss ist abgeschlossen.
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht vorverarbeitet wurde oder der Anbieter möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abschließt:
    
    1. Ruft [IMAPISupport::CompleteMsg](imapisupport-completemsg.md)auf. 
          
    2. Setzt den Nachrichtenfluss mit dem MAPI-Spooler fort. Weitere Informationen finden Sie unter [Senden von Nachrichten: MAPI Spooler Tasks](sending-messages-mapi-spooler-tasks.md).
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Anbieter nicht möchte, dass der Spooler die Nachrichtenverarbeitung abschließt:
    
    1. Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der **PR_SENTMAIL_ENTRYID** Eigenschaft identifiziert wird, sofern festgelegt. 
        
    2. Löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT-Eigenschaft** auf TRUE festgelegt wurde. 
        
    3. Entsperrt die Nachricht, wenn sie gesperrt ist. 
        
    4. Gibt an den Aufrufer zurück. Der Nachrichtenfluss ist abgeschlossen.
    
- F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
  1. Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
    
  2. Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
    
  3. Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

