---
title: Nachrichtenumschlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427192"
---
# <a name="message-envelope"></a>Nachrichtenumschlag

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
RFC 822-Header werden den MAPI-Eigenschaften wie folgt zugeordnet. PR_SENDER_ ist \* eine Abkürzung für die folgenden 5 Eigenschaften:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Ähnliche Abkürzungen werden für PR_SENT_REPRESENTING_ \* und andere Gruppen von Nachrichteneigenschaften verwendet.
  
|**SMTP-Header**|**MAPI-Eigenschaft**|
|:-----|:-----|
|Von:  <br/> |Ausgehend: PR_SENDER_ \* ; eingehende: PR_SENDER_ \* und PR_SENT_REPRESENTING_\*  <br/> |
|Datum:  <br/> |Ausgehend: aktuelle Uhrzeit; eingehenden: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|An:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) für Empfänger, bei denen **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, **PR_RECIPIENT_TYPE** MAPI_CC  <br/> |
|Bcc:  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, **PR_RECIPIENT_TYPE** MAPI_BCC  <br/> |
|||
|Empfangen:  <br/> |Keine entsprechende #A0 Geben Sie hier den lokalen Hostnamen und den Komponentennamen ein.  <br/> |
|Return-receipt-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Antwort an:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Betreff:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Keine bestimmte Längenbeschränkung.  <br/> |
|MIME-Version:  <br/> |Immer "1.0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Zur Kompatibilität mit MS Mail SMTP Gateway. _filename mm-dd-yyy hh:mm_Details unten.  <br/> |
|||
| _gesamtes SMTP-Nachrichtenumschlag_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|Headername TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for Absender only._The TBDheader sollte verwendet werden, um zu bestimmen, ob der Absender in der Lage ist, #A0 in einer Antwort zu interpretieren.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Entweder text/plain oder multipart/mixed. Siehe Abschnitt "Nachrichteninhalt".  <br/> |
   
Der X-MS-Attachment-Header ist als vier Token formatiert, getrennt durch ein Leerzeichen:
  
 _Datum der Namensgröße_
  
Das erste Token ist der Dateiname, der eingebettete Leerzeichen enthalten kann. Daher sollte dieser Header von rechts auf eingehende Nachrichten analysiert werden. Die Größe ist in Byte; das Datum ist als  _mm-dd-yyyy_ und die Uhrzeit  _als hh:mm formatiert._
  
> [!NOTE]
> MessageID wird nicht  PR_SEARCH_KEY, da die SMTP-Domäne bestimmte Anforderungen an das Format der Nachrichten-ID hat, die es unmöglich machen, einen beliebigen MAPI-Nachrichtenbezeichner zu codieren. Stattdessen wird MessageID **PR_TNEF_CORRELATION_KEY.** Diese Eigenschaft ist eine transportdefinierte Eigenschaft, die vom Transport festgelegt wird, der eine ausgehende Nachricht sendet und von einem Transport verwendet wird, der eine eingehende Nachricht empfängt. Weitere Informationen finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  

