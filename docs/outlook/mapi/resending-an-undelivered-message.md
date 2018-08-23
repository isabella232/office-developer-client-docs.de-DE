---
title: Erneutes Senden einer Nachricht nicht zugestellte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdb1ef3cf6db2a1b63b68a105867aa6624b80c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588895"
---
# <a name="resending-an-undelivered-message"></a>Erneutes Senden einer Nachricht nicht zugestellte
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Transportdienstes sendet einen non-Delivery Report (NDR), wenn sie erfolgreich eine Nachricht übermitteln ist nicht möglich, die Sie gesendet haben. Es ist Aufgabe der Client unabhängig davon, ob Benutzer versuchen können diese noch nicht übermittelten Nachrichten erneut zu senden. Wenn Sie unterstützen können Erneutes Senden von Nachrichten, Sie entweder mithilfe eines Formulars bereitgestellt von MAPI oder implementieren Sie eine eigene. Das MAPI-Formular zeigt die Namen der fehlgeschlagene Empfänger und den Grund für das Fehlschlagen der Übermittlung, wenn möglich, und enthält eine Schaltfläche, die bei Auswahl dieser Option ermöglicht einem Benutzer, die Nachricht erneut zu senden.
  
Wenn eine aktuellste Nachricht empfangen wird, sollte es genau wie die ursprüngliche Nachricht aussehen. Der Empfänger sollte zur Unterscheidung zwischen einer Nachricht, die auf der ersten Versuch der Übertragung oder ein nachfolgender Versuch bereitgestellt wurde. Antworten auf diese Nachricht sollte funktionieren, als ob die Nachricht erfolgreich beim ersten gesendet hat.
  
### <a name="to-resend-an-undelivered-message"></a>Eine nicht zugestellte Nachricht erneut zu senden.
  
1. Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) zum Erstellen einer neuen Nachricht ein. 
    
2. Kopieren Sie alle Eigenschaften aus der ursprünglichen Nachricht, ausgenommen die ** PR_MESSAGE_RECIPIENTS **-Eigenschaft ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) und die Eigenschaften **PR_SENDER** und **PR_SENT_REPRESENTING** . Nehmen Sie die folgende Eigenschaft Änderungen vor: 
    
   - Legen Sie mit des Berichts **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ** PR_ORIG_MESSAGE_CLASS **-Eigenschaft ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).
    
   - Legen Sie das MSGFLAG_RESEND-Flag in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) auf die ursprüngliche Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft festgelegt.
    
   - Legen Sie für jeden Empfänger MAPI_SUBMITTED in der Eigenschaft **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Duplizieren Sie jeden fehlerhaften Empfänger. Ändern Sie die **PR_RECIPIENT_TYPE** -Eigenschaft für das duplizierte Empfänger in MAPI_P1. Aus diesem Grund für jeden fehlerhaften Empfänger befinden sich jetzt zwei Einträge in der Tabelle Empfänger: eine Vorlage mit **PR_RECIPIENT_TYPE** auf den ursprünglichen Wert festgelegt und das andere mit **PR_RECIPIENT_TYPE** auf MAPI_P1 festgelegt. 
    
3. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md) So richten Sie bei Bedarf nachverfolgen Unterhaltung ein. 
    
4. Rufen Sie die neue Nachricht [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode, um die Empfängerliste zu aktualisieren. 
    
5. Rufen Sie [IMessage::SubmitMessage](imessage-submitmessage.md) zum Speichern und senden Sie die neue Nachricht. 
    

