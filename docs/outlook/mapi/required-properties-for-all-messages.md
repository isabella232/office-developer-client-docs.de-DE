---
title: Erforderliche Eigenschaften für alle Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df7e122f-0c44-4d81-8174-3a2d51671ba9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 329841a49154763a3e73a234e28def149719cb08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435978"
---
# <a name="required-properties-for-all-messages"></a>Erforderliche Eigenschaften für alle Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Tabelle werden die Eigenschaften beschrieben, die von Clients für Nachrichten aller Klassen festgelegt oder unterstützt werden können.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_CREATION_TIME** [Kanonische PidTagCreationTime-Eigenschaft](pidtagcreationtime-canonical-property.md) ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_DISPLAY_BCC** ([Pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md))  <br/> **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|||
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Kann von Clients für ausgehende Nachrichten festgelegt werden; muss von Nachrichtenspeicher Anbietern festgelegt werden, wenn Sie nicht von Clients festgelegt werden.  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Von Clients in ausgehenden Nachrichten vor dem Speichern und nach dem Speichern von Nachrichtenspeicher Anbietern festgelegt.  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> **PR_MESSAGE_RECIP_ME** ([Pidtagmessagerecipientme (](pidtagmessagerecipientme-canonical-property.md))  <br/> **PR_MESSAGE_TO_ME** ([Pidtagmessagetome (](pidtagmessagetome-canonical-property.md))  <br/> |Von Transportanbietern für eingehende Nachrichten festgelegt.  <br/> |
|||
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern in ausgehenden Nachrichten festgelegt  <br/> |
|**PR_ORIGINATOR_AND_DL_EXPANSION_HISTORY** ([Pidtagoriginatoranddistributionlistexpansionhistory (](pidtagoriginatoranddistributionlistexpansionhistory-canonical-property.md))  <br/> **PR_ORIGINATOR_CERTIFICATE** ([Pidtagoriginatorcertificate (](pidtagoriginatorcertificate-canonical-property.md))  <br/> **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([Pidtagoriginatornondeliveryreportrequested (](pidtagoriginatornondeliveryreportrequested-canonical-property.md))  <br/> **PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT** ([Pidtagoriginatorrequestedalternaterecipient (](pidtagoriginatorrequestedalternaterecipient-canonical-property.md))  <br/> **PR_ORIGINATOR_RETURN_ADDRESS** ([Pidtagoriginatorreturnaddress (](pidtagoriginatorreturnaddress-canonical-property.md))  <br/> |Von Transportanbietern in ausgehenden Nachrichten festgelegt.  <br/> |
|**PR_PARENT_ENTRYID** ([Pidtagparententryid (](pidtagparententryid-canonical-property.md))  <br/> **PR_PARENT_DISPLAY** ([Pidtagparentdisplay (](pidtagparentdisplay-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|||
|**PR_RCVD_REPRESENTING_ADDRTYPE** ([Pidtagreceivedrepresentingaddresstype (](pidtagreceivedrepresentingaddresstype-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([Pidtagreceivedrepresentingemailaddress (](pidtagreceivedrepresentingemailaddress-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_SEARCH_KEY** ([Pidtagreceivedrepresentingsearchkey (](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Von Transportanbietern für eingehende Nachrichten festgelegt.  <br/> |
|**PR_RECEIVED_BY_ADDRTYPE** ([Pidtagreceivedbyaddresstype (](pidtagreceivedbyaddresstype-canonical-property.md))  <br/> **PR_RECEIVED_BY_EMAIL_ADDRESS** ([Pidtagreceivedbyemailaddress (](pidtagreceivedbyemailaddress-canonical-property.md))  <br/> **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md))  <br/> **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md))  <br/> **PR_RECEIVED_BY_SEARCH_KEY** ([Pidtagreceivedbysearchkey (](pidtagreceivedbysearchkey-canonical-property.md))  <br/> |Von Transportanbietern für eingehende Nachrichten festgelegt.  <br/> |
|**PR_RECIPIENT_TYPE** ([Pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für eingehende Nachrichten festgelegt.  <br/> |
|**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
|**PR_SENDER_ADDRTYPE** ([Pidtagsenderaddresstype (](pidtagsenderaddresstype-canonical-property.md))  <br/> **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))  <br/> **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> **PR_SENDER_SEARCH_KEY** ([Pidtagsendersearchkey (](pidtagsendersearchkey-canonical-property.md))  <br/> |Clients können diese Eigenschaften für ausgehende Nachrichten festlegen, die von Transportanbietern jedoch festgelegt werden müssen.  <br/> |
|**PR_SENT_REPRESENTING_ADDRTYPE** ([Pidtagsentrepresentingaddresstype (](pidtagsentrepresentingaddresstype-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([Pidtagsentrepresentingemailaddress (](pidtagsentrepresentingemailaddress-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_ENTRYID** ([Pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_SEARCH_KEY** ([Pidtagsentrepresentingsearchkey (](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Clients können diese Eigenschaften für ausgehende Nachrichten festlegen, die von Transportanbietern jedoch festgelegt werden müssen.  <br/> |
|**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))  <br/> **PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))  <br/> |Von Nachrichtenspeicher Anbietern für ausgehende Nachrichten festgelegt.  <br/> |
   

