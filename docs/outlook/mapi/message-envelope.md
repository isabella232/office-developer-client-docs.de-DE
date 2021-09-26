---
title: Nachrichtenumschlag
manager: lindalu
ms.date: 09/14/2021
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Last modified: September 09, 2021'
ms.openlocfilehash: 787460bfbaebc6294f38dea4889cefec373c25a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620443"
---
# <a name="message-envelope"></a>Nachrichtenumschlag

**Gilt für**: Outlook 2013 | Outlook 2016
  
RFC 822-Header werden mapi-Eigenschaften wie folgt zugeordnet. PR_SENDER_ ist \* eine Abkürzung für die folgenden 5 Eigenschaften:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Ähnliche Abkürzungen werden für PR_SENT_REPRESENTING_ \* und andere Gruppen von Nachrichteneigenschaften verwendet.
  
|**SMTP-Header**|**MAPI-Eigenschaft**|
|:-----|:-----|
|Von:  <br/> |Ausgehend: \* PR_SENDER_; eingehend: PR_SENDER_ \* und PR_SENT_REPRESENTING_\*  <br/> |
|Datum:  <br/> |Ausgehend: aktuelle Zeit; eingehend: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|An:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) für Empfänger, bei denen **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, bei denen **PR_RECIPIENT_TYPE** MAPI_CC ist  <br/> |
|Bcc:  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, bei denen **PR_RECIPIENT_TYPE** MAPI_BCC ist  <br/> |
|||
|Erhalten:  <br/> |Keine entsprechende MAPI-Eigenschaft; Platzieren Sie hier den lokalen Hostnamen und den Komponentennamen.  <br/> |
|Return-receipt-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Antworten sie an:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Betreff:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Keine bestimmte Längenbeschränkung.  <br/> |
|MIME-Version:  <br/> |Immer "1.0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Aus Gründen der Kompatibilität mit dem MS Mail SMTP-Gateway. _filename Größe mm-dd-yyy hh:mm_Details unten.  <br/> |
|||
| _Gesamte SMTP-Nachrichtenumschlag_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|Headername TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for Absender only._The TBDheader sollte verwendet werden, um zu bestimmen, ob der Absender TNEF-Inhalte in einer Antwort interpretieren kann.  <br/> |
|Messageid:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Entweder Text/Nur-Text oder mehrteiliger/gemischter Text. Siehe Abschnitt "Nachrichteninhalt".  <br/> |
   
Der X-MS-Attachment-Header ist als vier Token formatiert, getrennt durch ein Leerzeichen:
  
 _Name Größe Datumszeit_
  
Das erste Token ist der Dateiname, der eingebettete Leerzeichen enthalten kann. Daher sollte dieser Header bei eingehenden Nachrichten von rechts analysiert werden. Die Größe ist in Byte angegeben. das Datum ist als  _mm-dd-yyyy_ formatiert und die Uhrzeit als  _hh:mm._
  
> [!NOTE]
> MessageID ist nicht **PR_SEARCH_KEY** zugeordnet, da die SMTP-Domäne bestimmte Anforderungen an das Format des Nachrichtenbezeichners hat, die es unmöglich machen, eine beliebige MAPI-Nachrichten-ID zu codieren. Stattdessen wird MessageID **PR_TNEF_CORRELATION_KEY** zugeordnet. Diese Eigenschaft ist eine transportdefinierte Eigenschaft, die vom Transport festgelegt wird, der eine ausgehende Nachricht sendet und von einem Transport verwendet wird, der eine eingehende Nachricht empfängt. Weitere Informationen finden Sie unter [Entwickeln eines TNEF-Enabled-Transportanbieters.](developing-a-tnef-enabled-transport-provider.md)
