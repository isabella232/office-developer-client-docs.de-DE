---
title: Senden einer Antwort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f47741369b1091c0dd24358e063de8f4675000fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437448"
---
# <a name="sending-a-reply"></a>Senden einer Antwort

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen unterstützen in der Regel zwei Arten von Antworten: eine, die nur an den Absender der ursprünglichen Nachricht gesendet wird, und eine, die zusätzlich zum Absender an alle anderen Empfänger gesendet wird, die in der Empfängerliste der ursprünglichen Nachricht enthalten sind. Diese zweite Art von Antwort wird häufig als Antwort für alle Nachrichten bezeichnet.
  
Um eine Antwort eines der beiden Typen zu senden, implementieren Sie einige der gleichen Aufgaben wie beim Senden einer ursprünglichen Nachricht. Beispielsweise öffnen Sie den Standardnachrichtenspeicher und den Ordner für ausgehende Nachrichten, in der Regel den Posteingang, und rufen die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des ausgehenden Ordners auf, um die Antwort zu erstellen. Außerdem öffnen Sie den Ordner, der die ursprüngliche Nachricht enthält, in der Regel den Posteingang. Informationen zum Öffnen verschiedener Ordner finden Sie unter [Opening a Message Store Folder](opening-a-message-store-folder.md).
  
Der Hauptunterschied zwischen dem Erstellen einer Antwort und dem Erstellen einer ursprünglichen Nachricht ist, dass bei einer Antwort die meisten Eigenschaften entweder auf den Eigenschaften der ursprünglichen Nachricht basieren oder direkt aus diesen kopiert werden. Anlagen – die eigenschaft PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) einer Nachricht – werden ausdrücklich ausgeschlossen. Die Empfängerliste für eine Antwort alle Nachricht wird aus der Liste der ursprünglichen Nachricht erstellt, wobei der Empfänger durch die **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) -Eigenschaft und alle blinden #A0 entfernt wird. Die **PR_RECEIVED_BY_SEARCH_KEY-Eigenschaft** stellt den aktuellen Benutzer dar. 
  
### <a name="to-send-a-reply"></a>So senden Sie eine Antwort
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen der Standardnachricht Store](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner "Outbox". Weitere Informationen finden Sie unter [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des Posteingangs auf, um die Antwort zu erstellen. 
    
4. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) der ursprünglichen Nachricht auf, um die folgenden Eigenschaften in die Antwortnachricht zu kopieren: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob Sie Rich Text Format unterstützen.
    
   - **PR \_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), wenn die Antwort zur gesamten Empfängerliste geht.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Fügen Sie die folgenden Eigenschaften nicht in Ihren Aufruf von **IMAPIProp::CopyTo ein:**
    
    |||
    |:-----|:-----|
    |**\_ \_ PR-CLIENT-ABSENDENZEIT \_** <br/> |**ZUSTELLUNGSZEIT \_ FÜR \_ PR-NACHRICHTEN \_** <br/> |
    |**DOWNLOADZEIT \_ FÜR \_ PR-NACHRICHTEN \_** <br/> |**\_PR-NACHRICHTENFLAGS \_** <br/> |
    |**PR \_ ORIGINATOR \_ DELIVERY \_ REPORT\REQUESTED** <br/> |**PR \_ RCVD \_ REPRESENTING-Eigenschaften**  <br/> |
    |**PR \_ READ \_ RECEIPT \_ ENTRYID** <br/> |**ANGEFORDERTE \_ \_ PR-LESEBESTÄTIGUNG \_** <br/> |
    |**PR \_ RECEIVED \_ BY-Eigenschaften**  <br/> |**PR \_ EIGENSCHAFTEN \_ DES REPLY-EMPFÄNGERs**  <br/> |
    |**PR \_ REPORT \_ ENTRYID** <br/> |**PR \_ SENDER-Eigenschaften**  <br/> |
    |**PR \_ SENT \_ REPRESENTING-Eigenschaften**  <br/> |**PR \_ SENTMAIL \_ ENTRYID** <br/> |
    |**PRÄFIX \_ DES PR-BETREFFS \_** <br/> | <br/> |
   
6. Fügen Sie der von Ihnen unterstützten Nachrichtentexteigenschaft Trenntext hinzu– **PR_BODY**, **PR_HTM** L oder **PR_RTF_COMPRESSED**.
    
7. Rufen [Sie ScCreateConversationIndex auf,](sccreateconversationindex.md)und übergeben Sie den Wert der **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) -Eigenschaft der ursprünglichen Nachricht.
    
