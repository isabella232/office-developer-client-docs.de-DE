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
ms.openlocfilehash: fd642575a3136eef3193e0bdbe884cf8f54ba337
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571297"
---
# <a name="message-envelope"></a>Nachrichtenumschlag

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
RFC 822 Kopfzeilen werden wie folgt zu MAPI-Eigenschaften zugeordnet. PR_SENDER_\* ist eine Abkürzung für die folgenden 5 Eigenschaften:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Ähnliche Abkürzungen dienen zum PR_SENT_REPRESENTING_\* und andere Gruppen mit Nachrichteneigenschaften.
  
|**SMTP-header**|**MAPI-Eigenschaft**|
|:-----|:-----|
|Von:  <br/> |Ausgehend: PR_SENDER_\*; Eingehend: PR_SENDER_\* und PR_SENT_REPRESENTING_\*  <br/> |
|Datum:  <br/> |Ausgehend: aktuelle Uhrzeit; Eingehende: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|An:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) für **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), auf dem MAPI_TO ist Empfänger  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, in denen **PR_RECIPIENT_TYPE** MAPI_CC ist  <br/> |
|Bcc:  <br/> |**PR_DISPLAY_NAME** und **PR_EMAIL_ADDRESS** für Empfänger, in denen **PR_RECIPIENT_TYPE** MAPI_BCC ist  <br/> |
|||
|Empfangen:  <br/> |Keine entsprechende MAPI-Eigenschaft; Lokaler Hostname und der Name der Komponente hier einfügen  <br/> |
|Zurückgeben des Empfangs auf:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Antwort an:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Betreff:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Keine bestimmte Länge Einschränkung.  <br/> |
|MIME-Version:  <br/> |Immer "1.0"  <br/> |
|||
|X-MS-Anlage:  <br/> |Für die Kompatibilität mit MS Mail SMTP-Gateway. _filename Größe mm-tt-Yyy Hh:mm_Details unten.  <br/> |
|||
| _gesamte SMTP-Nachrichtenumschlag_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|Kopfzeile Namen TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for Absender nur ._The TBDheader sollte verwendet werden, um festzustellen, ob der Absender TNEF-Inhalt in einer Antwort zu interpretieren ist.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Text/Plain oder Multipart/mixed. Siehe "Nachricht" Inhaltsabschnitt.  <br/> |
   
Der X-MS-Attachment-Header wird als vier Token, getrennt durch ein Leerzeichen formatiert:
  
 _Nennen Sie Größe Datum Uhrzeit_
  
Das erste Token lautet der Dateiname, der eingebettete Leerzeichen enthalten kann, sodass diese Kopfzeile aus der Recht auf eingehenden Nachrichten verarbeitet werden soll. Die Größe ist in Byte. das Datum wird als _mm-tt-jjjj,_ und die Uhrzeit als formatiert _hh: mm._
  
> [!NOTE]
> MessageID ist **PR_SEARCH_KEY** nicht, da die SMTP-Domäne spezifische Anforderungen für das Format des Bezeichners Nachricht seinerseits zum Codieren von einer beliebigen MAPI-ID unmöglich zugeordnet. Stattdessen wird MessageID **PR_TNEF_CORRELATION_KEY**zugeordnet. Diese Eigenschaft ist eine Transport definiert-Eigenschaft, die durch den Transport Senden ausgehender Nachrichten festgelegt und durch einen Transport eine eingehende Nachricht empfangen verwendet. Weitere Informationen finden Sie unter [Developing eines Transportdienstes TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  

