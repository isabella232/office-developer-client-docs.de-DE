---
title: Erneutes Senden einer nicht zugestellten Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328679"
---
# <a name="resending-an-undelivered-message"></a>Erneutes Senden einer nicht zugestellten Nachricht
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Transportanbieter sendet einen Unzustellbarkeitsbericht (NDR), wenn er eine von Ihnen übermittelte Nachricht nicht erfolgreich übermitteln kann. Es liegt beim Client, ob Benutzer versuchen können, diese nicht zugestellten Nachrichten erneut zu senden. Wenn Sie das erneute Senden von Nachrichten unterstützen, können Sie entweder ein von MAPI bereitgestelltes Formular verwenden oder Ihre eigenen implementieren. Das MAPI-Formular zeigt die Namen der fehlgeschlagenen Empfänger und den Grund für den Übermittlungsfehler an, sofern möglich, und enthält eine Schaltfläche, die es einem Benutzer ermöglicht, die Nachricht erneut zu senden.
  
Wenn eine erneut gesendete Nachricht empfangen wird, sollte Sie genau wie die ursprüngliche Nachricht aussehen. Der Empfänger sollte nicht zwischen einer Nachricht unterscheiden können, die beim ersten Übertragungsversuch oder einem nachfolgenden Versuch zugestellt wurde. Antworten auf diese Nachricht sollten genau so funktionieren, als ob die Nachricht beim ersten Mal erfolgreich gesendet wurde.
  
### <a name="to-resend-an-undelivered-message"></a>So senden Sie eine nicht zugestellte Nachricht erneut
  
1. Rufen Sie [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf, um eine neue Nachricht zu erstellen. 
    
2. Kopieren Sie alle Eigenschaften aus der ursprünglichen Nachricht, ohne die * * PR_MESSAGE_RECIPIENTS * * ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft, und die Eigenschaften **PR_SENDER** und **PR_SENT_REPRESENTING** . Nehmen Sie die folgenden Eigenschaftsänderungen vor: 
    
   - Legen Sie **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) auf die * * PR_ORIG_MESSAGE_CLASS * * ([pidtagoriginalmessageclass (](pidtagoriginalmessageclass-canonical-property.md))-Eigenschaft des Berichts fest.
    
   - Legen Sie das MSGFLAG_RESEND-Flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft fest.
    
   - Legen Sie **PR_ORIGINAL_ENTRYID** ([pidtagoriginalentryid (](pidtagoriginalentryid-canonical-property.md)) auf die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft der ursprünglichen Nachricht fest.
    
   - Legen Sie für jeden Empfänger MAPI_SUBMITTED in der **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))-Eigenschaft fest. 
    
   - Duplizieren Sie jeden fehlerhaften Empfänger. Ändern Sie die **PR_RECIPIENT_TYPE** -Eigenschaft für den doppelten Empfänger in MAPI_P1. Daher gibt es für jeden fehlerhaften Empfänger nun zwei Einträge in der Empfängertabelle: eine mit **PR_RECIPIENT_TYPE** , die auf den ursprünglichen Wert festgelegt ist, und die andere, wobei **PR_RECIPIENT_TYPE** auf MAPI_P1 festgelegt ist. 
    
3. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md) auf, um die Unterhaltungs Verfolgung bei Bedarf einzurichten. 
    
4. Rufen Sie die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode der neuen Nachricht auf, um die Empfängerliste zu aktualisieren. 
    
5. Rufen Sie [IMessage:: SubmitMessage](imessage-submitmessage.md) auf, um die neue Nachricht zu speichern und zu senden. 
    