8. Legen Sie ein Präfix für die Antwort. Wenn Sie den Standard "RE:" verwenden, verketten Sie diese Zeichen am Anfang von **PR_NORMALIZED_SUBJECT,** und legen Sie **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf diese neue Zeichenfolge. Legen Sie keine **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) Wenn Sie ein nicht standardmäßiges Präfix verwenden, z. B. eine Zeichenfolge, die länger als drei Zeichen ist, speichern Sie es in **PR_SUBJECT_PREFIX**. 
    
9. Legen Sie **die PR_SENT_REPRESENTING** auf die entsprechenden Werte in den eigenschaften **PR_RCVD_REPRESENTING.** 
    
10. Legen Sie jeden der Einträge in **PR \_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY \_ RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) auf den Eintragsbezeichner und Anzeigenamen eines primären Empfängers – eines Empfängers, dessen Typ MAPI_TO. Halten Sie diese Eigenschaften synchronisiert. Das heißt, **PR_REPLY_RECIPIENT \_ ENTRIES** und **PR_REPLY_RECIPIENT_NAMES** müssen die gleiche Anzahl von Einträgen enthalten, und ein Eintrag an einer bestimmten Position in einer der Eigenschaften muss einem Eintrag an derselben Position in der anderen Eigenschaft entsprechen. 
    
11. Wenn die Antwort nur an den Absender der ursprünglichen Nachricht gesendet wird, erstellen Sie eine einzelne Eintragsempfängerliste mit dem Empfänger, der durch die Eigenschaft PR_SENT_REPRESENTING der **ursprünglichen** Nachricht dargestellt wird. Weitere Informationen zum Erstellen einer Empfängerliste finden Sie unter [Creating a Recipient List](creating-a-recipient-list.md).
    
12. Wenn es sich bei der Antwort um eine Antwort handelt, erstellen Sie eine Empfängerliste wie folgt:
    
    1. Rufen Sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) der ursprünglichen Nachricht auf, um auf die Empfängertabelle zu zugreifen. 
        
    2. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md) um alle Zeilen in der Tabelle abzurufen. Ermitteln Sie, ob jede Zeile einen primären Empfänger oder einen Co-Kopie-Empfänger darstellt und in der Liste verbleiben soll, oder ob sie einen Blindkopieempfänger oder den Benutzer darstellt und aus der Liste entfernt werden sollte. 
        
    3. Unterscheiden Sie zwischen Empfängertypen, indem Sie sich die **spalte PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) anschauen. Diese Spalte wird auf "MAPI_TO" für primäre Empfänger, MAPI_CC für Empfänger von Carbonkopien und MAPI_BCC für Blindkopieempfänger festgelegt. 
        
    4. Vergleichen Sie **die PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) mit der **PR_RECEIVED_BY_SEARCH_KEY-Eigenschaft** der ursprünglichen Nachricht, um zu ermitteln, ob die Zeile den Benutzer darstellt. 
        
    5. Entfernen Sie unerwünschte Zeilen aus der Empfängerliste, indem Sie [MAPIFreeBuffer](mapifreebuffer.md) aufrufen, um den Speicher frei zu geben, der den entsprechenden Einträgen in der [SRowSet-Struktur](srowset.md) der Empfängertabelle zugeordnet ist. Legen Sie alle Werte im Eigenschaftenwertarray auf Null, alle **cValues-Member** auf Null und alle **lpProps-Member** in jeder [SRow-Struktur](srow.md) im **SRowSet** auf NULL. 
        
    6. Fügen Sie den Absender der Empfängerliste hinzu, wie durch die Eigenschaften **PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) und **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) der ursprünglichen Nachricht dargestellt wird. Überprüfen Sie, ob der Absender in der Liste nicht dupliziert ist.
        
    7. Rufen Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) der Antwortnachricht auf, indem Sie den  _ulFlags-Parameter_ auf Null festlegen, um eine neue Empfängerliste für die Antwort oder weitergeleitete Nachricht basierend auf der Liste aus der ursprünglichen Nachricht zu erstellen. 
    
13. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Antwort auf, um die Nachricht oder [IMessage::SubmitMessage](imessage-submitmessage.md) zu speichern und zu senden. 
    
> [!NOTE]
> Bevor **Sie IMessage::ModifyRecipients** aufrufen, um Änderungen in der Empfängerliste zu speichern, können Sie Benutzern erlauben, Änderungen über das Nachrichtenformular vorzunehmen. Benutzer können der Liste hinzufügen oder bestimmte Mitglieder entfernen. Das Zulassen, dass Benutzer Änderungen an einer Empfängerliste vornehmen können, ist ein optionales Clientfeature. 
  

