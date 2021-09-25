---
title: Senden von Nachrichten Nachrichtenspeicher Anbieter Aufgaben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3597a74ef789ea591a82a569069679a3dd8e449e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624244"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Senden von Nachrichten: Nachrichten Store Anbieteraufgaben

**Gilt für**: Outlook 2013 | Outlook 2016 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
Der Nachricht Informationsdienst bestimmt, ob er die MAPI-Warteschlange umfassen. Wenn die Nachricht Informationsdienst nicht eng verkn�pft ist, die Nachricht muss Vorverarbeitung, oder den eng gekoppelten Speicher und Transport k�nnen nicht bearbeitet werden alle Empf�nger, die MAPI-Warteschlange beteiligt sein muss. 
  
Das folgende Verfahren beschreibt die von einem Nachrichtenanbieter zum Senden einer Nachricht erforderlichen Aufgaben. 
  
**In IMessage::SubmitMessage der Nachrichtenspeicheranbieter:**
  
1. Calls [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) if the message has the MSGFLAG_RESEND flag set in its **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property and returns any errors to the client. **PrepareSubmit** überprüft die **eigenschaft PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) jedes Empfängers in der Empfängerliste der Nachricht.
    
   - Wenn das MAPI_SUBMITTED-Flag festgelegt ist, das angibt, dass der Empfänger die ursprüngliche Nachricht nicht empfangen hat, löscht **PrepareSubmit** das Flag und legt die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) auf TRUE fest. 
    
   - Wenn das flag MAPI_SUBMITTED nicht festgelegt ist und angibt, dass der Empfänger die ursprüngliche Nachricht empfangen hat, ändert **PrepareSubmit** die **PR_RECIPIENT_TYPE-Eigenschaft** in MAPI_P1 und legt die **PR_RESPONSIBILITY-Eigenschaft** auf TRUE fest und gibt alle von **PrepareSubmit** generierten Fehler an den Client zurück. 
    
2. Das Flag MSGFLAG_SUBMIT festgelegt in der Nachricht **PR_MESSAGE_FLAGS** -Eigenschaft. 
    
3. Stellt sicher, dass eine Spalte f�r **PR_RESPONSIBILITY** in der Tabelle Empf�nger und wird auf false fest, um anzugeben, dass kein Transport noch angenommenen Verantwortung f�r die �bermittlung der Nachricht wurde. 
    
4. Legt das Datum und die Uhrzeit des Ursprungs in der **eigenschaft PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) fest.
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - Erweitern Sie alle pers�nlichen Verteilerlisten und benutzerdefinierte Empf�nger, und Ersetzen Sie alle ge�nderten Anzeigenamen durch ihren Originalnamen.
   - Entfernen von Duplikaten.
   - Überprüfen Sie, ob eine erforderliche Vorverarbeitung erforderlich ist. Wenn die Vorverarbeitung erforderlich ist, legen Sie das NEEDS_PREPROCESSING-Flag und die **eigenschaft PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) fest, eine eigenschaft, die für MAPI reserviert ist. 
   - Legen Sie das Flag NEEDS_SPOOLER, wenn der Nachrichtenspeicher eng mit einer Transport verkn�pft ist und nicht behandelt alle Empf�nger werden kann. 
    
6. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenkennzeichnung NEEDS_PREPROCESSING festgelegt ist:
    
   - Versetzt die Nachricht in die ausgehende Warteschlange, wobei das SUBMITFLAG_PREPROCESS Bit in der **Eigenschaft PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) festgelegt ist.
   - Benachrichtigt die MAPI-Warteschlange, die die Warteschlange ge�ndert wurde.
   - Gibt die Steuerung an den Client, und Nachrichtenfluss wird in die Warteschlange MAPI fortgesetzt. 
   - Die MAPI-Warteschlange f�hrt die folgenden Aufgaben:
     - Sperrt die Nachricht, indem IMsgStore::SetLockState aufgerufen wird. 
     - Führt die erforderliche Vorverarbeitung durch, indem alle Vorverarbeitungsfunktionen in der Reihenfolge der Registrierung aufgerufen werden. Transportanbieter rufen IMAPISupport::RegisterPreprocessor auf, um Vorverarbeitungsfunktionen zu registrieren. 
     - Ruft IMessage::SubmitMessage in der geöffneten Nachricht auf, um dem Nachrichtenspeicher anzugeben, dass die Vorverarbeitung abgeschlossen ist.

<br/>

Die folgenden beiden Schritte werden im Clientprozess ausgeführt, wenn keine Vorverarbeitung erfolgt ist, und wenn der MAPI-Spooler **SubmitMessage** aufruft, wenn eine Vorverarbeitung erfolgt ist. 

**Der Nachrichtenspeicheranbieter:**

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Verarbeitet Empf�nger, die es verarbeiten kann.
   - Legt die **PR_RESPONSIBILITY** -Eigenschaft auf TRUE fest, f�r alle Empf�nger, die sie behandelt. 
   - F�hrt die folgenden Aufgaben aus, wenn alle Empf�nger zu diesem eng gekoppelten Store und Transport bekannt sind:
     - Ruft IMAPISupport::CompleteMsg auf, wenn die Nachricht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abschließt, was empfohlen wird, damit Messaging-Hooks aufgerufen werden können. Der Nachrichtenfluss wird mit dem MAPI-Spooler fortgesetzt, wie im folgenden Verfahren beschrieben.  
     - Führt die folgenden Aufgaben aus, wenn die Nachricht nicht vorverarbeitet wurde oder der Nachrichtenspeicheranbieter nicht möchte, dass der MAPI-Spooler die Nachrichtenverarbeitung abschließt:
       - Kopiert die Nachricht in den Ordner, der durch den Eintragsbezeichner in der Eigenschaft PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId) identifiziert wird, sofern festgelegt.
       - Löscht die Nachricht, wenn die eigenschaft PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) auf TRUE festgelegt wurde.
       - Entsperrt die Nachricht, wenn sie gesperrt ist.
       - Gibt an den Client zurück. Der Nachrichtenfluss ist abgeschlossen. 
   
2. F�hrt die folgenden Aufgaben aus, wenn der Nachrichtenspeicher nicht eng um einen Transport verkn�pft, nicht alle Empf�nger mit dem Nachrichtenspeicher bezeichnet wurden oder das Flag NEEDS_SPOOLER festgelegt ist:
    
   - Versetzt die Nachricht in der ausgehenden Warteschlange ohne das SUBMITFLAG_PREPROCESS Bit in der **PR_SUBMIT_FLAGS** -Eigenschaft festlegen. 
   - Benachrichtigt die MAPI-Warteschlange, die die ausgehende Warteschlange ge�ndert wurde, indem eine Benachrichtigung �ber eine Tabelle zu generieren. 
   - Gibt f�r den Client und Nachrichtenfluss weiterhin mit einem Satz von Aufgaben, die MAPI-Warteschlange.
    
Wenn eine Nachricht von den MAPI-Warteschlange verarbeitet werden, wird der Nachricht Speicheranbieter die Nachricht **PR_SUBMIT_FLAGS** -Eigenschaft auf SUBMITFLAG_LOCKED. Das SUBMITFLAG_LOCKED-Flag gibt an, dass die MAPI-Warteschlange die Nachricht zur ausschlie�lichen Verwendung gesperrt hat. Der andere Wert f�r **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, wird festgelegt, wenn die Nachricht muss Vorverarbeitung durch eine oder mehrere Pr�prozessor � Funktionen, die von einem Transportanbieter registriert. 
  

