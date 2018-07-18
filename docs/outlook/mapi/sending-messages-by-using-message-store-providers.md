---
title: Sendende von Nachrichten mithilfe der Nachricht speichern-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aaba816ca7efab6cee939087a18332561f31b81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795488"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Sendende von Nachrichten mithilfe der Nachricht speichern-Anbieter

**Betrifft**: Outlook 
  
Nachricht Anbieter sind nicht erforderlich, zur Unterstützung von ausgehenden Nachrichtenübermittlungen (d. h., die Möglichkeit für Clientanwendungen Anbieter die Nachricht zum Senden von Nachrichten verwenden). Clientanwendungen müssen einen Nachrichtenspeicher verwenden beim Senden von Nachrichten, da die Nachricht Daten sein müssen an Stelle gespeicherten Verfassen Sie zwischen der Uhrzeit des Endes der Benutzer ist es und die Zeit, die die MAPI-Warteschlange auf einem Transportdienstes für die Nachricht ermöglicht Übermittlung an die zugrunde liegenden messaging-System. Wenn Ihre Nachricht Speicheranbieter ausgehende Nachrichtenübermittlungen nicht unterstützt, kann es als Standard-Informationsspeicher verwendet werden.
  
Zum sendende von Nachrichten unterstützt, muss Ihre Nachricht Speicheranbieter Folgendes ausführen:
  
- Implementieren Sie eine Warteschlange für ausgehende Nachrichten.
    
- Unterstützung für die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode auf Message-Objekte im Nachrichtenspeicher erstellt. 
    
- Unterstützen die **IMsgStore** -Methoden, die speziell für die MAPI-Warteschlange sind: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)und [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
Die **SetLockState** -Methode ist wichtig für die ordnungsgemäße Interoperation zwischen dem MAPI-Warteschlange und Clients. Wenn die MAPI-Warteschlange für eine ausgehende Nachricht **SetLockState** aufruft, muss der Nachricht Informationsdienst nicht Clients, die die Nachricht nicht öffnen lassen. Wenn ein Client versucht, eine Nachricht zu öffnen, die durch die MAPI-Warteschlange gesperrt ist, sollte der Nachricht Speicheranbieter MAPI_E_NO_ACCESS zurückgegeben. Der Sperrstatus einer Nachricht benötigt keinen beständigen werden für den Fall, dass Sie der Speicher heruntergefahren wird, während die Nachricht durch die MAPI-Warteschlange gesperrt ist. 
  
Unabhängig davon, ob die MAPI-Warteschlange eine ausgehende Nachricht gesperrt hat sollte die Nachricht Informationsdienst keine Meldung in der Warteschlange für ausgehende Nachrichten, die zum Schreiben geöffnet werden zulassen. Wenn ein Client die [IMSgStore::OpenEntry](imsgstore-openentry.md) -Methode für eine ausgehende Nachricht mit dem MAPI_MODIFY-Flag aufruft, sollte der Anruf fehl und MAPI_E_SUBMITTED zurückzugeben. Wenn eine Clientanwendung **OpenEntry** für eine ausgehende Nachricht mit dem MAPI_BEST_ACCESS-Flag aufruft, sollte der Nachricht Speicheranbieter schreibgeschützten Zugriff auf die Nachricht zulassen. 
  
Wenn eine Nachricht von den MAPI-Warteschlange verarbeitet werden, wird der Nachricht Speicheranbieter die Nachricht **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))-Eigenschaft auf SUBMITFLAG_LOCKED. Der Wert SUBMITFLAG_LOCKED gibt an, dass die MAPI-Warteschlange die Nachricht zur ausschließlichen Verwendung gesperrt hat. Der andere Wert für **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht der vorverarbeitung durch eine oder mehrere Präprozessor – Funktionen, die von einem Transportanbieter registriert muss.
  
Die folgenden Verfahren wird beschrieben, wie die Nachrichtenspeicher, Transport- und MAPI-Warteschlange interagieren, um eine Nachricht von einem Client an einen oder mehrere Empfänger senden. 
  
