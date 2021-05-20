---
title: Senden von Nachrichten durch Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b34714a230adb44417624d149d34ed6a14a2dfa5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437609"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Senden von Nachrichten durch Nachrichtenspeicheranbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter sind nicht erforderlich, um ausgehende Nachrichtenübermittlungen zu unterstützen (d. h. die Möglichkeit für Clientanwendungen, den Nachrichtenspeicheranbieter zum Senden von Nachrichten zu verwenden). Clientanwendungen müssen beim Senden von Nachrichten einen Nachrichtenspeicher verwenden, da die Daten der Nachricht zwischen dem Zeitpunkt, zu dem der Benutzer mit dem Verfassen fertig ist, und dem Zeitpunkt, zu dem der MAPI-Spooler die Nachricht an einen Transportanbieter zur Übermittlung an das zugrunde liegende Messagingsystem übergibt, gespeichert werden müssen. Wenn Ihr Nachrichtenspeicheranbieter ausgehende Nachrichtenübermittlungen nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.
  
Um das Senden von Nachrichten zu unterstützen, muss Ihr Nachrichtenspeicheranbieter die folgenden Schritte unternehmen:
  
- Implementieren sie eine Warteschlange für ausgehende Nachrichten.
    
- Unterstützt die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) für Nachrichtenobjekte, die im Nachrichtenspeicher erstellt wurden. 
    
- Unterstützt die **IMsgStore-Methoden,** die für den MAPI-Spooler spezifisch sind: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)und [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
Die **SetLockState-Methode** ist wichtig für eine ordnungsgemäße Zusammenarbeit zwischen dem MAPI-Spooler und Clients. Wenn der MAPI-Spooler **SetLockState** für eine ausgehende Nachricht aufruft, darf der Nachrichtenspeicheranbieter die Nachricht nicht von Clients öffnen lassen. Wenn ein Client versucht, eine Nachricht zu öffnen, die durch den MAPI-Spooler gesperrt ist, sollte der Nachrichtenspeicheranbieter MAPI_E_NO_ACCESS. Der gesperrte Status einer Nachricht muss nicht dauerhaft sein, wenn der Speicher heruntergefahren wird, während die Nachricht vom MAPI-Spooler gesperrt wird. 
  
Unabhängig davon, ob der MAPI-Spooler eine ausgehende Nachricht gesperrt hat, sollte der Nachrichtenspeicheranbieter nicht zulassen, dass eine Nachricht in der Warteschlange für ausgehende Nachrichten zum Schreiben geöffnet wird. Wenn ein Client die [IMSgStore::OpenEntry-Methode](imsgstore-openentry.md) für eine ausgehende Nachricht mit dem Flag MAPI_MODIFY aufruft, sollte der Aufruf fehlschlagen und MAPI_E_SUBMITTED. Wenn eine Clientanwendung **OpenEntry** für eine ausgehende Nachricht mit dem MAPI_BEST_ACCESS aufruft, sollte der Nachrichtenspeicheranbieter schreibgeschützten Zugriff auf die Nachricht zulassen. 
  
Wenn eine Nachricht vom #A0 verarbeitet werden soll, legt der Nachrichtenspeicheranbieter die **eigenschaft PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) der Nachricht auf SUBMITFLAG_LOCKED. Der SUBMITFLAG_LOCKED gibt an, dass der MAPI-Spooler die Nachricht für die exklusive Verwendung gesperrt hat. Der andere Wert für **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, wird festgelegt, wenn für die Nachricht eine Vorverarbeitung durch eine oder mehrere von einem Transportanbieter registrierte Präprozessorfunktionen erforderlich ist.
  
In den folgenden Verfahren wird beschrieben, wie der Nachrichtenspeicher, der Transport und der MAPI-Spooler interagieren, um eine Nachricht von einem Client an einen oder mehrere Empfänger zu senden. 
  
Die Clientanwendung ruft die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf. In **SubmitMessage** führt der Nachrichtenspeicheranbieter die folgenden Schritte aus:
  
1. Ruft [IMAPISupport::P repareSubmit auf.](imapisupport-preparesubmit.md) Wenn MAPI einen Fehler zurückgibt, gibt der Nachrichtenspeicheranbieter diesen Fehler an den Client zurück.
    
2. Legt das MSGFLAG_SUBMIT in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft der Nachricht fest.
    
3. Stellt sicher, dass eine Spalte für die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) -Eigenschaft in der Empfängertabelle enthalten ist, und legt diese auf FALSE fest, um anzugeben, dass noch kein Transport die Verantwortung für die Übertragung der Nachricht übernommen hat.
    
