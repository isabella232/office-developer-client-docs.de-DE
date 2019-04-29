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
  
Die Clientanwendungen innerhalb des MAPI-Subsystems erwarten eine Reihe von Eigenschaften in einer empfangenen Nachricht. Wenn der Transportanbieter eine Nachricht in MAPI eingibt, sollte diese Eigenschaft festgelegt werden, da Sie entweder der einzige Prozess mit den erforderlichen Informationen ist oder zumindest die beste Quelle für die Informationen ist.
  
Anbieter werden dazu ermutigt, die Werte für alle diese Eigenschaften in eingehenden Nachrichten festzulegen.
  
|**Eigenschaftsname**|**Beschreibung**|
|:-----|:-----|
|**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Der Betreff der Nachricht.  <br/> |
|**PR_BODY** ([Pidtagbody (](pidtagbody-canonical-property.md))  <br/> |Nur-Text-Nachrichtentext.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Komprimierter RTF-Nachrichtentext.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Datum und Uhrzeit der Zustellung der Nachricht.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Der Anzeigename des Nachrichten Erstellers.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des Nachrichten Erstellers.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([Pidtagsendersearchkey (](pidtagsendersearchkey-canonical-property.md))  <br/> |Der Suchschlüssel des Adressbuchs des Nachrichten Erstellers.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Der Zeitpunkt, zu dem die Nachricht vom Messaging Client des Absenders an das Messagingsystem gesendet wurde.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Der Name des Stellvertreters für das Senden.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([Pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Der Adressbucheintrag der sendenden Stellvertretung.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([Pidtagsentrepresentingsearchkey (](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Der Suchschlüssel des Adressbuchs des sendenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Der Name des Stellvertreters für den Empfang.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Der Adressbucheintrag des empfangenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([Pidtagreceivedrepresentingsearchkey (](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Der Suchschlüssel des Adressbuchs des empfangenden Delegaten.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([Pidtagreplyrecipientnames (](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Die Liste der angezeigten Namen des Delegierten Empfängers, getrennt durch ein Semikolon und Leerzeichen (";").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([Pidtagreplyrecipiententries (](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Die Liste der Delegierten Empfänger für eine Antwort.  <br/> |
|**PR_MESSAGE_TO_ME** ([Pidtagmessagetome (](pidtagmessagetome-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "an"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "CC"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
|**PR_MESSAGE_RECIP_ME** ([Pidtagmessagerecipientme (](pidtagmessagerecipientme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger ausdrücklich als "an", "CC" oder "Bcc"-Empfänger (nicht in einer Gruppe) benannt wurde.  <br/> |
   
Anbieter, die über keine offensichtlichen Zuordnungen verfügen, können die **PR_SENT_REPRESENTING** -Gruppe von Eigenschaften auf dieselben Werte wie die **PR_SENDER** -Gruppe, die **PR_RCVD_REPRESENTING** -Gruppe von Eigenschaften auf dieselben Werte wie die PR_RECEIVED_BY festlegen. ** **Gruppe und kann die **PR_REPLY_RECIPIENT** -Eigenschaftengruppe basierend auf den Werten der **PR_SENDER** -Gruppe erstellen. **PR_SENT_REPRESENTING_NAME** kann beispielsweise auf den gleichen Wert wie **PR_SENDER_NAME**festgelegt werden.
  
Die **PR_ENTRYID** -oder **PR_ENTRYLIST** -Eigenschaft kann, falls erforderlich, durch Aufrufen der [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) -Methode generiert werden. Die **PR_SEARCH_KEY** -Gruppe von Eigenschaften kann generiert werden, indem die **PR_ADDRTYPE** -Eigenschaft, die einem Benutzer zugeordnet ist, ein Doppelpunkt (:) und die **PR_EMAIL_ADDRESS** -Eigenschaft, die dem Benutzer zugeordnet ist, und anschließend das Ergebnis in Großbuchstaben geändert werden. . Die Windows-API-Funktion **CharUpperBuff** ist eine praktische Funktion, die für diesen Zweck verwendet werden kann. Dieses Verfahren erfordert eine kanonische Form der Adresse, die als binäre Menge verglichen werden kann. Beachten Sie, dass dies nicht erforderlich ist, wenn der Transportanbieter in Bezug auf e-Mail-Adressen die Groß-/Kleinschreibung beachtet. 
  

