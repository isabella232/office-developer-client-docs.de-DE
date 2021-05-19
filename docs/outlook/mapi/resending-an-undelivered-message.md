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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432667"
---
# <a name="resending-an-undelivered-message"></a>Erneutes Senden einer nicht zugestellten Nachricht
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Transportanbieter sendet einen Unzustellbarkeitsbericht (Non-Delivery Report, Unzustellbarkeitsbericht), wenn eine übermittelte Nachricht nicht erfolgreich übermittelt werden kann. Es liegt beim Client, ob Benutzer versuchen können, diese nicht zugestellten Nachrichten erneut zu senden. Wenn Sie das erneute Senden von Nachrichten unterstützen, können Sie entweder ein von MAPI bereitgestelltes Formular verwenden oder Ein eigenes Formular implementieren. Das MAPI-Formular zeigt nach Möglichkeit die Namen der fehlgeschlagenen Empfänger und den Grund für den Zustellungsfehler an und enthält eine Schaltfläche, mit der ein Benutzer die Nachricht bei Auswahl erneut senden kann.
  
Wenn eine Ressentimentsnachricht empfangen wird, sollte sie genau wie die ursprüngliche Nachricht aussehen. Der Empfänger sollte nicht zwischen einer Nachricht unterscheiden können, die beim ersten Übertragungsversuch zugestellt wurde, oder einem nachfolgenden Versuch. Antworten auf diese Nachricht sollten genau so funktionieren, als wäre die Nachricht beim ersten Mal erfolgreich gesendet worden.
  
### <a name="to-resend-an-undelivered-message"></a>So senden Sie eine nicht zugestellte Nachricht erneut
  
1. Rufen [Sie IMAPIFolder::CreateMessage auf,](imapifolder-createmessage.md) um eine neue Nachricht zu erstellen. 
    
2. Kopieren Sie alle Eigenschaften aus der ursprünglichen Nachricht, ausgenommen die ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft und die eigenschaften **PR_SENDER** **und PR_SENT_REPRESENTING.** Nehmen Sie die folgenden Eigenschaftsänderungen vor: 
    
   - Legen **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) auf die **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) -Eigenschaft des Berichts.
    
   - Legen Sie das MSGFLAG_RESEND in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft.
    
   - Legen **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) auf die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) der ursprünglichen Nachricht.
    
   - Legen Sie für jeden Empfänger MAPI_SUBMITTED in der **PR_RECIPIENT_TYPE** ([PidTagRecipientType ) -Eigenschaft.](pidtagrecipienttype-canonical-property.md) 
    
   - Duplizieren Sie jeden fehlgeschlagenen Empfänger. Ändern Sie **PR_RECIPIENT_TYPE** Eigenschaft für den doppelten Empfänger in MAPI_P1. Daher sind für jeden fehlgeschlagenen Empfänger nun zwei Einträge in der Empfängertabelle enthalten: einer  mit **PR_RECIPIENT_TYPE** auf den ursprünglichen Wert und der andere mit PR_RECIPIENT_TYPE auf MAPI_P1. 
    
3. Rufen [Sie ScCreateConversationIndex auf,](sccreateconversationindex.md) um die Unterhaltungsverfolgung bei Bedarf zu einrichten. 
    
4. Rufen Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) der neuen Nachricht auf, um die Empfängerliste zu aktualisieren. 
    
5. Rufen [Sie IMessage::SubmitMessage auf,](imessage-submitmessage.md) um die neue Nachricht zu speichern und zu senden. 
    

