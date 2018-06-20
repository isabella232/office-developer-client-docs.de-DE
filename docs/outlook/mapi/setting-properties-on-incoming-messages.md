---
title: Festlegen von Eigenschaften für eingehende Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6233afffd532c420ae170ae45b1bf93d6571865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795537"
---
# <a name="setting-properties-on-incoming-messages"></a>Festlegen von Eigenschaften für eingehende Nachrichten

  
  
**Betrifft**: Outlook 
  
Die Clientanwendungen innerhalb des MAPI-Subsystems erwarten eine Reihe von Eigenschaften in jeder empfangenen Nachricht. Wenn der Adressbuchhierarchie eine Nachricht im MAPI öffnet, sollte diese Eigenschaften seit dem ist der einzige Prozess mit den erforderlichen Informationen dazu, oder mindestens die beste Informationsquelle ist festgelegt werden.
  
Anbieter werden empfohlen, die Werte für alle diese Eigenschaften in eingehenden Nachrichten festzulegen.
  
|**Name der Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Der Betreff der Nachricht.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Nur-Text des Nachrichtentexts.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Komprimierte RTF Meldungstext.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Das Datum und die Zeit, die die Nachricht gesendet wurde.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Der Anzeigename des Nachrichtenabsenders angezeigt.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Das Adressbuch Adresseintrag des Nachrichtenabsenders angezeigt.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Die Adresse Adressbuch suchen-Taste des Nachrichtenabsenders angezeigt.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Die Zeit, die die Nachricht an die messaging-System von messaging-Client des Absenders übermittelt wurde.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Der Name des repräsentative Delegaten zum Senden.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Das Adressbuch Adresseintrag des sendenden Delegaten.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Die Adresse Adressbuch suchen-Taste des sendenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Der Name des repräsentative Delegaten für den Empfang.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Das Adressbuch Adresseintrag des empfangenden Delegaten.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Die Adresse Adressbuch suchen-Taste des empfangenden Delegaten.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Die Liste der delegierte Empfänger anzuzeigen, getrennt durch ein Semikolon und ein Leerzeichen (";").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Die Liste der delegierte Empfänger für eine Antwort.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Gibt an, dass der Empfänger speziell als Empfänger "zu" (nicht in einer Gruppe) mit dem Namen wurde.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger speziell als "cc"-Empfänger (nicht in einer Gruppe) mit dem Namen wurde.  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Gibt an, dass der Empfänger speziell als einen "an", mit dem Namen wurde "cc" und "Bcc-Empfänger (nicht in einer Gruppe).  <br/> |
   
Anbieter, die keine offensichtlichen Zuordnungen aufweisen können auf dieselben Werte wie der Gruppe der **PR_RCVD_REPRESENTING** Gruppe von Eigenschaften, die dieselben Werte wie die **PR_RECEIVED_BY **PR_SENDER** **PR_SENT_REPRESENTING** Gruppe von Eigenschaften festlegen. **gruppieren und **PR_REPLY_RECIPIENT** Gruppe von Eigenschaften basierend auf den Werten der Gruppe der **PR_SENDER** erstellen können. Beispielsweise kann **PR_SENT_REPRESENTING_NAME** auf den gleichen Wert wie **PR_SENDER_NAME**festgelegt werden.
  
Die Eigenschaft **PR_ENTRYID** oder **PR_ENTRYLIST** kann, falls erforderlich, generiert werden durch Aufrufen der [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) -Methode. **PR_SEARCH_KEY** Gruppe von Eigenschaften kann durch Verketten der **PR_ADDRTYPE** Eigenschaft im Zusammenhang mit einem Benutzer, einen Doppelpunkt (:)) und die **PR_EMAIL_ADDRESS** Eigenschaft im Zusammenhang mit dem Benutzer generiert werden und das Ergebnis in Großbuchstaben ändern . Die Windows-API-Funktion **CharUpperBuff** ist eine praktische Funktion, die für diesen Zweck verwendet. Dieser Vorgang wird, stellen Sie eine kanonische Form der Adresse, die als eine binäre Menge verglichen werden können. Beachten Sie, dass dies nicht erforderlich ist, wenn der Adressbuchhierarchie in Bezug auf e-Mail-Adressen Groß-/Kleinschreibung beachtet. 
  