4. Legt Das Datum und die Uhrzeit der Ursprünge in der **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) -Eigenschaft fest.
    
5. Ruft [IMAPISupport::ExpandRecips auf,](imapisupport-expandrecips.md) um die folgenden Schritte zu tun: 
    
    1. Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
        
    2. Entfernen von Duplikaten.
        
    3. Überprüfen Sie die erforderliche Vorverarbeitung, und legen Sie, falls die Vorverarbeitung erforderlich ist, das flag NEEDS_PREPROCESSING und die **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md))-Eigenschaft, die für MAPI reserviert ist. 
        
    4. Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
    1. Legt die Nachricht in die ausgehende Warteschlange ein, SUBMITFLAG_PREPROCESS bit in der PR_SUBMIT_FLAGS **festgelegt** ist. 
        
    2. Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
        
    3. Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. Die MAPI-Warteschlange f�hrt die folgenden Aufgaben: 
    
       1. Sperrt die Nachricht durch Aufrufen von [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Führt die benötigte Vorverarbeitung durch Aufrufen aller Vorverarbeitungsfunktionen in der Reihenfolge der Registrierung aus. Transportanbieter rufen [IMAPISupport::RegisterPreprocessor auf,](imapisupport-registerpreprocessor.md) um Vorverarbeitungsfunktionen zu registrieren. 
            
       3. Ruft [IMessage::SubmitMessage](imessage-submitmessage.md) für die geöffnete Nachricht auf, um dem Nachrichtenspeicher anzugeben, dass die Vorverarbeitung abgeschlossen ist. 
    
Wenn keine Vorverarbeitung oder eine Vorverarbeitung und der MAPI-Spooler **"SubmitMessage"** ausgeführt wurde, führt der Nachrichtenspeicheranbieter im Clientprozess die folgenden Schritte aus: 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
    
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
    
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind: 
    
     - Ruft [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) auf, wenn die Nachricht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abgeschlossen hat. Der Nachrichtenfluss wird mit dem MAPI-Spooler fortgesetzt. 
    
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter nicht möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abgeschlossen hat:
    
       1. Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) -Eigenschaft identifiziert wird, sofern festgelegt.
            
       2. Löscht die Nachricht, **wenn PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) -Eigenschaft auf TRUE festgelegt wurde.
            
       3. Entsperrt die Nachricht, wenn sie gesperrt ist.
            
       4. Gibt an den Client zurück. Der Nachrichtenfluss ist abgeschlossen.
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht vorverarbeitet wurde oder der Anbieter möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abgeschlossen hat:
    
    1. Ruft [IMAPISupport::CompleteMsg auf.](imapisupport-completemsg.md) 
          
    2. Setzt den Nachrichtenfluss mit dem MAPI-Spooler fort. Weitere Informationen finden Sie unter [Sending Messages: MAPI Spooler Tasks](sending-messages-mapi-spooler-tasks.md).
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Anbieter nicht möchte, dass der Spooler die Nachrichtenverarbeitung abgeschlossen hat:
    
    1. Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der **PR_SENTMAIL_ENTRYID** festgelegt ist. 
        
    2. Löscht die Nachricht, **wenn die PR_DELETE_AFTER_SUBMIT** auf TRUE festgelegt wurde. 
        
    3. Entsperrt die Nachricht, wenn sie gesperrt ist. 
        
    4. Gibt an den Anrufer zurück. Der Nachrichtenfluss ist abgeschlossen.
    
- F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
  1. Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
    
  2. Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
    
  3. Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

