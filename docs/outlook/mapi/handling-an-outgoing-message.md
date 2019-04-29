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
  
Eine ausgehende Nachricht ist eine Nachricht, die an einen oder mehrere Empfänger über ein oder mehrere Messagingsysteme gesendet oder in einem Ordner in einem Nachrichtenspeicher bereitgestellt werden kann.
  
## <a name="create-and-send-an-outgoing-message"></a>Erstellen und Senden einer ausgehenden Nachricht
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md) und [Öffnen des Standardnachrichten Speichers](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner Postausgang. Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).
    
3. Rufen Sie die **IMAPIFolder:: CreateMessage** -Methode des Postausgangs Ordners auf, um die neue Nachricht zu erstellen. Weitere Informationen finden Sie unter [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),
    
4. Erstellen Sie eine Empfängerliste mit einem oder mehreren gelösten Empfängern. Weitere Informationen finden Sie unter [Erstellen einer Empfängerliste](creating-a-recipient-list.md).
    
5. Optional können Sie einen Betreff hinzufügen. Weitere Informationen finden Sie unter [Erstellen eines Nachrichtenbetreffs](creating-a-message-subject.md).
    
6. Fügen Sie den Nachrichtentext hinzu. Weitere Informationen finden Sie unter [Creating Message Text](creating-message-text.md).
    
7. Wenn der Nachrichtentext formatiert ist, fügen Sie Renderinginformationen hinzu. Weitere Informationen finden Sie unter [Hinzufügen von Renderinformationen zu formatiertEm Text](adding-rendering-information-to-formatted-text.md).
    
8. Optional können Sie eine oder mehrere Anlagen hinzufügen. Weitere Informationen finden Sie unter [Erstellen einer Nachrichtenanlage](creating-a-message-attachment.md).
    
9. Legen Sie andere Nachrichteneigenschaften wie gewünscht fest, und speichern und senden Sie dann die Nachricht, indem Sie **IMessage:: SubmitMessage**aufrufen. Weitere Informationen finden Sie unter [IMessage:: SubmitMessage](imessage-submitmessage.md).
    
10. Löschen Sie die gesendete Nachricht, wenn die **PR\_DELETE_AFTER_SUBMIT** ([PIDTAGDELETEAFTERSUBMIT (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf true festgelegt ist, oder verschieben Sie Sie in den Ordner, der durch die **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft identifiziert wird. Weitere Informationen finden Sie unter [Verarbeiten einer gesendetEn Nachricht](processing-a-sent-message.md).
    
Wenn Sie die Nachricht vor dem Senden erkennt speichern möchten, rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht auf. Weitere Informationen finden Sie unter [Speichern einer Nachricht](saving-a-message.md) oder [Senden einer Nachricht](sending-a-message.md). 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen einer Empfängerliste](creating-a-recipient-list.md): Beschreibt das Erstellen einer Empfängerliste.
    
- [Erstellen eines Nachrichtenbetreffs](creating-a-message-subject.md): Beschreibt, wie ein optionaler Betreff für eine Nachricht erstellt wird.
    
- [Erstellen von Nachrichtentext](creating-message-text.md): Beschreibt, wie Nachrichtentext erstellt wird.
    
- [Hinzufügen von Renderinformationen zu formatiertEm Text](adding-rendering-information-to-formatted-text.md): Beschreibt, wo in formatiertem Text eine Anlage gerendert werden soll.
    
- [Erstellen einer Nachrichtenanlage](creating-a-message-attachment.md): Beschreibt, wie Anlagen erstellt werden.
    
- [Speichern einer Nachricht](saving-a-message.md): Beschreibt, wie Clients Nachrichten speichern.
    
- [Senden einer Nachricht](sending-a-message.md): Beschreibt, wie eine Nachricht gesendet wird.
    
- [Verarbeiten einer gesendetEn Nachricht](processing-a-sent-message.md): Beschreibt, wie gesendete Nachrichten verarbeitet werden können.
    

