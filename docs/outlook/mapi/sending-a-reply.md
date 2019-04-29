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
  
Client Anwendungen unterstützen in der Regel zwei Arten von Antworten: eine, die nur an den Absender der ursprünglichen Nachricht gesendet wird, und eine, die an alle anderen Empfänger gesendet wird, die in der Empfängerliste der ursprünglichen Nachricht zusätzlich zum Absender enthalten sind. Dieser zweite Antworttyp wird gemeinhin als "alle Antworten"-Nachricht bezeichnet.
  
Um eine Antwort von einem der beiden Typen zu senden, implementieren Sie einige der gleichen Aufgaben wie beim Senden einer ursprünglichen Nachricht. Sie können beispielsweise den standardmäßigen Nachrichtenspeicher und den Ordner für ausgehende Nachrichten öffnen, normalerweise den Postausgang, und die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode des ausgehenden Ordners aufrufen, um die Antwort zu erstellen. Außerdem öffnen Sie den Ordner, der die ursprüngliche Nachricht enthält, in der Regel den Posteingang. Informationen zum Öffnen unterschiedlicher Ordner finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).
  
Der Hauptunterschied zwischen dem Erstellen einer Antwort und dem Erstellen einer ursprünglichen Nachricht besteht darin, dass die meisten Eigenschaften mit einer Reply-Eigenschaft entweder auf oder direkt aus den Eigenschaften der ursprünglichen Nachricht kopiert werden. Attachments – die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft einer Nachricht ist ausdrücklich ausgeschlossen. Die Empfängerliste für eine alle Antworten Nachricht wird aus der ursprünglichen Liste der Nachricht mit dem Empfänger von der **PR_RECEIVED_BY_SEARCH_KEY** ([pidtagreceivedbysearchkey (](pidtagreceivedbysearchkey-canonical-property.md))-Eigenschaft dargestellt und alle Blind Carbon Copy-Empfänger entfernt erstellt. Die **PR_RECEIVED_BY_SEARCH_KEY** -Eigenschaft stellt den aktuellen Benutzer dar. 
  
### <a name="to-send-a-reply"></a>So senden Sie eine Antwort
  
1. Öffnen Sie den Standardnachrichtenspeicher. Weitere Informationen finden Sie unter [Öffnen des Standardnachrichten Speichers](opening-the-default-message-store.md).
    
2. Öffnen Sie den Ordner Postausgang. Weitere Informationen finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md).
    
3. Rufen Sie die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode des Postausgangs auf, um die Antwort zu erstellen. 
    
4. Rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode der ursprünglichen Nachricht auf, um die folgenden Eigenschaften in die Antwortnachricht zu kopieren: 
    
   - **PR\_-Textkörper** ([pidtagbody (](pidtagbody-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), je nachdem, ob Sie das Rich-Text-Format unterstützen oder nicht.
    
   - **PR\_-MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)), wenn die Antwort in der gesamten Empfängerliste angezeigt wird.
    
   - **PR\_-NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Schließen Sie die folgenden Eigenschaften nicht in den Aufruf von **IMAPIProp:: CopyTo**ein:
    
    |||
    |:-----|:-----|
    |**Zeit\_für\_die\_Einreichung des PR-Clients** <br/> |**Liefer\_\_Zeit\_für PR-Nachrichten** <br/> |
    |**Download\_\_Zeit\_der PR-Nachricht** <br/> |**PR\_-\_Nachrichtenkennzeichen** <br/> |
    |**PR\_-\_Absender\_ REPORT\REQUESTED** <br/> |**PR\_-\_RCVD** , die Eigenschaften darstellen  <br/> |
    |**PR\_-\_Lese\_Bestätigung-Eintrags-Nr.** <br/> |**PR\_-\_Lese\_Bestätigung angefordert** <br/> |
    |**Von\_Eigenschaften\_empfangene PR**  <br/> |**Empfänger\_Eigenschaften\_für PR-Antworten**  <br/> |
    |**PR\_-\_Bericht-Eintrags-Nr.** <br/> |**PR\_-Absender** Eigenschaften  <br/> |
    |**PR\_gesendet\_** , die Eigenschaften darstellt  <br/> |**PR\_-\_SENTMAIL-Eintrags-Nr.** <br/> |
    |**PR\_-\_Betreff-Präfix** <br/> | <br/> |
   
6. Hinzufügen von Trennzeichen zu jeder Nachrichtentext Eigenschaft, die Sie unterstützen – **PR_BODY**, **PR_HTM**L oder **PR_RTF_COMPRESSED**.
    
7. Rufen Sie [ScCreateConversationIndex](sccreateconversationindex.md)auf, und übergeben Sie den Wert der **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))-Eigenschaft der ursprünglichen Nachricht.
    
