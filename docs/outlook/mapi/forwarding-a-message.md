---
title: Weiterleiten einer Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 146c8b4d711982118fd9da185a5b095a1bae6b2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791736"
---
# <a name="forwarding-a-message"></a>Weiterleiten einer Nachricht

**Betrifft**: Outlook 
  
Weiterleiten einer Nachricht umfasst viele der dieselben Aufgaben wie die ursprüngliche Nachricht. Zuerst, öffnen Sie den standardmäßigen Nachrichtenspeicher und dem Ordner, der ausgehende Nachrichten, in der Regel im Ordner Postausgang, halten und rufen Sie diesen Ordner [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode, um die Nachricht weitergeleitet werden zu erstellen. Darüber hinaus müssen Sie den Ordner öffnen, der die ursprüngliche Nachricht, typischerweise im Posteingang enthält. Informationen zum Öffnen von verschiedenen Ordnern finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).
  
Der Hauptunterschied zwischen Erstellen einer Nachricht weitergeleitet werden, und erstellen die ursprüngliche ist, dass mit einer weitergeleiteten Nachricht, die meisten Eigenschaften sind entweder basierend auf, oder direkt über die Eigenschaften der ursprünglichen Nachricht kopiert. 
  
**Um eine Nachricht weiterzuleiten**
  
1. Öffnen Sie die Standard-Informationsspeicher. Weitere Informationen finden Sie unter [Standard-Informationsspeicher zu öffnen](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner Postausgang. Weitere Informationen finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).
    
3. Rufen Sie den Postausgang [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode zum Erstellen einer neuen Nachricht weitergeleiteten. 
    
4. Rufen Sie die ursprüngliche Nachricht [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um die folgenden Eigenschaften in der weitergeleiteten Nachricht zu kopieren: 
    
   - **Kurs\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob die Rich-Text-Format, nur-Text oder HTML unterstützt.
    
   - **Kurs\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Kopieren Sie die e-Mail-Anlagen aus der ursprünglichen Nachricht durch Aufrufen der ursprünglichen Nachricht **IMAPIProp::CopyTo** -Methode, um die Eigenschaft **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) zu kopieren oder durch den folgenden Aufruf drei Schritt-Verfahren für jede Anlage kopiert werden:
    
   1. Rufen Sie die neue Nachricht [IMessage::CreateAttach](imessage-createattach.md) -Methode, um eine neue Anlage erstellen weitergeleitet. 
      
   2. Rufen Sie die ursprüngliche Nachricht [IMessage::OpenAttach](imessage-openattach.md) -Methode zum Öffnen der Anlage kopiert werden soll. 
      
   3. Rufen Sie die ursprüngliche Nachricht **IMAPIProp::CopyTo** -Methode, um alle Anlagen Eigenschaften aus der alten Anlage in die neue kopieren. 
    
6. Nehmen Sie die folgenden Eigenschaften nicht in den Anruf auf **IMAPIProp::CopyTo**aus: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** -Eigenschaften  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** -Eigenschaften  <br/> |**PR_REPLY_RECIPIENT** -Eigenschaften  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER** -Eigenschaften  <br/> |
|**PR_SENT_REPRESENTING** -Eigenschaften  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Formatieren Sie den Nachrichtentext durch Hinzufügen von Einzug und einer Kopfzeile Absatz, der den ursprünglichen Absender enthält Datum der Übertragung, Betreff und Empfängerliste. Schließen Sie Internet-Schreibweise Anfangszeichen mit dem Inhalt nicht.
    
2. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md), übergeben den Wert der Eigenschaft für die ursprüngliche Nachricht **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
3. Legen Sie ein Präfix für den weitergeleiteten Nachrichten. Bei Verwendung den Standard "Firmware:", diese Zeichen auf den Anfang der **PR_NORMALIZED_SUBJECT** verketten und **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf die neue Zeichenfolge festgelegt. **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) nicht festgelegt. Bei Verwendung ein nicht standardmäßigen Präfixes, wie eine Zeichenfolge mit mehr als drei Zeichen im **PR_SUBJECT_PREFIX**speichern. 
    
4. Legen Sie die **PR_SENT_REPRESENTING** -Eigenschaften auf die entsprechenden Werte in den Eigenschaften des **PR_RCVD_REPRESENTING** . 
    
5. Erstellen einer Empfängerliste. Weitere Informationen finden Sie unter [Erstellen einer Liste der Empfänger](creating-a-recipient-list.md).
    
6. Rufen Sie die weitergeleitete Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zum Speichern oder [IMessage::SubmitMessage](imessage-submitmessage.md) zu speichern und senden. 
    
## <a name="see-also"></a>Siehe auch

- [PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)

