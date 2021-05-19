---
title: Weiterleiten einer Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433178"
---
# <a name="forwarding-a-message"></a>Weiterleiten einer Nachricht

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Weiterleiten einer Nachricht umfasst viele der gleichen Aufgaben wie das Senden einer ursprünglichen Nachricht. Zunächst müssen Sie den Standardnachrichtenspeicher und den Ordner öffnen, der für ausgehende Nachrichten, in der Regel für den Posteingang, bestimmt ist, und die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) dieses Ordners aufrufen, um die zu weiterleitende Nachricht zu erstellen. Sie müssen auch den Ordner öffnen, der die ursprüngliche Nachricht enthält, in der Regel den Posteingang. Informationen zum Öffnen verschiedener Ordner finden Sie unter [Opening a Message Store Folder](opening-a-message-store-folder.md).
  
Der Hauptunterschied zwischen dem Erstellen einer nachricht, die weitergeleitet werden soll, und dem Erstellen des Originals besteht in der, dass bei einer weitergeleiteten Nachricht die meisten Eigenschaften entweder auf Eigenschaften der ursprünglichen Nachricht basieren oder direkt aus diesen kopiert werden. 
  
**So weiterleiten Sie eine Nachricht**
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen der Standardnachricht Store](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner "Outbox". Weitere Informationen finden Sie unter [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des Posteingangs auf, um eine neue weitergeleitete Nachricht zu erstellen. 
    
4. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) der ursprünglichen Nachricht auf, um die folgenden Eigenschaften in die weitergeleitete Nachricht zu kopieren: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob Sie Rich Text Format, Nur-Text oder HTML unterstützen.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Kopieren Sie die Nachrichtenanlagen aus der ursprünglichen Nachricht, indem Sie entweder die **IMAPIProp::CopyTo-Methode** der ursprünglichen Nachricht aufrufen, um die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft zu kopieren, oder indem Sie die folgenden drei Schritte für jede zu kopierende Anlage aufrufen:
    
   1. Rufen Sie die [IMessage::CreateAttach-Methode](imessage-createattach.md) der neuen weitergeleiteten Nachricht auf, um eine neue Anlage zu erstellen. 
      
   2. Rufen Sie die [IMessage::OpenAttach-Methode](imessage-openattach.md) der ursprünglichen Nachricht auf, um die zu kopierende Anlage zu öffnen. 
      
   3. Rufen Sie die **IMAPIProp::CopyTo-Methode** der ursprünglichen Nachricht auf, um alle Anlageneigenschaften aus der alten Anlage in die neue zu kopieren. 
    
6. Fügen Sie die folgenden Eigenschaften nicht in Ihren Aufruf von **IMAPIProp::CopyTo ein:** 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** Eigenschaften  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** Eigenschaften  <br/> |**PR_REPLY_RECIPIENT** Eigenschaften  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER** Eigenschaften  <br/> |
|**PR_SENT_REPRESENTING** Eigenschaften  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Formatieren Sie den Nachrichtentext, indem Sie Einzug und einen Kopfzeilenabsatz hinzufügen, der den ursprünglichen Absender, das Übertragungsdatum, den Betreff und die Empfängerliste enthält. Schließen Sie keine Präfixzeichen im Internetformat in den Inhalt ein.
    
2. Rufen [Sie ScCreateConversationIndex auf,](sccreateconversationindex.md)und übergeben Sie den Wert der **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) -Eigenschaft der ursprünglichen Nachricht.
    
3. Legen Sie ein Präfix für die weitergeleitete Nachricht. Wenn Sie den Standard "FW:" verwenden, verketten Sie diese Zeichen am Anfang von **PR_NORMALIZED_SUBJECT,** und legen Sie **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf diese neue Zeichenfolge. Legen Sie keine **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) Wenn Sie ein nicht standardmäßiges Präfix verwenden, z. B. eine Zeichenfolge, die länger als drei Zeichen ist, speichern Sie es in **PR_SUBJECT_PREFIX**. 
    
4. Legen Sie **die PR_SENT_REPRESENTING** auf die entsprechenden Werte in den eigenschaften **PR_RCVD_REPRESENTING.** 
    
5. Erstellen Sie eine Empfängerliste. Weitere Informationen finden Sie unter [Creating a Recipient List](creating-a-recipient-list.md).
    
6. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der weitergeleiteten Nachricht auf, um sie zu speichern, oder [IMessage::SubmitMessage,](imessage-submitmessage.md) um sie zu speichern und zu senden. 
    
## <a name="see-also"></a>Siehe auch

- [PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)

