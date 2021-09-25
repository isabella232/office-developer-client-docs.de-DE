---
title: Senden von Nachrichten MAPI-Warteschlange Aufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1380d7528f0902ec34ec0af9b7a31a4602d1b071
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578648"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Senden von Nachrichten: MAPI-Spooleraufgaben

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Warteschlange ist bei der �bertragung beteiligt, wenn der Nachrichtenspeicher mit einem Transportanbieter nicht eng verkn�pft ist, wenn den eng gekoppelten Speicher und Transport einen Empf�nger nicht verarbeiten k�nnen und die Nachricht Vorverarbeitung erforderlich ist.
  
 **Nach der erforderlichen Vorverarbeitung f�hrt die MAPI-Warteschlange die folgenden Schritte aus:**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Übergibt der Transportanbieter die Nachricht an alle Empfänger, deren **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) -Eigenschaft auf FALSE festgelegt ist. 
    
3. Ruft die entsprechende Funktion ([RemovePreprocessInfo](removepreprocessinfo.md)) auf, um alle zusätzlichen Informationen zu bereinigen, die der Nachricht zur Verwendung während der Vorverarbeitung hinzugefügt wurden, wenn die **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) -Eigenschaft festgelegt wurde. This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - Hebt die Sperre der Nachricht.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. Anschließend wird die Nachricht in den Ordner kopiert, der durch den Eintragsbezeichner in der **Eigenschaft PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) identifiziert wird, wenn sie nicht durch die gesendete Nachrichtenverarbeitung eines Messaging-Hook-Anbieters abgelöst wird. Schließlich wird die Nachricht gelöscht, wenn die **eigenschaft PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) auf TRUE festgelegt wurde. 
    

