---
title: Weiterleiten einer Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 37515d7a45115988945112bef892975bb193ff3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551590"
---
# <a name="forwarding-a-message"></a>Weiterleiten einer Nachricht

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Weiterleiten einer Nachricht umfasst viele der gleichen Aufgaben wie das Senden einer ursprünglichen Nachricht. Zuerst müssen Sie den Standardnachrichtenspeicher und den Ordner öffnen, der für ausgehende Nachrichten vorgesehen ist, in der Regel der Postausgang, und die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) dieses Ordners aufrufen, um die zu weiterleitende Nachricht zu erstellen. Sie müssen auch den Ordner öffnen, der die ursprüngliche Nachricht enthält, in der Regel den Posteingang. Informationen zum Öffnen verschiedener Ordner finden Sie unter [Öffnen einer Nachricht Store Ordners.](opening-a-message-store-folder.md)
  
Der Hauptunterschied zwischen dem Erstellen einer zu weiterleitenden Nachricht und dem Erstellen des Originals besteht darin, dass bei einer weitergeleiteten Nachricht die meisten Eigenschaften entweder auf eigenschaften der ursprünglichen Nachricht basieren oder direkt aus diesen kopiert werden. 
  
**So leiten Sie eine Nachricht weiter**
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen der Standardnachricht Store](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner "Postausgang". Weitere Informationen finden Sie unter [Öffnen einer Nachricht Store Ordners.](opening-a-message-store-folder.md)
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des Posteingangs auf, um eine neue weitergeleitete Nachricht zu erstellen. 
    
4. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) der ursprünglichen Nachricht auf, um die folgenden Eigenschaften in die weitergeleitete Nachricht zu kopieren: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob Sie Rich-Text-Format, Nur-Text oder HTML unterstützen.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Kopieren Sie die Nachrichtenanlagen aus der ursprünglichen Nachricht, indem Sie entweder die **IMAPIProp::CopyTo-Methode** der ursprünglichen Nachricht aufrufen, um die **eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) zu kopieren, oder indem Sie die folgenden drei Schritte für jede zu kopierende Anlage aufrufen:
    
   1. Rufen Sie die [IMessage::CreateAttach-Methode](imessage-createattach.md) der neuen weitergeleiteten Nachricht auf, um eine neue Anlage zu erstellen. 
      
   2. Rufen Sie die [IMessage::OpenAttach-Methode](imessage-openattach.md) der ursprünglichen Nachricht auf, um die zu kopierende Anlage zu öffnen. 
      
   3. Rufen Sie die **IMAPIProp::CopyTo-Methode** der ursprünglichen Nachricht auf, um alle Anlageneigenschaften aus der alten Anlage in die neue zu kopieren. 
    
6. Schließen Sie die folgenden Eigenschaften nicht in Den Aufruf von **IMAPIProp::CopyTo** ein: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** Eigenschaften  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** Eigenschaften  <br/> |**PR_REPLY_RECIPIENT** Eigenschaften  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER-Eigenschaften**  <br/> |
|**PR_SENT_REPRESENTING-Eigenschaften**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Formatieren Sie den Nachrichtentext durch Hinzufügen eines Einzugs und eines Kopfzeilenabsatzs, der den ursprünglichen Absender, das Datum der Übertragung, den Betreff und die Empfängerliste enthält. Fügen Sie keine Internetpräfixzeichen in den Inhalt ein.
    
2. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md)auf, und übergeben Sie den Wert der **eigenschaft PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) der ursprünglichen Nachricht.
    
3. Legen Sie ein Präfix für die weitergeleitete Nachricht fest. Wenn Sie den Standard "FW:" verwenden, verketten Sie diese Zeichen am Anfang von **PR_NORMALIZED_SUBJECT,** und legen **Sie PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf diese neue Zeichenfolge fest. **PR_SUBJECT_PREFIX** nicht festlegen ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Wenn Sie ein nicht standardmäßiges Präfix verwenden, z. B. eine Zeichenfolge, die länger als drei Zeichen ist, speichern Sie es in **PR_SUBJECT_PREFIX**. 
    
4. Legen Sie die **PR_SENT_REPRESENTING** Eigenschaften auf die entsprechenden Werte in den **eigenschaften PR_RCVD_REPRESENTING** fest. 
    
5. Dient zum Erstellen einer Empfängerliste. Weitere Informationen finden Sie unter [Erstellen einer Empfängerliste.](creating-a-recipient-list.md)
    
6. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der weitergeleiteten Nachricht auf, um sie zu speichern, oder [IMessage::SubmitMessage,](imessage-submitmessage.md) um sie zu speichern und zu senden. 
    
## <a name="see-also"></a>Siehe auch

- [PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)