Die Clientanwendung ruft die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode. In **SubmitMessage**führt der Nachrichtenanbieter Folgendes aus:
  
1. Ruft die [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). Wenn MAPI einen Fehler zurückgibt, gibt der Anbieter für die Nachricht anmelden, Fehler an den Client zurück.
    
2. Legt die MSGFLAG_SUBMIT bit in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht.
    
3. Stellt sicher, dass eine Spalte für die Eigenschaft **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) in der Tabelle Empfänger und wird auf false fest, um anzugeben, dass kein Transport noch Verantwortung für die Übertragung der Nachricht angenommen hat.
    
4. Legt das Datum und die Uhrzeit der Aufnahme in der Eigenschaft **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Ruft die [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) die folgenden Aufgaben: 
    
    1. Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
        
    2. Entfernen von Duplikaten.
        
    3. Prüfen Sie, ob alle erforderlichen vorverarbeitung und, wenn der vorverarbeitung erforderlich ist, legen Sie das Kennzeichen NEEDS_PREPROCESSING und die **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md))-Eigenschaft, die für die MAPI reserviert ist. 
        
    4. Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
    1. Versetzt die Nachricht in der ausgehenden Warteschlange mit dem SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festgelegt. 
        
    2. Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
        
    3. Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. Die MAPI-Warteschlange f�hrt die folgenden Aufgaben: 
    
       1. Sperrt die Nachricht durch Aufrufen von [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Führt die erforderlichen vorverarbeitung durch Aufrufen von alle vorverarbeitenden Funktionen in der Reihenfolge der Registrierung. Transportanbieter Aufrufen [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) um vorverarbeitenden Funktionen zu registrieren. 
            
       3. Anrufe [IMessage::SubmitMessage](imessage-submitmessage.md) auf der geöffneten Nachricht an, dass die Nachricht gespeichert, der vorverarbeitung ist abgeschlossen. 
    
Wenn es wurde keine vorverarbeitung, oder es wurde der vorverarbeitung und die MAPI-Warteschlange aufgerufen **SubmitMessage**, Anbieter die Nachricht wird in der Clientprozess Folgendes: 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
    
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
    
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind: 
    
     - Wenn die Nachricht vorverarbeitet wurde oder der Nachricht Speicheranbieter die MAPI-Warteschlange zur vollständigen Nachricht, die Verarbeitung möchte von Anrufen [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) . Nachrichtenfluss mit der MAPI-Warteschlange wird fortgesetzt. 
    
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachricht Speicheranbieter nicht die MAPI-Warteschlange zum Abschließen der Verarbeitung von Nachrichten möchte:
    
       1. Legen Sie die Kopien die Nachricht in den Ordner von der Eintrags-ID in der Eigenschaft **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) identifiziert.
            
       2. Löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf TRUE festgelegt wurde.
            
       3. Entsperrt die Nachricht, wenn sie gesperrt ist.
            
       4. Gibt an den Client. Nachrichtenfluss ist abgeschlossen.
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht vorverarbeitet wurde oder der Anbieter die MAPI-Warteschlange zum Abschließen der Verarbeitung von Nachrichten möchte:
    
    1. Ruft die [IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Nachrichtenfluss mit der MAPI-Warteschlange weiter. Weitere Informationen finden Sie unter [Nachrichten senden: MAPI-Warteschlange Aufgaben](sending-messages-mapi-spooler-tasks.md).
    
  - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Anbieter nicht die Warteschlange zum Abschließen der Verarbeitung von Nachrichten möchte:
    
    1. Kopien legen Sie die Nachricht in den Ordner, der durch die Eintrags-ID in der **PR_SENTMAIL_ENTRYID** -Eigenschaft, sofern bezeichnet wird. 
        
    2. Löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT** -Eigenschaft auf TRUE festgelegt wurde. 
        
    3. Entsperrt die Nachricht, wenn sie gesperrt ist. 
        
    4. Gibt für den Anrufer. Nachrichtenfluss ist abgeschlossen.
    
- F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
  1. Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
    
  2. Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
    
  3. Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

