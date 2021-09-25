---
title: Senden einer Antwort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2d21f62900ca1a9cbeb6aab84695409a40f03fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609446"
---
# <a name="sending-a-reply"></a>Senden einer Antwort

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen unterstützen in der Regel zwei Arten von Antworten: eine, die nur an den Absender der ursprünglichen Nachricht gesendet wird, und eine, die zusätzlich zum Absender an alle anderen Empfänger gesendet wird, die in der Empfängerliste der ursprünglichen Nachricht enthalten sind. Dieser zweite Antworttyp wird allgemein als Antwort auf alle Nachrichten bezeichnet.
  
Um eine Antwort eines der beiden Typen zu senden, implementieren Sie einige der gleichen Aufgaben wie beim Senden einer ursprünglichen Nachricht. Beispielsweise öffnen Sie den Standardnachrichtenspeicher und den Ordner für ausgehende Nachrichten, in der Regel den Postausgang, und rufen die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des ausgehenden Ordners auf, um die Antwort zu erstellen. Außerdem öffnen Sie den Ordner, der die ursprüngliche Nachricht enthält, in der Regel den Posteingang. Informationen zum Öffnen verschiedener Ordner finden Sie unter [Öffnen einer Nachricht Store Ordners.](opening-a-message-store-folder.md)
  
Der Hauptunterschied zwischen dem Erstellen einer Antwort und dem Erstellen einer ursprünglichen Nachricht besteht darin, dass bei einer Antwort die meisten Eigenschaften entweder auf eigenschaften der ursprünglichen Nachricht basieren oder direkt aus diesen kopiert werden. Anlagen – **die eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) einer Nachricht – werden ausdrücklich ausgeschlossen. Die Empfängerliste für eine Antwort auf alle Nachrichten wird aus der Liste der ursprünglichen Nachricht erstellt, wobei der Empfänger durch die **Eigenschaft PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) dargestellt wird und alle Blindkopieempfänger entfernt werden. Die **PR_RECEIVED_BY_SEARCH_KEY-Eigenschaft** stellt den aktuellen Benutzer dar. 
  
### <a name="to-send-a-reply"></a>So senden Sie eine Antwort
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen der Standardnachricht Store](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner "Postausgang". Weitere Informationen finden Sie unter [Öffnen einer Nachricht Store Ordners.](opening-a-message-store-folder.md)
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des Posteingangs auf, um die Antwort zu erstellen. 
    
4. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) der ursprünglichen Nachricht auf, um die folgenden Eigenschaften in die Antwortnachricht zu kopieren: 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob Rich Text Format unterstützt wird.
    
   - **PR \_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), wenn die Antwort an die gesamte Empfängerliste gesendet wird.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Schließen Sie die folgenden Eigenschaften nicht in Den Aufruf von **IMAPIProp::CopyTo** ein:
    
    |||
    |:-----|:-----|
    |**\_ \_ ABSENDEN DES PR-CLIENTS \_** <br/> |**\_ \_ ÜBERMITTLUNGSZEIT FÜR PR-NACHRICHTEN \_** <br/> |
    |**\_ \_ DOWNLOADZEIT FÜR PR-NACHRICHTEN \_** <br/> |**\_ \_ PR-NACHRICHTEN-FLAGS** <br/> |
    |**PR \_ ORIGINATOR \_ DELIVERY \_ REPORT\REQUESTED** <br/> |**PR \_ \_RCVD-DARSTELLUNG von** Eigenschaften  <br/> |
    |**PR \_ READ \_ RECEIPT \_ ENTRYID** <br/> |**\_PR-LESEBESTÄTIGUNG \_ \_ ANGEFORDERT** <br/> |
    |**PR \_ RECEIVED \_ BY-Eigenschaften**  <br/> |**PR \_ REPLY \_ RECIPIENT-Eigenschaften**  <br/> |
    |**PR \_ REPORT \_ ENTRYID** <br/> |**PR \_ SENDER-Eigenschaften**  <br/> |
    |**PR \_ GESENDETE \_ DARSTELLUNGSeigenschaften**  <br/> |**PR \_ SENTMAIL \_ ENTRYID** <br/> |
    |**\_PRÄFIX FÜR PR-BETREFF \_** <br/> | <br/> |
   
6. Fügen Sie der unterstützten Nachrichtentexteigenschaft Trenntext hinzu – **PR_BODY,** **PR_HTM** L oder **PR_RTF_COMPRESSED.**
    
7. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md)auf, und übergeben Sie den Wert der **eigenschaft PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) der ursprünglichen Nachricht.
    
