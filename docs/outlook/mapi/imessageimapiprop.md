---
title: IMessage IMAPIProp
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
ms.openlocfilehash: 9ed02e19a2934f785b03bb8553a08e16c7bb30e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792517"
---
# <a name="imessage--imapiprop"></a>IMessage: IMAPIProp

  
  
**Betrifft**: Outlook 
  
Verwaltet werden Nachrichten, die Anlagen und Empfänger.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Objekt Message  <br/> |
|Implementiert von:  <br/> |Nachricht-Anbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMessage  <br/> |
|Zeigertyp:  <br/> |LPMESSAGE  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetAttachmentTable](imessage-getattachmenttable.md) <br/> |Gibt die Nachricht Anlagentabelle zurück.  <br/> |
|[OpenAttach](imessage-openattach.md) <br/> |Öffnet eine Anlage.  <br/> |
|[CreateAttach](imessage-createattach.md) <br/> |Erstellt eine neue Anlage.  <br/> |
|[DeleteAttach](imessage-deleteattach.md) <br/> |Löscht eine Anlage.  <br/> |
|[GetRecipientTable](imessage-getrecipienttable.md) <br/> |Gibt die Empfänger der Nachricht-Tabelle zurück.  <br/> |
|[ModifyRecipients](imessage-modifyrecipients.md) <br/> |Hinzugef�gt, gel�scht oder Empf�nger der Nachricht �ndert.  <br/> |
|[SubmitMessage](imessage-submitmessage.md) <br/> |Speichert alle Änderungen auf die Nachricht und markiert sie als Vorbereitung auf senden.  <br/> |
|[SetReadFlag](imessage-setreadflag.md) <br/> |Festgelegt oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht und das Senden von lesen Berichte verwaltet.  <br/> |
   
Die folgenden Eigenschaften sind für Nachrichten zu einem bestimmten Zeitpunkt während ihres Lebenszyklus erforderlich. Die meisten Eigenschaften schreibgeschützt werden vom Anbieter Store Nachricht festgelegt, wenn ein Client eine Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufruft. Andere schreibgeschützte Eigenschaften werden von der Adressbuchhierarchie festgelegt. 
  
|**Erforderliche Eigenschaften für Nachrichten von allen Klassen**|**Zugriff**|
|:-----|:-----|
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_ORIGINATOR** -Eigenschaften  <br/> |Schreibgeschützt.  <br/> |
|**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECEIVED_BY** -Eigenschaften  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_SENDER** -Eigenschaften  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
Die folgenden Eigenschaften werden alle schreibgeschützt für Clients, mit Ausnahme von **PR_BODY**. Clients erstellen diese Eigenschaft, wenn sie einen Bericht verarbeiten.
  
|**Eigenschaften für Nachrichten melden**|
|:-----|
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC** ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md))  <br/> |
|**PR_MESSAGE_CLASS** <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_BCC** ([PidTagOriginalDisplayBcc](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_CC** ([PidTagOriginalDisplayCc](pidtagoriginaldisplaycc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_TO** ([PidTagOriginalDisplayTo](pidtagoriginaldisplayto-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBJECT** ([PidTagOriginalSubject](pidtagoriginalsubject-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md))  <br/> |
|**PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md))  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |
|**PR_SEARCH_KEY** <br/> |
|**PR_SENDER** -Eigenschaften  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**Eigenschaften für Empfänger der Nachricht**|**Zugriff**|**Erforderlich oder optional**|
|:-----|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |Erforderlich  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |Erforderlich  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |Erforderlich  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |Optional  <br/> |
|**PR_ENTRYID** <br/> |Schreibgeschützt.  <br/> |Erforderlich  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |Erforderlich  <br/> |
|**PR_SEARCH_KEY** <br/> |Schreibgeschützt.  <br/> |Optional  <br/> |
   

