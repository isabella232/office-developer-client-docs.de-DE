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
ms.openlocfilehash: 8bfa5709dede4a9501d261e0f495acbc0894b470
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795496"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Senden von Nachrichten: Nachrichtenspeicher Anbieter Aufgaben

**Betrifft**: Outlook 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
Der Nachricht Informationsdienst bestimmt, ob er die MAPI-Warteschlange umfassen. Wenn die Nachricht Informationsdienst nicht eng verkn�pft ist, die Nachricht muss Vorverarbeitung, oder den eng gekoppelten Speicher und Transport k�nnen nicht bearbeitet werden alle Empf�nger, die MAPI-Warteschlange beteiligt sein muss. 
  
Das folgende Verfahren beschreibt die von einem Nachrichtenanbieter zum Senden einer Nachricht erforderlichen Aufgaben. 
  
**In der IMessage::SubmitMessage die Nachricht Speicheranbieter**:
  
1. [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) aufgerufen, wenn die Nachricht das MSGFLAG_RESEND-Flag, das in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft festgelegt wurde und Fehlermeldungen an den Client zurück. **PrepareSubmit** überprüft die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft der einzelnen Empfänger in der Liste der Empfänger der Nachricht.
    
   - Wenn das Flag MAPI_SUBMITTED festgelegt ist, gibt an, dass der Empfänger die ursprüngliche Nachricht nicht erhalten haben, **PrepareSubmit** löscht das Flag und die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft auf TRUE festgelegt. 
    
   - Wenn das Flag MAPI_SUBMITTED nicht festgelegt ist, der angibt, dass der Empf�nger der urspr�nglichen Nachricht erhalten hat, �ndert die Eigenschaft **PR_RECIPIENT_TYPE** in MAPI_P1 **PrepareSubmit** und die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE festgelegt und etwaige Fehler generierte **PrepareSubmit** an den Client zur�ckgegeben. 
    
2. Das Flag MSGFLAG_SUBMIT festgelegt in der Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft. 
    
3. Stellt sicher, dass eine Spalte f�r **PR_RESPONSIBILITY** in der Tabelle Empf�nger und wird auf false fest, um anzugeben, dass kein Transport noch angenommenen Verantwortung f�r die �bermittlung der Nachricht wurde. 
    
4. Legt das Datum und die Uhrzeit der Aufnahme in der Eigenschaft **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
   - Entfernen von Duplikaten.
   - Erforderliche vorverarbeitung suchen Sie, und wenn der vorverarbeitung erforderlich ist, legen Sie das Kennzeichen NEEDS_PREPROCESSING und der **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md))-Eigenschaft, einer Eigenschaft, die für die MAPI reserviert. 
   - Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
   - Versetzt die Nachricht in der ausgehenden Warteschlange mit dem SUBMITFLAG_PREPROCESS Bit in der Eigenschaft **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) festgelegt.
   - Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
   - Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. 
   - Die MAPI-Warteschlange f�hrt die folgenden Aufgaben:
     - Sperrt die Nachricht durch Aufrufen von IMsgStore::SetLockState. 
     - Führt die erforderlichen vorverarbeitung durch Aufrufen von alle vorverarbeitenden Funktionen in der Reihenfolge der Registrierung. Transportanbieter aufrufen IMAPISupport::RegisterPreprocessor vorverarbeitenden Funktionen registrieren. 
     - Ruft IMessage::SubmitMessage auf der geöffneten Nachricht der Nachrichtenspeicher an, dass der vorverarbeitung abgeschlossen ist.

<br/>

Die folgenden beiden Schritte auftreten im Clientprozess, wenn es wurde keine vorverarbeitung und wenn die MAPI-Warteschlange **SubmitMessage** aufruft, wenn es vorverarbeitung wurde. 

**Die Nachricht Speicheranbieter**:

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind:
     - IMAPISupport::CompleteMsg aufgerufen, wenn die Nachricht vorverarbeitet wurde oder die Nachrichtenspeicher Anbieter möchte der MAPI-Warteschlange für die Durchführung Verarbeitung von Nachrichten, wird empfohlen, damit messaging, dass Haken aufgerufen werden können. Nachrichtenfluss wird die MAPI-Warteschlange fort, wie im folgenden Verfahren beschrieben.  
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachricht Speicheranbieter nicht die MAPI-Warteschlange zum Abschließen der Verarbeitung von Nachrichten möchte:
       - Kopien legen Sie die Nachricht in den Ordner, der durch die Eintrags-ID in der Eigenschaft PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), sofern bezeichnet wird.
       - Löscht die Nachricht, wenn die PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit)-Eigenschaft auf TRUE festgelegt wurde.
       - Entsperrt die Nachricht, wenn sie gesperrt ist.
       - Gibt an den Client. Nachrichtenfluss ist abgeschlossen. 
   
2. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
   - Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
   - Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
   - Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
Wenn eine Nachricht von den MAPI-Warteschlange verarbeitet werden, wird der Nachricht Speicheranbieter die Nachricht **PR_SUBMIT_FLAGS** -Eigenschaft auf SUBMITFLAG_LOCKED. Das SUBMITFLAG_LOCKED-Flag gibt an, dass die MAPI-Warteschlange die Nachricht zur ausschlie�lichen Verwendung gesperrt hat. Der andere Wert f�r **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht muss Vorverarbeitung durch eine oder mehrere Pr�prozessor � Funktionen, die von einem Transportanbieter registriert. 
  

