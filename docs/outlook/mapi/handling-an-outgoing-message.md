---
title: Behandeln von ausgehenden Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 18fe188f7906b3a2fdd8192a353cc8ba39ad0247
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556693"
---
# <a name="handling-an-outgoing-message"></a>Behandeln von ausgehenden Nachrichten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine ausgehende Nachricht ist eine Nachricht, die an einen oder mehrere Empfänger in einem oder mehreren Messagingsystemen gesendet oder in einem Ordner in einem Nachrichtenspeicher bereitgestellt werden kann.
  
## <a name="create-and-send-an-outgoing-message"></a>Erstellen und Senden einer ausgehenden Nachricht
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen einer Nachricht Store](opening-a-message-store.md) und Öffnen der [Standardnachricht Store](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner "Postausgang". Weitere Informationen finden Sie unter [Öffnen einer Nachricht Store Ordners.](opening-a-message-store-folder.md)
    
3. Rufen Sie die **IMAPIFolder::CreateMessage-Methode** des Postausgangsordners auf, um die neue Nachricht zu erstellen. Weitere Informationen finden Sie unter [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Erstellen Sie eine Empfängerliste mit einem oder mehreren aufgelösten Empfängern. Weitere Informationen finden Sie unter [Erstellen einer Empfängerliste.](creating-a-recipient-list.md)
    
5. Fügen Sie optional einen Betreff hinzu. Weitere Informationen finden Sie unter [Erstellen eines Nachrichtenbetreffs.](creating-a-message-subject.md)
    
6. Fügen Sie den Nachrichtentext hinzu. Weitere Informationen finden Sie unter [Erstellen von Nachrichtentext](creating-message-text.md).
    
7. Wenn der Nachrichtentext formatiert ist, fügen Sie Renderinginformationen hinzu. Weitere Informationen finden Sie unter [Hinzufügen von Renderinginformationen zu formatiertem Text.](adding-rendering-information-to-formatted-text.md)
    
8. Fügen Sie optional eine oder mehrere Anlagen hinzu. Weitere Informationen finden Sie unter [Erstellen einer Nachrichtenanlage.](creating-a-message-attachment.md)
    
9. Legen Sie andere Nachrichteneigenschaften nach Bedarf fest, und speichern und senden Sie die Nachricht, indem **Sie IMessage::SubmitMessage** aufrufen. Weitere Informationen finden Sie unter [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Löschen Sie die gesendete Nachricht, wenn die **\_ PR-DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) -Eigenschaft auf TRUE festgelegt ist, oder verschieben Sie sie in den Von der **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) -Eigenschaft identifizierten Ordner. Weitere Informationen finden Sie unter [Verarbeiten einer gesendeten Nachricht.](processing-a-sent-message.md)
    
Wenn Sie die Nachricht intermittant speichern möchten, bevor Sie sie senden, rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht auf. Weitere Informationen finden Sie unter ["Speichern einer Nachricht"](saving-a-message.md) oder ["Senden einer Nachricht".](sending-a-message.md) 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen einer Empfängerliste:](creating-a-recipient-list.md)Beschreibt, wie eine Empfängerliste erstellt wird.
    
- [Erstellen eines Nachrichtenbetreffs:](creating-a-message-subject.md)Beschreibt, wie ein optionaler Betreff für eine Nachricht erstellt wird.
    
- [Erstellen von Nachrichtentext:](creating-message-text.md)Beschreibt, wie Nachrichtentext erstellt wird.
    
- [Hinzufügen von Renderinginformationen zu formatiertem Text:](adding-rendering-information-to-formatted-text.md)Beschreibt, wo in formatiertem Text eine Anlage gerendert werden soll.
    
- [Erstellen einer Nachrichtenanlage:](creating-a-message-attachment.md)Beschreibt, wie Anlagen erstellt werden.
    
- [Speichern einer Nachricht:](saving-a-message.md)Beschreibt, wie Clients Nachrichten speichern.
    
- [Senden einer Nachricht:](sending-a-message.md)Beschreibt, wie eine Nachricht gesendet wird.
    
- [Verarbeiten einer gesendeten Nachricht:](processing-a-sent-message.md)Beschreibt, wie gesendete Nachrichten verarbeitet werden können.
    

