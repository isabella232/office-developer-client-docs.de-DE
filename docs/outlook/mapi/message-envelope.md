---
title: Nachrichtenumschlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356924"
---
# <a name="message-envelope"></a>Nachrichtenumschlag

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
RFC 822-Header werden MAPI-Eigenschaften wie folgt zugeordnet. PR_SENDER_\* ist eine Abkürzung für die folgenden 5 Eigenschaften:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([Pidtagsenderaddresstype (](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([Pidtagsendersearchkey (](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Ähnliche Abkürzungen werden für PR_SENT_REPRESENTING_\* und andere Gruppen von Nachrichteneigenschaften verwendet.
  
|**SMTP-Header**|**MAPI-Eigenschaft**|
|:-----|:-----|
|Von:  <br/> |Ausgehend\*: PR_SENDER_; eingehend: PR_SENDER_\* und PR_SENT_REPRESENTING_\*  <br/> |
|Datum  <br/> |Ausgehend: aktuelle Uhrzeit; eingehend: **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|An:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) für Empfänger, bei denen **PR_RECIPIENT_TYPE** ([pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md)) MAPI_TO ist  <br/> |
|CC  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, bei denen **PR_RECIPIENT_TYPE** MAPI_CC ist  <br/> |
|BCC  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, bei denen **PR_RECIPIENT_TYPE** MAPI_BCC ist  <br/> |
|||
|Empfangen  <br/> |Keine entsprechende MAPI-Eigenschaft; Geben Sie hier den lokalen Hostnamen und ihren Komponentennamen ein.  <br/> |
|Return-Receipt-an:  <br/> |**PR_REPORT_NAME** ([Pidtagreportname (](pidtagreportname-canonical-property.md)) und **PR_REPORT_ENTRYID** ([pidtagreportentryid (](pidtagreportentryid-canonical-property.md))  <br/> |
|Reply-an:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([Pidtagreplyrecipiententries (](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY_RECIPIENT_NAMES** ([pidtagreplyrecipientnames (](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Betreff:  <br/> |**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) Keine bestimmte Längenbeschränkung.  <br/> |
|MIME-Version:  <br/> |Immer "1,0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Zur Kompatibilität mit dem MS Mail-SMTP-Gateway. _FileName Größe mm-DD-yyy hh: mm_Details unten.  <br/> |
|||
| _vollständiger SMTP-Nachrichtenumschlag_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([Pidtagtransportmessageheaders (](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|Kopfzeilenname ist festgelegt  <br/> |**PR_SEND_RICH_INFO** ([Pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md)) _for Sender only. _The-TBDheader sollte verwendet werden, um zu bestimmen, ob der Absender TNEF-Inhalte in einer Antwort interpretieren kann.  <br/> |
|MessageId  <br/> |**PR_TNEF_CORRELATION_KEY** ([Pidtagtnefcorrelationkey (](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Entweder Text/Plain oder multipart/mixed. Weitere Informationen finden Sie im Abschnitt "Nachrichteninhalt".  <br/> |
   
Der X-MS-Attachment-Header ist als vier Token formatiert, getrennt durch ein Leerzeichen:
  
 _namens Größe (Datum)_
  
Das erste Token ist der Dateiname, der möglicherweise eingebettete Leerzeichen enthält, sodass diese Kopfzeile von rechts auf eingehende Nachrichten analysiert werden sollte. Die Größe ist in Byte; das Datum ist als _mm-tt-yyyy_ und als _hh: mm formatiert._
  
> [!NOTE]
> MessageID ist nicht **PR_SEARCH_KEY** zugeordnet, da die SMTP-Domäne bestimmte Anforderungen an das Format der Nachrichtenkennung hat, die es unmöglich macht, einen beliebigen MAPI-Nachrichtenbezeichner zu codieren. Stattdessen wird MessageID **PR_TNEF_CORRELATION_KEY**zugeordnet. Diese Eigenschaft ist eine Transport definierte Eigenschaft, die durch den Transport festgelegt wird, der eine ausgehende Nachricht sendet und von einem Transport verwendet wird, der eine eingehende Nachricht empfängt. Weitere Informationen finden Sie unter [Entwickeln eines TNEF-fähigEn Transport Anbieters](developing-a-tnef-enabled-transport-provider.md). 
  