8. Legen Sie ein Präfix für die Antwort fest. Wenn Sie den Standard "RE:" verwenden, verketten Sie diese Zeichen am Anfang von **PR_NORMALIZED_SUBJECT** , und legen Sie **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) auf diese neue Zeichenfolge fest. Legen Sie **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md)) nicht fest. Wenn Sie ein nicht standardmäßiges Präfix verwenden, wie etwa eine Zeichenfolge mit mehr als drei Zeichen, speichern Sie es in **PR_SUBJECT_PREFIX**. 
    
9. Legen Sie die **PR_SENT_REPRESENTING** -Eigenschaften auf die entsprechenden Werte in den **PR_RCVD_REPRESENTING** -Eigenschaften fest. 
    
10. Legen Sie alle Einträge in **PR\_REPLY_RECIPIENT_ENTRIES** ([pidtagreplyrecipiententries (](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY\_RECIPIENT_NAMES** ([pidtagreplyrecipientnames (](pidtagreplyrecipientnames-canonical-property.md)) auf die Eintrags-ID und den Anzeigenamen eines primärer Empfänger – ein Empfänger, dessen Typ MAPI_TO ist. Halten Sie diese Eigenschaften synchronisiert. Das heißt, **PR_REPLY_RECIPIENT\_-Einträge** und **PR_REPLY_RECIPIENT_NAMES** müssen die gleiche Anzahl von Einträgen enthalten, und ein Eintrag an einer bestimmten Position in einer der Eigenschaften muss einem Eintrag an derselben Position in der anderen entsprechen. Eigenschaft. 
    
11. Wenn die Antwort nur an den Absender der ursprünglichen Nachricht gesendet wird, erstellen Sie eine einzelne Eintrags Empfängerliste mit dem Empfänger, der von der **PR_SENT_REPRESENTING** -Eigenschaft der ursprünglichen Nachricht dargestellt wird. Weitere Informationen zum Erstellen einer Empfängerliste finden Sie unter [Erstellen einer Empfängerliste](creating-a-recipient-list.md).
    
12. Wenn die Antwort eine Antwort ist, erstellen Sie eine Empfängerliste wie folgt:
    
    1. Rufen Sie die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode der ursprünglichen Nachricht auf, um auf die Empfängertabelle zuzugreifen. 
        
    2. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Zeilen in der Tabelle abzurufen. Bestimmen Sie, ob jede Zeile einen Primär-oder Kohlenstoff Kopie-Empfänger darstellt und in der Liste verbleiben soll, oder ob es sich um einen Blind Carbon Copy-Empfänger oder den Benutzer handelt und aus der Liste entfernt werden sollte. 
        
    3. UnterScheiden Sie zwischen Empfängertypen, indem Sie sich die Spalte **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md)) ansehen. Diese Spalte wird für primäre Empfänger, MAPI_CC für MAPI_TO-Empfänger und MAPI_BCC für blinde Kopie-Empfänger festgelegt. 
        
    4. Vergleichen Sie die **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Spalte mit der **PR_RECEIVED_BY_SEARCH_KEY** -Eigenschaft der ursprünglichen Nachricht, um zu bestimmen, ob die Zeile den Benutzer darstellt. 
        
    5. Entfernen Sie unerwünschte Zeilen aus der Empfängerliste, indem Sie [mapifreebufferfreigegeben](mapifreebuffer.md) aufrufen, um den Arbeitsspeicher freizugeben, der den entsprechenden Einträgen in der [SRowSet](srowset.md) -Struktur der Empfängertabelle zugeordnet ist. Legen Sie alle Werte im Eigenschaftswert Array auf 0 (null), alle **cValues** -Elemente auf 0 (null) und alle **lpProps** -Elemente in jeder [SRow](srow.md) -Struktur in der **SRowSet** auf NULL fest. 
        
    6. Hinzufügen des Absenders zur Empfängerliste gemäß der **PR\_-SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) und **PR_SENT_REPRESENTING_ENTRYID** ([pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md)) der ursprünglichen Nachricht Eigenschaften. Stellen Sie sicher, dass der Absender nicht in der Liste dupliziert wird.
        
    7. Rufen Sie die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode der Antwortnachricht auf, und legen Sie den Parameter _ulFlags_ auf NULL fest, um eine neue Empfängerliste für die Antwort oder weitergeleitete Nachricht zu erstellen, die auf der Liste der ursprünglichen Nachricht basiert. 
    
13. Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Antwort auf, um die Nachricht zu speichern, oder [IMessage:: SubmitMessage](imessage-submitmessage.md) , um Sie zu speichern und zu senden. 
    
> [!NOTE]
> Bevor Sie **IMessage:: ModifyRecipients** zum Speichern von Änderungen in der Empfängerliste aufrufen, können Sie Benutzern erlauben, Änderungen über das Nachrichtenformular vorzunehmen. Benutzer können der Liste hinzufügen oder bestimmte Mitglieder entfernen. Wenn Benutzer Änderungen an einer Empfängerliste vornehmen können, ist dies ein optionales Client Feature. 
  

