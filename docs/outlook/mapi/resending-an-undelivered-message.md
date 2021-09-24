---
title: Erneutes Senden einer nicht zugestellten Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: abe1e54c4205d8b7d09344dfa09c20af5e560b26
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550155"
---
# <a name="resending-an-undelivered-message"></a>Erneutes Senden einer nicht zugestellten Nachricht
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Transportanbieter sendet einen Unzustellbarkeitsbericht (Non-Delivery Report, NDR), wenn er eine von Ihnen übermittelte Nachricht nicht erfolgreich übermitteln kann. Es liegt an dem Client, ob Benutzer versuchen können, diese unzugestellten Nachrichten erneut zu senden. Wenn Sie das erneute Senden von Nachrichten unterstützen, können Sie entweder ein von mapi bereitgestelltes Formular verwenden oder Ein eigenes implementieren. Das MAPI-Formular zeigt die Namen der fehlgeschlagenen Empfänger und nach Möglichkeit den Grund für den Zustellungsfehler an und enthält eine Schaltfläche, die einem Benutzer bei Auswahl ermöglicht, die Nachricht erneut zu senden.
  
Wenn eine erneute Nachricht empfangen wird, sollte sie genau wie die ursprüngliche Nachricht aussehen. Der Empfänger sollte nicht in der Lage sein, zwischen einer Nachricht zu unterscheiden, die beim ersten Übertragungsversuch übermittelt wurde, oder einem nachfolgenden Versuch. Antworten auf diese Nachricht sollten genau so funktionieren, als ob die Nachricht beim ersten Mal erfolgreich gesendet worden wäre.
  
### <a name="to-resend-an-undelivered-message"></a>So senden Sie eine nicht zugestellte Nachricht erneut
  
1. Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf, um eine neue Nachricht zu erstellen. 
    
2. Kopieren Sie alle Eigenschaften aus der ursprünglichen Nachricht, mit Ausnahme der ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft und der **eigenschaften PR_SENDER** und **PR_SENT_REPRESENTING.** Nehmen Sie die folgenden Eigenschaftsänderungen vor: 
    
   - Legen Sie **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) auf die **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) -Eigenschaft des Berichts fest.
    
   - Legen Sie das flag MSGFLAG_RESEND in der **Eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) fest.
    
   - Legen Sie **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) auf die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) der ursprünglichen Nachricht fest.
    
   - Legen Sie für jeden Empfänger MAPI_SUBMITTED in der **Eigenschaft PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) fest. 
    
   - Duplizieren Sie jeden fehlgeschlagenen Empfänger. Ändern Sie die **eigenschaft PR_RECIPIENT_TYPE** für den duplizierten Empfänger in MAPI_P1. Daher gibt es für jeden fehlgeschlagenen Empfänger jetzt zwei Einträge in der Empfängertabelle: eine mit **PR_RECIPIENT_TYPE** auf ihren ursprünglichen Wert und die andere mit **PR_RECIPIENT_TYPE** auf MAPI_P1 festgelegt. 
    
3. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md) auf, um die Unterhaltungsverfolgung bei Bedarf einzurichten. 
    
4. Rufen Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) der neuen Nachricht auf, um die Empfängerliste zu aktualisieren. 
    
5. Rufen Sie [IMessage::SubmitMessage](imessage-submitmessage.md) auf, um die neue Nachricht zu speichern und zu senden. 
    

