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
ms.openlocfilehash: 3f3330c132abdf35d0e4f67775c03f7d2e9fcc76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563989"
---
# <a name="handling-an-outgoing-message"></a>Behandeln von ausgehenden Nachrichten

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine ausgehende Nachricht ist eine Nachricht, die an einen oder mehrere Empfänger gesendet werden kann, über eine oder mehrere messaging-Systemen oder in einen Ordner in einem Nachrichtenspeicher veröffentlicht werden.
  
## <a name="create-and-send-an-outgoing-message"></a>Erstellen Sie und senden Sie eine ausgehende Nachricht
  
1. Öffnen Sie die Standard-Informationsspeicher. Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md) und [Öffnen Sie die Standard-Informationsspeicher](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner Postausgang. Weitere Informationen finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).
    
3. Aufrufen der Ordner Postausgang **IMAPIFolder::CreateMessage** -Methode, um die neue Nachricht zu erstellen. Weitere Informationen finden Sie unter [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Erstellen Sie eine Empfängerliste mit einen oder mehrere aufgelösten Empfänger. Weitere Informationen finden Sie unter [Erstellen einer Liste der Empfänger](creating-a-recipient-list.md).
    
5. Fügen Sie optional einen Betreff hinzu. Weitere Informationen finden Sie unter [Erstellen einer Betreff der Nachricht](creating-a-message-subject.md).
    
6. Fügen Sie den Nachrichtentext hinzu. Weitere Informationen finden Sie unter [Erstellen des Nachrichtentexts](creating-message-text.md).
    
7. Wenn der Nachrichtentext formatiert ist, fügen Sie Renderinginformationen hinzu. Weitere Informationen finden Sie unter [Hinzufügen von Rendern von Informationen in Text formatiert](adding-rendering-information-to-formatted-text.md).
    
8. Fügen Sie optional eine oder mehrere Anlagen hinzu. Weitere Informationen finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).
    
9. Legen Sie nach Bedarf weitere Nachrichteneigenschaften und speichern und Senden der Nachricht durch Aufrufen von **IMessage::SubmitMessage**. Weitere Informationen finden Sie unter [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Die gesendete Nachricht löschen, wenn die **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf TRUE oder verschieben in den Ordner identifiziert durch die **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))-Eigenschaft festgelegt ist. Weitere Informationen finden Sie in der [Verarbeitung einer Nachricht gesendet](processing-a-sent-message.md).
    
Wenn Sie möchten abwechselnd speichern Sie die Nachricht vor dem senden, rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode. Weitere Informationen finden Sie unter, [Speichern einer Nachricht](saving-a-message.md) oder [Senden einer Nachricht](sending-a-message.md). 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen einer Liste der Empfänger](creating-a-recipient-list.md): Beschreibt das Erstellen einer Empfängerliste.
    
- [Erstellen Sie einen Betreff der Nachricht](creating-a-message-subject.md): Beschreibt, wie Sie einen optionalen Betreff für eine Nachricht zu erstellen.
    
- [Erstellen des Nachrichtentexts](creating-message-text.md): Erstellen des Nachrichtentexts beschrieben.
    
- [Rendern von Informationen zu formatierten Text hinzufügen](adding-rendering-information-to-formatted-text.md): Beschreibt, in dem in formatierten Text eine Anlage gerendert werden.
    
- [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md): Beschreibt, wie Anlagen erstellen.
    
- [Speichern einer Nachricht](saving-a-message.md): Beschreibt, wie Clients Nachrichten speichern.
    
- [Senden einer Nachricht](sending-a-message.md): Beschreibt, wie Sie eine Nachricht senden.
    
- [Verarbeiten einer Nachricht gesendet](processing-a-sent-message.md): Beschreibt, wie Sie gesendete Nachrichten verarbeitet werden können.
    

