---
title: Empfänger Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437287"
---
# <a name="recipient-tables"></a>Empfänger Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Empfängertabelle enthält Informationen zu allen Empfängern einer Nachricht. Nachrichtenspeicher Anbieter implementieren Empfänger Tabellen und Clientanwendungen verwenden Sie. Clients greifen auf eine Empfängertabelle zu, indem Sie die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode aufrufen oder wenn der Nachrichtenspeicher Anbieter Sie unterstützt, an die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode. Clients greifen auf Empfänger Tabellen **** mit OpenProperty zu, indem Sie **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) für das Property-Tag und IID_IMAPITable für den Schnittstellenbezeichner angeben. Änderungen an einer Empfängertabelle können durch Aufrufen der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode erfolgen. 
  
Empfänger Tabellen haben unterschiedliche Spaltensätze, je nachdem, ob die Nachricht übermittelt wurde. Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Empfänger Tabellen:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([Pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([Pidtagrowid (](pidtagrowid-canonical-property.md))
    
Die optionalen Eigenschaften sind:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([Pidtagspoolerstatus (](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))
    
ÜberMittelte Nachrichten sollten diese zusätzlichen Eigenschaften in den erforderlichen Spaltensatz aufnehmen:
  
- **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([Pidtagresponsibility (](pidtagresponsibility-canonical-property.md))
    
Abhängig von der Implementierung eines Anbieters können zusätzliche Spalten wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [Entry](entryid.md)-out in der Tabelle enthalten sein.
  
Jeder Nachrichtenspeicher Anbieter, der die Nachrichtenübertragung unterstützt, wie in dem STORE_SUBMIT_OK-Bit angegeben, das in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Anbieters festgelegt ist, sollte Unterstützung für eine bestimmte Gruppe von Einschränkungen in einer Empfänger Tabellen Implementierung. Die **and**-, **or**-, exist-und Property-Einschränkungen gehören zu den Arten von Einschränkungen, die für Empfänger Tabellen Benutzer verfügbar sein sollten. Nur die Operatoren EQUAL und ungleich werden für die Eigenschaftseinschränkung unterstützt. Diese Einschränkungen müssen mit den folgenden Eigenschaften funktionieren:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

