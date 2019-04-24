---
title: IMessage-IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage
api_type:
- COM
ms.assetid: 7e244d40-595e-432c-aa8c-f9f62ca3c138
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 217411dc8bae12a3d7544a4cfd189c4c8f863195
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332872"
---
# <a name="imessage--imapiprop"></a>IMessage : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet Nachrichten, Anlagen und Empfänger.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Objekt Message  <br/> |
|Implementiert von:  <br/> |Nachrichtenspeicher Anbieter  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMessage  <br/> |
|Zeigertyp:  <br/> |LPMESSAGE  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetAttachmentable](imessage-getattachmenttable.md) <br/> |Gibt die Anlage Tabelle der Nachricht zurück.  <br/> |
|[OpenAttach](imessage-openattach.md) <br/> |Öffnet eine Anlage.  <br/> |
|[CreateAttach](imessage-createattach.md) <br/> |Erstellt eine neue Anlage.  <br/> |
|[DeleteAttach](imessage-deleteattach.md) <br/> |Löscht eine Anlage.  <br/> |
|[GetRecipientable](imessage-getrecipienttable.md) <br/> |Gibt die Empfängertabelle der Nachricht zurück.  <br/> |
|[ModifyRecipients](imessage-modifyrecipients.md) <br/> |Hinzugef�gt, gel�scht oder Empf�nger der Nachricht �ndert.  <br/> |
|[SubmitMessage](imessage-submitmessage.md) <br/> |Speichert alle Änderungen an der Nachricht und markiert sie als sendebereit.  <br/> |
|[SetReadFlag](imessage-setreadflag.md) <br/> |Das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht wird festgelegt oder gelöscht, und das Senden von Lese Berichten wird verwaltet.  <br/> |
   
Die folgenden Eigenschaften sind für Nachrichten zu einem bestimmten Zeitpunkt während ihres Lebenszyklus erforderlich. Die meisten schreibgeschützten Eigenschaften werden vom Nachrichtenspeicher Anbieter festgelegt, wenn ein Client die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode einer Nachricht aufruft. Andere schreibgeschützte Eigenschaften werden vom Transportanbieter festgelegt. 
  
|**Erforderliche Eigenschaften für Nachrichten aller Klassen**|**Access**|
|:-----|:-----|
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DISPLAY_BCC** ([Pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MESSAGE_RECIP_ME** ([Pidtagmessagerecipientme (](pidtagmessagerecipientme-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_MESSAGE_TO_ME** ([Pidtagmessagetome (](pidtagmessagetome-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_ORIGINATOR** -Eigenschaften  <br/> |Schreibgeschützt  <br/> |
|**PR_PARENT_DISPLAY** ([Pidtagparentdisplay (](pidtagparentdisplay-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_PARENT_ENTRYID** ([Pidtagparententryid (](pidtagparententryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECEIVED_BY** -Eigenschaften  <br/> |Schreibgeschützt  <br/> |
|**PR_RECIPIENT_TYPE** ([Pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_SENDER** -Eigenschaften  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
Die folgenden Eigenschaften sind alle für Clients schreibgeschützt, mit Ausnahme von **PR_BODY**. Clients erstellen diese Eigenschaft, wenn Sie einen Bericht verarbeiten.
  
|**Eigenschaften für Berichtnachrichten**|
|:-----|
|**PR_BODY** ([Pidtagbody (](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |
|**PR_MESSAGE_CLASS** <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([Pidtagoriginaldeliverytime (](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_BCC** ([Pidtagoriginaldisplaybcc (](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_CC** ([Pidtagoriginaldisplaycc (](pidtagoriginaldisplaycc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_TO** ([Pidtagoriginaldisplayto (](pidtagoriginaldisplayto-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBJECT** ([Pidtagoriginalsubject (](pidtagoriginalsubject-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBMIT_TIME** ([Pidtagoriginalsubmittime (](pidtagoriginalsubmittime-canonical-property.md))  <br/> |
|**PR_REPORT_TAG** ([Pidtagreporttag (](pidtagreporttag-canonical-property.md))  <br/> |
|**PR_REPORT_TEXT** ([Pidtagreporttext (](pidtagreporttext-canonical-property.md))  <br/> |
|**PR_REPORT_TIME** ([Pidtagreporttime (](pidtagreporttime-canonical-property.md))  <br/> |
|**PR_SEARCH_KEY** <br/> |
|**PR_SENDER** -Eigenschaften  <br/> |
|**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**Eigenschaften für Nachrichtenempfänger**|**Access**|**Erforderlich oder optional**|
|:-----|:-----|:-----|
|**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |Erforderlich  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |Erforderlich  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |Erforderlich  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |Optional  <br/> |
|**PR_ENTRYID** <br/> |Schreibgeschützt  <br/> |Erforderlich  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |Erforderlich  <br/> |
|**PR_SEARCH_KEY** <br/> |Schreibgeschützt  <br/> |Optional  <br/> |
   

