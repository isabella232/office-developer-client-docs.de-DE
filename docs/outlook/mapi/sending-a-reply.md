---
title: Senden eine Antwort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4d8c995f5fbca322fca44cdcbb0de224af6b2fbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590288"
---
# <a name="sending-a-reply"></a>Senden eine Antwort

**Betrifft**: Outlook 2013 | Outlook 2016 
  
-Clientanwendungen unterstützt zwei Arten von Antworten in der Regel: eine, die gesendet wird, nur für den Absender der ursprünglichen Nachricht, die an alle Empfänger, die in der ursprünglichen Nachricht zusätzlich zu den Absender der Empfängerliste enthalten gesendet wird. In diesem zweiten Art von Antwort wird häufig eine Antwort genannt, die alle Nachrichten.
  
Um eine Antwort eines beliebigen Typs zu senden, implementieren Sie einige der Aufgaben, die Sie würde, wenn Sie eine ursprüngliche Nachricht senden. Angenommen, öffnen Sie den standardmäßigen Nachrichtenspeicher und der ausgehende Nachrichtenordner, in der Regel im Ordner Postausgang, und rufen Sie den ausgehenden Ordner [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode, um die Antwort zu erstellen. Darüber hinaus öffnen Sie den Ordner, der die ursprüngliche Nachricht, typischerweise im Posteingang. Informationen zum Öffnen von verschiedenen Ordnern finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).
  
Der Hauptunterschied zwischen erstellen eine Antwort und erstellen eine ursprüngliche Nachricht ist, dass mit eine Antwort die, die meisten Eigenschaften sind entweder basierend auf, oder direkt über die Eigenschaften der ursprünglichen Nachricht kopiert. Anlagen – eine Nachricht **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft – insbesondere ausgeschlossen werden. Die Empfängerliste für eine Antwort, die alle Nachrichten mit dem Empfänger, dargestellt durch die Eigenschaft **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) und entfernt alle Bcc-Empfänger aus der ursprünglichen Nachricht erstellt wird. Die **PR_RECEIVED_BY_SEARCH_KEY** -Eigenschaft stellt den aktuellen Benutzer. 
  
### <a name="to-send-a-reply"></a>Um eine Antwort zu senden.
  
1. Öffnen Sie die Standard-Informationsspeicher. Weitere Informationen finden Sie unter [Standard-Informationsspeicher zu öffnen](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner Postausgang. Weitere Informationen finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md).
    
3. Rufen Sie den Postausgang [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode, um die Antwort zu erstellen. 
    
4. Rufen Sie die ursprüngliche Nachricht [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um die folgenden Eigenschaften in die Antwortnachricht zu kopieren: 
    
   - **Kurs\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob die Rich-Text-Format unterstützt.
    
   - **Kurs\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), wenn die Antwort an die gesamte Empfängerliste gesendet wird.
    
   - **Kurs\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Nehmen Sie die folgenden Eigenschaften nicht in den Anruf auf **IMAPIProp::CopyTo**aus:
    
    |||
    |:-----|:-----|
    |**Kurs\_CLIENT\_SUBMIT\_Zeit** <br/> |**Kurs\_Nachricht\_Übermittlung\_Zeit** <br/> |
    |**Kurs\_Nachricht\_herunterladen\_Zeit** <br/> |**Kurs\_Nachricht\_FLAGS** <br/> |
    |**Kurs\_Absender\_Übermittlung\_ REPORT\REQUESTED** <br/> |**PR\_empfangene\_REPRESENTING** Eigenschaften  <br/> |
    |**Kurs\_lesen\_Bestätigung\_ENTRYID** <br/> |**Kurs\_lesen\_Bestätigung\_angefordert** <br/> |
    |**PR\_RECEIVED\_BY** Eigenschaften  <br/> |**PR\_Antwort\_Empfänger** Eigenschaften  <br/> |
    |**Kurs\_Bericht\_ENTRYID** <br/> |**PR\_Absender** Eigenschaften  <br/> |
    |**PR\_gesendete\_REPRESENTING** Eigenschaften  <br/> |**Kurs\_SENTMAIL\_ENTRYID** <br/> |
    |**Kurs\_Betreff\_Präfix** <br/> | <br/> |
   
6. Hinzufügen von Trennzeichen Text günstigsten Nachricht-Body-Eigenschaft, die Sie unterstützen – **PR_BODY**, **PR_HTM**L oder **PR_RTF_COMPRESSED**.
    
7. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md), übergeben den Wert der Eigenschaft für die ursprüngliche Nachricht **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
8. Legen Sie ein Präfix für die Antwort. Bei Verwendung den Standard "AW:", diese Zeichen auf den Anfang der **PR_NORMALIZED_SUBJECT** verketten und **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf die neue Zeichenfolge festgelegt. **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) nicht festgelegt. Bei Verwendung ein nicht standardmäßigen Präfixes, wie eine Zeichenfolge mit mehr als drei Zeichen im **PR_SUBJECT_PREFIX**speichern. 
    
