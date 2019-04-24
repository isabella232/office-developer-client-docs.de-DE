---
title: Senden von Nachrichten Nachrichtenspeicher Anbieter Aufgaben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b65113e59b236b1f13596627a8669ae458f76369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338430"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Senden von Nachrichten: Aufgaben des Nachrichtenspeicher Anbieters

**Gilt für**: Outlook 2013 | Outlook 2016 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
Der Nachricht Informationsdienst bestimmt, ob er die MAPI-Warteschlange umfassen. Wenn die Nachricht Informationsdienst nicht eng verkn�pft ist, die Nachricht muss Vorverarbeitung, oder den eng gekoppelten Speicher und Transport k�nnen nicht bearbeitet werden alle Empf�nger, die MAPI-Warteschlange beteiligt sein muss. 
  
Das folgende Verfahren beschreibt die von einem Nachrichtenanbieter zum Senden einer Nachricht erforderlichen Aufgaben. 
  
**In IMessage:: SubmitMessage der Nachrichtenspeicher Anbieter**:
  
1. Ruft [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) , wenn die Nachricht das MSGFLAG_RESEND-Flag in seiner **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft festgelegt und Fehler an den Client zurückgibt. **PrepareSubmit** überprüft die **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft jedes Empfängers in der Empfängerliste der Nachricht.
    
   - Wenn das MAPI_SUBMITTED-Flag festgelegt ist, das angibt, dass der Empfänger die ursprüngliche Nachricht nicht empfangen hat, löscht **PrepareSubmit** das Flag und legt die **PR_RESPONSIBILITY** ([PIDTAGRESPONSIBILITY (](pidtagresponsibility-canonical-property.md))-Eigenschaft auf true fest. 
    
   - Wenn das Flag MAPI_SUBMITTED nicht festgelegt ist, der angibt, dass der Empf�nger der urspr�nglichen Nachricht erhalten hat, �ndert die Eigenschaft **PR_RECIPIENT_TYPE** in MAPI_P1 **PrepareSubmit** und die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE festgelegt und etwaige Fehler generierte **PrepareSubmit** an den Client zur�ckgegeben. 
    
2. Das Flag MSGFLAG_SUBMIT festgelegt in der Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft. 
    
3. Stellt sicher, dass eine Spalte f�r **PR_RESPONSIBILITY** in der Tabelle Empf�nger und wird auf false fest, um anzugeben, dass kein Transport noch angenommenen Verantwortung f�r die �bermittlung der Nachricht wurde. 
    
4. Legt das Datum und die Uhrzeit der Ursprung in der **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))-Eigenschaft.
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
   - Entfernen von Duplikaten.
   - Überprüfen Sie, ob eine erforderliche Vorverarbeitung erforderlich ist, und legen Sie das NEEDS_PREPROCESSING-Flag und die **PR_PREPROCESS** ([pidtagpreprocess (](pidtagpreprocess-canonical-property.md))-Eigenschaft, eine für MAPI reservierte Eigenschaft, fest, wenn die Vorverarbeitung erforderlich ist. 
   - Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
   - Platziert die Nachricht in der ausgehenden Warteschlange mit dem SUBMITFLAG_PREPROCESS-Bit, das in der **PR_SUBMIT_FLAGS** ([pidtagsubmitflags (](pidtagsubmitflags-canonical-property.md))-Eigenschaft festgelegt ist.
   - Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
   - Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. 
   - Die MAPI-Warteschlange f�hrt die folgenden Aufgaben:
     - Sperrt die Nachricht durch Aufrufen von IMsgStore:: SetLockState. 
     - Führt die erforderliche Vorverarbeitung aus, indem alle Vorverarbeitungsfunktionen in der Reihenfolge der Registrierung aufgerufen werden. Transport Anbieter rufen IMAPISupport:: RegisterPreprocessor auf, um Vorverarbeitungsfunktionen zu registrieren. 
     - Ruft IMessage:: SubmitMessage für die offene Nachricht auf, um dem Nachrichtenspeicher anzuzeigen, dass die Vorverarbeitung abgeschlossen ist.

<br/>

Die folgenden beiden Schritte werden im Clientprozess ausgeführt, wenn keine Vorverarbeitung vorliegt, und wenn der MAPI-Spooler **SubmitMessage** aufruft, wenn eine Vorverarbeitung vorliegt. 

**Nachrichtenspeicher Anbieter**:

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind:
     - Ruft IMAPISupport:: CompleteMsg auf, wenn die Nachricht vorverarbeitet wurde oder der Nachrichtenspeicher Anbieter wünscht, dass der MAPI-Spooler die Nachrichtenverarbeitung durchführt, die empfohlen wird, damit Messaging-Hooks aufgerufen werden können. Der Nachrichtenfluss wird mit dem MAPI-Spooler fortgesetzt, wie im folgenden Verfahren beschrieben.  
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachrichtenspeicher Anbieter nicht möchten, dass die Nachrichtenverarbeitung vom MAPI-Spooler abgeschlossen wird:
       - Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der PR_SENTMAIL_ENTRYID (Pidtagsentmailentryid ()-Eigenschaft identifiziert wird, falls festgelegt.
       - Löscht die Nachricht, wenn die PR_DELETE_AFTER_SUBMIT (Pidtagdeleteaftersubmit ()-Eigenschaft auf TRUE festgelegt wurde.
       - Hebt die Sperre der Nachricht auf, wenn Sie gesperrt ist.
       - Gibt den Client zurück. Der Nachrichtenfluss ist abgeschlossen. 
   
2. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
   - Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
   - Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
   - Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
Wenn eine Nachricht von den MAPI-Warteschlange verarbeitet werden, wird der Nachricht Speicheranbieter die Nachricht **PR_SUBMIT_FLAGS** -Eigenschaft auf SUBMITFLAG_LOCKED. Das SUBMITFLAG_LOCKED-Flag gibt an, dass die MAPI-Warteschlange die Nachricht zur ausschlie�lichen Verwendung gesperrt hat. Der andere Wert f�r **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht muss Vorverarbeitung durch eine oder mehrere Pr�prozessor � Funktionen, die von einem Transportanbieter registriert. 
  

