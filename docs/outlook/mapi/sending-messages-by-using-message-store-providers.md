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
  
Nachrichtenspeicher Anbieter sind nicht zur Unterstützung ausgehender Nachrichtenübermittlungen erforderlich (also die Möglichkeit, dass Clientanwendungen den Nachrichtenspeicher Anbieter zum Senden von Nachrichten verwenden können). Client Anwendungen müssen beim Senden von Nachrichten einen Nachrichtenspeicher verwenden, da die Daten der Nachricht irgendwo zwischen dem Zeitpunkt gespeichert werden müssen, zu dem der Benutzer Sie erstellt hat, und der Zeit, die der MAPI-Spooler die Nachricht an einen Transportanbieter für Übermittlung an das zugrunde liegende Messagingsystem. Wenn der Nachrichtenspeicher Anbieter ausgehende Nachrichten nicht unterstützt, kann er nicht als Standardnachrichtenspeicher verwendet werden.
  
Um das Senden von Nachrichten zu unterstützen, muss der Nachrichtenspeicher Anbieter folgende Schritte ausführen:
  
- Implementieren Sie eine Warteschlange für ausgehende Nachrichten.
    
- Unterstützen Sie die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode für Nachrichtenobjekte, die im Nachrichtenspeicher erstellt werden. 
    
- Unterstützen Sie die **IMsgStore** -Methoden, die für den MAPI-Spooler spezifisch sind: [IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)und [IMsgStore:: SetLockState](imsgstore-setlockstate.md).
    
Die **SetLockState** -Methode ist wichtig für eine ordnungsgemäße Zusammenarbeit zwischen dem MAPI-Spooler und den Clients. Wenn der MAPI-Spooler **SetLockState** für eine ausgehende Nachricht aufruft, darf der Nachrichtenspeicher Anbieter die Nachricht nicht öffnen. Wenn ein Client versucht, eine vom MAPI-Spooler gesperrte Nachricht zu öffnen, sollte der Nachrichtenspeicher Anbieter MAPI_E_NO_ACCESS zurückgeben. Der gesperrte Status einer Nachricht muss nicht persistent sein, wenn der Speicher heruntergefahren wird, während die Nachricht vom MAPI-Spooler gesperrt wird. 
  
Unabhängig davon, ob der MAPI-Spooler eine ausgehende Nachricht gesperrt hat, sollte der Nachrichtenspeicher Anbieter nicht zulassen, dass eine Nachricht in der Warteschlange für ausgehende Nachrichten zum Schreiben geöffnet wird. Wenn ein Client die [IMSgStore:: OpenEntry](imsgstore-openentry.md) -Methode für eine ausgehende Nachricht mit dem MAPI_MODIFY-Flag aufruft, sollte der Aufruf fehlschlagen und MAPI_E_SUBMITTED zurückgeben. Wenn eine Clientanwendung **OpenEntry** für eine ausgehende Nachricht mit dem MAPI_BEST_ACCESS-Flag aufruft, sollte der Nachrichtenspeicher Anbieter schreibgeschützten Zugriff auf die Nachricht zulassen. 
  
Wenn eine Nachricht vom MAPI-Spooler verarbeitet werden soll, legt der Nachrichtenspeicher Anbieter die **PR_SUBMIT_FLAGS** ([pidtagsubmitflags (](pidtagsubmitflags-canonical-property.md))-Eigenschaft der Nachricht auf SUBMITFLAG_LOCKED fest. Der SUBMITFLAG_LOCKED-Wert gibt an, dass die MAPI-Warteschlange die Nachricht für ihre exklusive Verwendung gesperrt hat. Der andere Wert für **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht die Vorverarbeitung durch eine oder mehrere präprozessorfunktionen erfordert, die von einem Transportanbieter registriert werden.
  
In den folgenden Verfahren wird beschrieben, wie Nachrichtenspeicher, Transport und MAPI-Spooler interagieren, um eine Nachricht von einem Client an einen oder mehrere Empfänger zu senden. 
  
Die Clientanwendung Ruft die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf. In **SubmitMessage**führt der Nachrichtenspeicher Anbieter folgende Aktionen aus:
  
1. Ruft [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md). Wenn MAPI einen Fehler zurückgibt, gibt der Nachrichtenspeicher Anbieter diesen Fehler an den Client zurück.
    
2. Legt das MSGFLAG_SUBMIT-Bit in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht fest.
    
3. Stellt sicher, dass eine Spalte für die **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft in der Recipient-Tabelle vorhanden ist, und legt Sie auf false fest, um anzugeben, dass noch kein Transport die Verantwortung für die Übertragung der Nachricht übernommen hat.
    
4. Legt das Datum und die Uhrzeit der Ursprung in der **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))-Eigenschaft.
    