9. Legen Sie die **PR_SENT_REPRESENTING** -Eigenschaften auf die entsprechenden Werte in den Eigenschaften des **PR_RCVD_REPRESENTING** . 
    
10. Legen Sie jedes der Einträge im **PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) auf den Eintrag Bezeichner und Anzeigename den Namen des ein primäre Empfänger – eines Empfängers, dessen Typ MAPI_TO ist. Lassen Sie diese Eigenschaften synchronisiert. D. h., **PR_REPLY_RECIPIENT\_Einträge** **PR_REPLY_RECIPIENT_NAMES** muss die gleiche Anzahl von Einträgen aus der enthalten und ein Eintrag an einer bestimmten Position in der Eigenschaften eines Eintrags an derselben Position in der anderen entsprechen -Eigenschaft. 
    
11. Wenn die Antwort nur an den Absender der ursprünglichen Nachricht gesendet wird, erstellen Sie eine einzelnen Eintrag Empfängerliste mit dem Empfänger, dargestellt durch die ursprüngliche Nachricht **PR_SENT_REPRESENTING** -Eigenschaft. Weitere Informationen zum Erstellen einer Empfängerliste finden Sie unter [Erstellen einer Empfängerliste](creating-a-recipient-list.md).
    
12. Wenn die Antwort auf eine Antwort, die alle ist, erstellen Sie eine Empfängerliste wie folgt:
    
    1. Rufen Sie die ursprüngliche Nachricht [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode zum Zugriff auf die Empfänger Tabelle. 
        
    2. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) , um alle Zeilen in der Tabelle abzurufen. Bestimmen Sie, wenn jede Zeile einen Primär- oder Carbon Copy, Blindkopie Empfänger stellt und in der Liste bleiben soll, oder wenn er einen Bcc-Empfänger oder der Benutzer stellt und aus der Liste entfernt werden soll. 
        
    3. Unterscheiden Sie zwischen Empfängertypen anhand der Spalte **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Diese Spalte wird MAPI_TO für primären Empfänger, MAPI_CC für Cc-Empfänger und MAPI_BCC für blind Carbon Copy, Blindkopie Empfänger festgelegt. 
        
    4. Vergleichen der Spalte **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) mit der **PR_RECEIVED_BY_SEARCH_KEY** -Eigenschaft der ursprünglichen Nachricht zu ermitteln, ob die Zeile den Benutzer darstellt. 
        
    5. Entfernen Sie unerwünschte Zeilen aus der Empfängerliste durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) , um die entsprechenden Einträge in der Empfänger [SRowSet](srowset.md) Tabellenstruktur zugeordneten Arbeitsspeicher freizugeben. Alle Werte im Array Eigenschaft Wert, alle Mitglieder **cValues** 0 (null), 0 (null) und alle Mitglieder **LpProps** in jedem [SRow](srow.md) Struktur in der **SRowSet** auf NULL festgelegt wurde. 
        
    6. Den Absender der Empfängerliste hinzufügen, dargestellt durch der ursprünglichen Nachricht **PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) und **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) Eigenschaften. Überprüfen Sie, dass der Absender in der Liste nicht dupliziert werden.
        
    7. Rufen Sie die Antwortnachricht [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode, wenn der Parameter _UlFlags_ auf 0 (null), um eine neue Empfängerliste zur Beantwortung erstellen oder weitergeleitete Nachricht basierend auf der Liste aus der ursprünglichen Nachricht. 
    
13. Rufen Sie die Antwort [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zum Speichern der Nachricht oder [IMessage::SubmitMessage](imessage-submitmessage.md) zu speichern und senden. 
    
> [!NOTE]
> Bevor Sie **IMessage::ModifyRecipients** zum Speichern der Änderungen in der Empfängerliste aufrufen, können Sie Benutzer über das Nachrichtenformular Modifikationen gestatten. Benutzer können der Liste hinzufügen oder Entfernen von bestimmten Mitglieder. Ermöglichen, dass Benutzer eine Empfängerliste ändern ist eine optionale Clientfunktion. 
  

