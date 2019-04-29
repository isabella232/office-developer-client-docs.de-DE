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
  
Das Weiterleiten einer Nachricht umfasst viele der gleichen Aufgaben wie das Senden einer ursprünglichen Nachricht. Zunächst müssen Sie den standardmäßigen Nachrichtenspeicher und den Ordner, der für ausgehende Nachrichten vorgesehen ist, in der Regel den Postausgang öffnen und die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode dieses Ordners aufrufen, um die zu sendende Nachricht zu erstellen. Sie müssen auch den Ordner öffnen, der die ursprüngliche Nachricht enthält, normalerweise den Posteingang. Informationen zum Öffnen unterschiedlicher Ordner finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).
  
Der Hauptunterschied zwischen dem Erstellen einer Nachricht, die weitergeleitet wird, und dem Erstellen des Originals besteht darin, dass die meisten Eigenschaften bei einer weitergeleiteten Nachricht direkt aus den Eigenschaften der ursprünglichen Nachricht kopiert werden. 
  
**So leiten Sie eine Nachricht weiter**
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen des Standardnachrichten Speichers](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner Postausgang. Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).
    
3. Rufen Sie die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode des Postausgangs auf, um eine neue weitergeleitete Nachricht zu erstellen. 
    
4. Rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode der ursprünglichen Nachricht auf, um die folgenden Eigenschaften in die weitergeleitete Nachricht zu kopieren: 
    
   - **PR\_** -Textkörper ([pidtagbody (](pidtagbody-canonical-property.md)), **PR\_-HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob Sie Rich-Text-Format, nur-Text oder HTML unterstützen.
    
   - **PR\_-NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Kopieren Sie die Nachrichtenanlagen aus der ursprünglichen Nachricht, indem Sie die **IMAPIProp:: CopyTo** -Methode der ursprünglichen Nachricht aufrufen, um die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft zu kopieren oder indem Sie Folgendes aufrufen. dreistufiges Verfahren für jede zu kopierende Anlage:
    
   1. Rufen Sie die [IMessage:: createattach](imessage-createattach.md) -Methode der neuen weitergeleiteten Nachricht auf, um eine neue Anlage zu erstellen. 
      
   2. Rufen Sie die [IMessage:: openattach](imessage-openattach.md) -Methode der ursprünglichen Nachricht auf, um die zu kopierende Anlage zu öffnen. 
      
   3. Rufen Sie die **IMAPIProp:: CopyTo** -Methode der ursprünglichen Nachricht auf, um alle Anlageneigenschaften aus der alten Anlage in die neue zu kopieren. 
    
6. Schließen Sie die folgenden Eigenschaften nicht in den Aufruf von **IMAPIProp:: CopyTo**ein: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([Pidtagmessagedownloadtime (](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** -Eigenschaften  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([Pidtagreadreceiptentryid (](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([Pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** -Eigenschaften  <br/> |**PR_REPLY_RECIPIENT** -Eigenschaften  <br/> |
|**PR_REPORT_ENTRYID** ([Pidtagreportentryid (](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER** -Eigenschaften  <br/> |
|**PR_SENT_REPRESENTING** -Eigenschaften  <br/> |**PR_SENTMAIL_ENTRYID** ([Pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([Pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Formatieren Sie den Nachrichtentext, indem Sie Einzüge und einen Kopf Absatz hinzufügen, der den ursprünglichen Absender, das Sendedatum, den Betreff und die Empfängerliste enthält. Verwenden Sie keine Präfixzeichen im Internet Format mit dem Inhalt.
    
2. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md)auf, und übergeben Sie den Wert der **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))-Eigenschaft der ursprünglichen Nachricht.
    
3. Legen Sie ein Präfix für die weitergeleitete Nachricht fest. Wenn Sie den Standard "FW:" verwenden, verketten Sie diese Zeichen am Anfang von **PR_NORMALIZED_SUBJECT** , und legen Sie **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf diese neue Zeichenfolge fest. Legen Sie **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md)) nicht fest. Wenn Sie ein nicht standardmäßiges Präfix verwenden, wie etwa eine Zeichenfolge mit mehr als drei Zeichen, speichern Sie es in **PR_SUBJECT_PREFIX**. 
    
4. Legen Sie die **PR_SENT_REPRESENTING** -Eigenschaften auf die entsprechenden Werte in den **PR_RCVD_REPRESENTING** -Eigenschaften fest. 
    
5. Erstellen Sie eine Empfängerliste. Weitere Informationen finden Sie unter [Erstellen einer Empfängerliste](creating-a-recipient-list.md).
    
6. Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der weitergeleiteten Nachricht auf, um Sie zu speichern, oder [IMessage:: SubmitMessage](imessage-submitmessage.md) , um Sie zu speichern und zu senden. 
    
## <a name="see-also"></a>Siehe auch

- [Kanonische Pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)