8. Legen Sie ein Präfix für die Antwort fest. Wenn Sie den Standard "RE:" verwenden, verketten Sie diese Zeichen am Anfang von **PR_NORMALIZED_SUBJECT,** und legen **Sie PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf diese neue Zeichenfolge fest. **PR_SUBJECT_PREFIX** nicht festlegen ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Wenn Sie ein nicht standardmäßiges Präfix verwenden, z. B. eine Zeichenfolge, die länger als drei Zeichen ist, speichern Sie es in **PR_SUBJECT_PREFIX**. 
    
9. Legen Sie die **PR_SENT_REPRESENTING** Eigenschaften auf die entsprechenden Werte in den **eigenschaften PR_RCVD_REPRESENTING** fest. 
    
10. Legen Sie alle Einträge in **PR \_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY \_ RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) auf die Eintrags-ID und den Anzeigenamen eines primären Empfängers fest – einen Empfänger, dessen Typ MAPI_TO ist. Lassen Sie diese Eigenschaften synchronisiert. Das heißt, **PR_REPLY_RECIPIENT \_ ENTRIES** und **PR_REPLY_RECIPIENT_NAMES** müssen dieselbe Anzahl von Einträgen enthalten, und ein Eintrag an einer bestimmten Position in einer der Eigenschaften muss einem Eintrag an derselben Position in der anderen Eigenschaft entsprechen. 
    
11. Wenn die Antwort nur an den Absender der ursprünglichen Nachricht gesendet wird, erstellen Sie eine Empfängerliste mit einem einzelnen Eintrag, wobei der Empfänger durch die **eigenschaft PR_SENT_REPRESENTING** der ursprünglichen Nachricht dargestellt wird. Weitere Informationen zum Erstellen einer Empfängerliste finden Sie unter [Erstellen einer Empfängerliste.](creating-a-recipient-list.md)
    
12. Wenn es sich bei der Antwort um eine Antwort handelt, erstellen Sie eine Empfängerliste wie folgt:
    
    1. Rufen Sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) der ursprünglichen Nachricht auf, um auf die Empfängertabelle zuzugreifen. 
        
    2. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen in der Tabelle abzurufen. Bestimmen Sie, ob jede Zeile einen primären empfänger oder einen Kopierempfänger darstellt und in der Liste verbleiben soll oder ob sie einen blinden Empfänger einer Kopie oder den Benutzer darstellt und aus der Liste entfernt werden soll. 
        
    3. Unterscheiden Sie zwischen Empfängertypen, indem Sie die **Spalte PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) betrachten. Diese Spalte wird auf MAPI_TO für primäre Empfänger, MAPI_CC für Empfänger von Kopierkopien und MAPI_BCC für Blindkopieempfänger festgelegt. 
        
    4. Vergleichen Sie die Spalte **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) mit der **PR_RECEIVED_BY_SEARCH_KEY** Eigenschaft der ursprünglichen Nachricht, um zu bestimmen, ob die Zeile den Benutzer darstellt. 
        
    5. Entfernen Sie unerwünschte Zeilen aus der Empfängerliste, indem Sie [MAPIFreeBuffer](mapifreebuffer.md) aufrufen, um den Speicher freizugeben, der den entsprechenden Einträgen in der [SRowSet-Struktur](srowset.md) der Empfängertabelle zugeordnet ist. Legen Sie alle Werte im Eigenschaftswertarray auf Null, alle **cValues-Elemente** auf Null und alle **lpProps-Elemente** in jeder [SRow-Struktur](srow.md) im **SRowSet** auf NULL fest. 
        
    6. Fügen Sie den Absender der Empfängerliste hinzu, wie durch die **\_ PR-SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) und **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) -Eigenschaften der ursprünglichen Nachricht dargestellt. Überprüfen Sie, ob der Absender in der Liste nicht dupliziert wurde.
        
    7. Rufen Sie die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) der Antwortnachricht auf, indem Sie den  _ulFlags-Parameter_ auf Null festlegen, um eine neue Empfängerliste für die Antwort oder weitergeleitete Nachricht basierend auf der Liste aus der ursprünglichen Nachricht zu erstellen. 
    
13. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Antwort auf, um die Nachricht zu speichern, oder [IMessage::SubmitMessage,](imessage-submitmessage.md) um sie zu speichern und zu senden. 
    
> [!NOTE]
> Vor dem Aufrufen von **IMessage::ModifyRecipients** zum Speichern von Änderungen in der Empfängerliste können Sie Benutzern erlauben, Änderungen über das Nachrichtenformular vorzunehmen. Benutzer können der Liste hinzufügen oder bestimmte Mitglieder entfernen. Das Zulassen von Benutzern, Änderungen an einer Empfängerliste vorzunehmen, ist ein optionales Clientfeature. 
  

