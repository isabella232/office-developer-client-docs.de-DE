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
ms.openlocfilehash: de29707c7a257ea0e7ad658622d2a3054487f8b5
ms.sourcegitcommit: adcf409d56b6cb25be6117f09794defa41ad6c0f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "37495306"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Senden von Nachrichten: Nachrichten Store Anbieteraufgaben

**Gilt für**: Outlook 2013 | Outlook 2016 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
Der Nachricht Informationsdienst bestimmt, ob er die MAPI-Warteschlange umfassen. Wenn die Nachricht Informationsdienst nicht eng verkn�pft ist, die Nachricht muss Vorverarbeitung, oder den eng gekoppelten Speicher und Transport k�nnen nicht bearbeitet werden alle Empf�nger, die MAPI-Warteschlange beteiligt sein muss. 
  
Das folgende Verfahren beschreibt die von einem Nachrichtenanbieter zum Senden einer Nachricht erforderlichen Aufgaben. 
  
**In IMessage::SubmitMessage, der Nachrichtenspeicheranbieter**:
  
1. Ruft [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) auf, wenn in der Nachricht das **flag MSGFLAG_RESEND** in der eigenschaft PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) festgelegt ist, und gibt Fehler an den Client zurück. **PrepareSubmit** überprüft **die PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft jedes Empfängers in der Empfängerliste der Nachricht.
    
   - Wenn das MAPI_SUBMITTED festgelegt ist, das angibt, dass der Empfänger die ursprüngliche Nachricht nicht empfangen hat, wird das Flag von **PrepareSubmit** entfernt und die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) auf TRUE festgelegt. 
    
   - Wenn das MAPI_SUBMITTED-Flag nicht festgelegt ist und angibt, dass der Empfänger die ursprüngliche Nachricht empfangen hat, ändert **PrepareSubmit** die **PR_RECIPIENT_TYPE-Eigenschaft** in MAPI_P1 und legt die **PR_RESPONSIBILITY-Eigenschaft** auf TRUE fest und gibt alle Fehler zurück, die **von PrepareSubmit** an den Client generiert werden. 
    
2. Das Flag MSGFLAG_SUBMIT festgelegt in der Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft. 
    
3. Stellt sicher, dass eine Spalte f�r **PR_RESPONSIBILITY** in der Tabelle Empf�nger und wird auf false fest, um anzugeben, dass kein Transport noch angenommenen Verantwortung f�r die �bermittlung der Nachricht wurde. 
    
4. Legt Das Datum und die Uhrzeit der Ursprünge in der **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) -Eigenschaft fest.
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
   - Entfernen von Duplikaten.
   - Überprüfen Sie, ob eine erforderliche Vorverarbeitung erforderlich ist, und legen Sie das flag NEEDS_PREPROCESSING und die **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) -Eigenschaft, eine Eigenschaft, die für MAPI reserviert ist. 
   - Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
   - Legt die Nachricht in der ausgehenden Warteschlange mit dem SUBMITFLAG_PREPROCESS in der **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) -Eigenschaft.
   - Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
   - Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. 
   - Die MAPI-Warteschlange f�hrt die folgenden Aufgaben:
     - Sperrt die Nachricht durch Aufrufen von IMsgStore::SetLockState. 
     - Führt die benötigte Vorverarbeitung durch Aufrufen aller Vorverarbeitungsfunktionen in der Reihenfolge der Registrierung aus. Transportanbieter rufen IMAPISupport::RegisterPreprocessor auf, um Vorverarbeitungsfunktionen zu registrieren. 
     - Ruft IMessage::SubmitMessage für die geöffnete Nachricht auf, um dem Nachrichtenspeicher anzugeben, dass die Vorverarbeitung abgeschlossen ist.

<br/>

Die folgenden beiden Schritte treten im Clientprozess auf, wenn keine Vorverarbeitung erfolgt ist, und wenn der MAPI-Spooler **SubmitMessage** aufruft, wenn eine Vorverarbeitung erfolgt ist. 

**Der Nachrichtenspeicheranbieter**:

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind:
     - Ruft IMAPISupport::CompleteMsg auf, wenn die Nachricht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abgeschlossen hat, was empfohlen wird, damit Messaging hooks aufgerufen werden können. Der Nachrichtenfluss wird wie im folgenden Verfahren beschrieben mit dem MAPI-Spooler fortgesetzt.  
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter nicht möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abgeschlossen hat:
       - Kopiert die Nachricht in den Ordner, der durch die Eintrags-ID in der PR_SENTMAIL_ENTRYID -Eigenschaft (PidTagSentMailEntryId) identifiziert wird, sofern festgelegt.
       - Löscht die Nachricht, wenn die PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit)-Eigenschaft auf TRUE festgelegt wurde.
       - Entsperrt die Nachricht, wenn sie gesperrt ist.
       - Gibt an den Client zurück. Der Nachrichtenfluss ist abgeschlossen. 
   
2. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
   - Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
   - Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
   - Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
Wenn eine Nachricht von den MAPI-Warteschlange verarbeitet werden, wird der Nachricht Speicheranbieter die Nachricht **PR_SUBMIT_FLAGS** -Eigenschaft auf SUBMITFLAG_LOCKED. Das SUBMITFLAG_LOCKED-Flag gibt an, dass die MAPI-Warteschlange die Nachricht zur ausschlie�lichen Verwendung gesperrt hat. Der andere Wert f�r **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht muss Vorverarbeitung durch eine oder mehrere Pr�prozessor � Funktionen, die von einem Transportanbieter registriert. 
  

