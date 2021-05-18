---
title: Behandeln von ausgehenden Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407627"
---
# <a name="handling-an-outgoing-message"></a>Behandeln von ausgehenden Nachrichten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine ausgehende Nachricht ist eine Nachricht, die über ein oder mehrere Messagingsysteme an einen oder mehrere Empfänger gesendet oder in einem Ordner in einem Nachrichtenspeicher bereitgestellt werden kann.
  
## <a name="create-and-send-an-outgoing-message"></a>Erstellen und Senden einer ausgehenden Nachricht
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Opening a Message Store](opening-a-message-store.md) and Opening the Default Message [Store](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner "Outbox". Weitere Informationen finden Sie unter [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
3. Rufen Sie die **IMAPIFolder::CreateMessage-Methode des Posteingangsordners** auf, um die neue Nachricht zu erstellen. Weitere Informationen finden Sie unter [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Erstellen Sie eine Empfängerliste mit einem oder mehreren aufgelösten Empfängern. Weitere Informationen finden Sie unter [Creating a Recipient List](creating-a-recipient-list.md).
    
5. Fügen Sie optional einen Betreff hinzu. Weitere Informationen finden Sie unter [Creating a Message Subject](creating-a-message-subject.md).
    
6. Fügen Sie den Nachrichtentext hinzu. Weitere Informationen finden Sie unter [Creating Message Text](creating-message-text.md).
    
7. Wenn der Nachrichtentext formatiert ist, fügen Sie Renderinginformationen hinzu. Weitere Informationen finden Sie unter [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).
    
8. Fügen Sie optional eine oder mehrere Anlagen hinzu. Weitere Informationen finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).
    
9. Legen Sie andere Nachrichteneigenschaften wie gewünscht, und speichern Und senden Sie die Nachricht, indem Sie **IMessage::SubmitMessage aufrufen.** Weitere Informationen finden Sie unter [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Löschen Sie die gesendete **\_ Nachricht, wenn** die PR DELETE_AFTER_SUBMIT ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) -Eigenschaft auf TRUE festgelegt ist, oder verschieben Sie sie in den Ordner, der durch die **eigenschaft PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) identifiziert wird. Weitere Informationen finden Sie unter [Processing a Sent Message](processing-a-sent-message.md).
    
Wenn Sie die Nachricht vor dem Senden intermittant speichern möchten, rufen Sie die [IMAPIProp::SaveChanges-Methode der Nachricht](imapiprop-savechanges.md) auf. Weitere Informationen finden Sie unter [Speichern einer Nachricht oder](saving-a-message.md) Senden einer [Nachricht](sending-a-message.md). 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen einer Empfängerliste](creating-a-recipient-list.md): Beschreibt das Erstellen einer Empfängerliste.
    
- [Erstellen eines Nachrichtensubjekts:](creating-a-message-subject.md)Beschreibt das Erstellen eines optionalen Betreffs für eine Nachricht.
    
- [Erstellen von Nachrichtentext](creating-message-text.md): Beschreibt das Erstellen von Nachrichtentext.
    
- [Hinzufügen von Renderinginformationen zum formatierten Text](adding-rendering-information-to-formatted-text.md): Beschreibt, wo im formatierten Text eine Anlage gerendert werden soll.
    
- [Erstellen einer Nachrichtenanlage:](creating-a-message-attachment.md)Beschreibt das Erstellen von Anlagen.
    
- [Speichern einer Nachricht](saving-a-message.md): Beschreibt, wie Clients Nachrichten speichern.
    
- [Senden einer Nachricht](sending-a-message.md): Beschreibt das Senden einer Nachricht.
    
- [Verarbeiten einer gesendeten Nachricht:](processing-a-sent-message.md)Beschreibt, wie gesendete Nachrichten verarbeitet werden können.
    

