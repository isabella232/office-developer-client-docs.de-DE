---
title: Festlegen von Eigenschaften für eingehende Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432695"
---
# <a name="setting-properties-on-incoming-messages"></a>Festlegen von Eigenschaften für eingehende Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Clientanwendungen im MAPI-Subsystem erwarten eine Reihe von Eigenschaften in jeder empfangenen Nachricht. Wenn der Transportanbieter eine Nachricht in mapI einsenn, sollte er diese Eigenschaften festlegen, da er entweder der einzige Prozess mit den erforderlichen Informationen ist oder zumindest die beste Informationsquelle ist.
  
Anbieter werden aufgefordert, die Werte für alle diese Eigenschaften in eingehenden Nachrichten zu setzen.
  
|**Eigenschaftsname**|**Beschreibung**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Der Betreff der Nachricht.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Nur-Text-Nachrichtentext.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Komprimierter RTF-Nachrichtentext.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Das Datum und die Uhrzeit, zu der die Nachricht zugestellt wurde.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Der Anzeigename des Nachrichtenherkunftsgebers.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des Nachrichtenherkunftsgebers.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Der Adressbuchsuchschlüssel des Nachrichtenherkunftsgebers.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Der Zeitpunkt, zu dem die Nachricht vom Messagingclient des Absenders an das Messagingsystem übermittelt wurde.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Der Name der repräsentativen Stellvertretung für das Senden.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des sendenden Stellvertreters.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Der Adressbuchsuchschlüssel des sendenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Der Name der repräsentativen Stellvertretung für den Empfang.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Der Adressbucheintrag der empfangenden Stellvertretung.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Der Adressbuchsuchschlüssel des empfangenden Stellvertreters.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Die Liste der delegierten Empfängeranzeigenamen, getrennt durch ein Semikolon und Leerzeichen ("; ").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Die Liste der delegierten Empfänger für eine Antwort.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "an"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "cc"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "to", "cc" oder "bcc" (nicht in einer Gruppe) benannt wurde.  <br/> |
   
Anbieter ohne offensichtliche Zuordnungen können die **PR_SENT_REPRESENTING-Gruppe** von Eigenschaften auf die gleichen Werte wie die **PR_SENDER-Gruppe,** die **PR_RCVD_REPRESENTING-Gruppe** von Eigenschaften auf die gleichen Werte wie die **PR_RECEIVED_BY-Gruppe** festlegen und die **PR_REPLY_RECIPIENT-Gruppe** von Eigenschaften basierend auf den Werten der **PR_SENDER-Gruppe** erstellen. Beispielsweise kann **PR_SENT_REPRESENTING_NAME** auf denselben Wert wie bei **PR_SENDER_NAME.**
  
Die **PR_ENTRYID** oder **PR_ENTRYLIST-Eigenschaft** kann bei Bedarf durch Aufrufen der [IMAPISupport::CreateOneOff-Methode generiert](imapisupport-createoneoff.md) werden. Die **PR_SEARCH_KEY-Gruppe** von Eigenschaften kann generiert werden, indem die einem Benutzer zugeordnete **PR_ADDRTYPE-Eigenschaft,** ein Doppelpunkt (:)) und die dem Benutzer zugeordnete **PR_EMAIL_ADDRESS-Eigenschaft** verkettt und dann das Ergebnis in Großbuchstaben geändert wird. Die Windows-API-Funktion **CharUpperBuff** ist eine bequeme Funktion, die sie zu diesem Zweck verwenden kann. Bei diesem Prozess ist es erforderlich, eine kanonische Form der Adresse zu erstellen, die als binäre Menge verglichen werden kann. Beachten Sie, dass dies nicht erforderlich ist, wenn beim Transportanbieter bei E-Mail-Adressen die Kleinschreibung beachtet wird. 
  