5. Ruft [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) auf, um folgende Aufgaben auszuführen: 
    
    1. Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
        
    2. Entfernen von Duplikaten.
        
    3. Überprüfen Sie, ob die erforderliche Vorverarbeitung erforderlich ist, und legen Sie das NEEDS_PREPROCESSING-Flag und die **PR_PREPROCESS** ([pidtagpreprocess (](pidtagpreprocess-canonical-property.md))-Eigenschaft fest, die für MAPI reserviert ist. 
        
    4. Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
    1. Platziert die Nachricht in der ausgehenden Warteschlange mit dem SUBMITFLAG_PREPROCESS-Bit, das in der **PR_SUBMIT_FLAGS** -Eigenschaft festgelegt ist. 
        
    2. Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
        
    3. Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. Die MAPI-Warteschlange f�hrt die folgenden Aufgaben: 
    
       1. Sperrt die Nachricht durch Aufrufen von [IMsgStore:: SetLockState](imsgstore-setlockstate.md).
            
       2. Führt die erforderliche Vorverarbeitung aus, indem alle Vorverarbeitungsfunktionen in der Reihenfolge der Registrierung aufgerufen werden. Transport Anbieter rufen [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) auf, um Vorverarbeitungsfunktionen zu registrieren. 
            
       3. Ruft [IMessage:: SubmitMessage](imessage-submitmessage.md) für die offene Nachricht auf, um dem Nachrichtenspeicher anzuzeigen, dass die Vorverarbeitung abgeschlossen ist. 
    
Wenn es keine Vorverarbeitung oder eine Vorverarbeitung gab, und der MAPI-Spooler namens **SubmitMessage**, führt der Nachrichtenspeicher Anbieter im Clientprozess folgende Aktionen aus: 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
    
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
    
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind: 
    
     - Ruft [IMAPISupport:: CompleteMsg](imapisupport-completemsg.md) auf, wenn die Nachricht vorverarbeitet wurde oder der Nachrichtenspeicher Anbieter den MAPI-Spooler zum Abschließen der Nachrichtenverarbeitung wünscht. Der Nachrichtenfluss wird mit dem MAPI-Spooler fortgesetzt. 
    
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachrichtenspeicher Anbieter nicht möchten, dass die Nachrichtenverarbeitung vom MAPI-Spooler abgeschlossen wird:
    
       1. Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft identifiziert wird, falls festgelegt.
            
       2. Löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT** ([pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf true festgelegt wurde.
            
       3. Hebt die Sperre der Nachricht auf, wenn Sie gesperrt ist.
            
       4. Gibt den Client zurück. Der Nachrichtenfluss ist abgeschlossen.
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht vorverarbeitet wurde oder der Anbieter den MAPI-Spooler zum Abschließen der Nachrichtenverarbeitung wünscht:
    
    1. Ruft [IMAPISupport:: CompleteMsg](imapisupport-completemsg.md)auf. 
          
    2. Setzt den Nachrichtenfluss mit dem MAPI-Spooler fort. Weitere Informationen finden Sie unter [Senden von Nachrichten: MAPI](sending-messages-mapi-spooler-tasks.md)-spoolEr-Aufgaben.
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder wenn der Spooler die Nachrichtenverarbeitung nicht abschließen soll:
    
    1. Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der **PR_SENTMAIL_ENTRYID** -Eigenschaft identifiziert wird, falls festgelegt. 
        
    2. Löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT** -Eigenschaft auf true festgelegt wurde. 
        
    3. Hebt die Sperre der Nachricht auf, wenn Sie gesperrt ist. 
        
    4. Gibt den Aufrufer zurück. Der Nachrichtenfluss ist abgeschlossen.
    
- F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
  1. Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
    
  2. Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
    
  3. Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

