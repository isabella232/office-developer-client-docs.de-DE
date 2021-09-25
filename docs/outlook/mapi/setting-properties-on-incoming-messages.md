---
title: Festlegen von Eigenschaften für eingehende Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c7cf42cb4e034993347785697f9bc0719c925b22
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591157"
---
# <a name="setting-properties-on-incoming-messages"></a>Festlegen von Eigenschaften für eingehende Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Clientanwendungen innerhalb des MAPI-Subsystems erwarten eine Reihe von Eigenschaften in jeder empfangenen Nachricht. Wenn der Transportanbieter eine Nachricht in die MAPI einfügt, sollte er diese Eigenschaften festlegen, da es sich entweder um den einzigen Prozess mit den erforderlichen Informationen handelt oder zumindest die beste Quelle der Informationen ist.
  
Anbieter werden empfohlen, die Werte für alle diese Eigenschaften in eingehenden Nachrichten festzulegen.
  
|**Eigenschaftsname**|**Beschreibung**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Der Betreff der Nachricht.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Nur-Text-Nachrichtentext.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Komprimierter RTF-Nachrichtentext.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Datum und Uhrzeit der Zustellung der Nachricht.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Der Anzeigename des Nachrichtenursprungsgebers.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des Absenders der Nachricht.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Der Adressbuchsuchschlüssel des Nachrichtenursprungsgebers.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Der Zeitpunkt, zu dem die Nachricht vom Nachrichtenclient des Absenders an das Nachrichtensystem übermittelt wurde.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Der Name der repräsentativen Stellvertretung für das Senden.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des sendenden Delegaten.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Der Adressbuchsuchschlüssel des sendenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Der Name der repräsentativen Stellvertretung für den Empfang.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des empfangenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Der Adressbuchsuchschlüssel des empfangenden Delegaten.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Die Liste der delegierten Empfängeranzeigenamen, getrennt durch ein Semikolon und Leerzeichen ("; ").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Die Liste der delegierten Empfänger für eine Antwort.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Gibt an, dass der Empfänger explizit als "an"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "cc"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger explizit als "an", "cc" oder "bcc" (nicht in einer Gruppe) benannt wurde.  <br/> |
   
Anbieter, die keine offensichtlichen Zuordnungen haben, können die **PR_SENT_REPRESENTING** Gruppe von Eigenschaften auf dieselben Werte wie die **PR_SENDER** Gruppe, die **PR_RCVD_REPRESENTING** Gruppe von Eigenschaften auf dieselben Werte wie die **PR_RECEIVED_BY** Gruppe festlegen und die **PR_REPLY_RECIPIENT** Gruppe von Eigenschaften basierend auf den Werten der **PR_SENDER** Gruppe erstellen. Beispielsweise können **PR_SENT_REPRESENTING_NAME** auf denselben Wert wie **PR_SENDER_NAME** festgelegt werden.
  
Die **PR_ENTRYID-** oder **PR_ENTRYLIST-Eigenschaft** kann bei Bedarf durch Aufrufen der [IMAPISupport::CreateOneOff-Methode](imapisupport-createoneoff.md) generiert werden. Die **PR_SEARCH_KEY** Gruppe von Eigenschaften kann durch Verketten der **PR_ADDRTYPE** Einem Benutzer zugeordneten Eigenschaft, eines Doppelpunkts (:) und der **PR_EMAIL_ADDRESS** dem Benutzer zugeordneten Eigenschaft generiert werden, und das Ergebnis wird dann in Großbuchstaben geändert. Die Windows API-Funktion **CharUpperBuff** ist eine praktische Funktion für diesen Zweck. Bei diesem Vorgang ist es erforderlich, eine kanonische Form der Adresse zu erstellen, die als binäre Menge verglichen werden kann. Beachten Sie, dass dies nicht erforderlich ist, wenn beim Transportanbieter die Groß-/Kleinschreibung in Bezug auf E-Mail-Adressen beachtet wird. 
  

