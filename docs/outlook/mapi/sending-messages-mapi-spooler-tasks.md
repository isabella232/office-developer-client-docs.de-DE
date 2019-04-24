---
title: Senden von Nachrichten MAPI-Warteschlange Aufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339676"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Senden von Nachrichten: MAPI-Spooler-Aufgaben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Warteschlange ist bei der �bertragung beteiligt, wenn der Nachrichtenspeicher mit einem Transportanbieter nicht eng verkn�pft ist, wenn den eng gekoppelten Speicher und Transport einen Empf�nger nicht verarbeiten k�nnen und die Nachricht Vorverarbeitung erforderlich ist.
  
 **Nach der erforderlichen Vorverarbeitung f�hrt die MAPI-Warteschlange die folgenden Schritte aus:**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Der Transportanbieter sendet die Nachricht an alle Empfänger, deren **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft auf false festgelegt ist. 
    
3. Ruft die entsprechende Funktion ([RemovePreprocessInfo](removepreprocessinfo.md)) zum Bereinigen zusätzlicher Informationen auf, die der Nachricht zur Verwendung während der Vorverarbeitung hinzugefügt wurden, wenn die **PR_PREPROCESS** ([pidtagpreprocess (](pidtagpreprocess-canonical-property.md))-Eigenschaft festgelegt wurde. This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - Hebt die Sperre der Nachricht.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. Anschließend wird die Nachricht in den Ordner kopiert, der durch die Eintrags-ID in der **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft identifiziert wird, wenn Sie nicht durch die Verarbeitung der gesendeten Nachrichten eines Messaging-Hooks ersetzt wird. Schließlich wird die Nachricht gelöscht, wenn die **PR_DELETE_AFTER_SUBMIT** ([pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf true festgelegt wurde. 
    

