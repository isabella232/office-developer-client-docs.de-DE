---
title: Empfängertabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fc71a5128796d74f06a896ad8b1bc2cdc153c060
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599151"
---
# <a name="recipient-tables"></a>Empfängertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Empfängertabelle enthält Informationen zu allen Empfängern einer Nachricht. Nachrichtenspeicheranbieter implementieren Empfängertabellen, und Clientanwendungen verwenden diese. Clients greifen auf eine Empfängertabelle zu, indem sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) aufrufen oder wenn der Nachrichtenspeicheranbieter sie unterstützt, an die [IMAPIProp::OpenProperty-Methode.](imapiprop-openproperty.md) Clients greifen mit **OpenProperty** auf Empfängertabellen zu, indem **sie PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) für das Eigenschaftentag und IID_IMAPITable für den Schnittstellenbezeichner angeben. Änderungen an einer Empfängertabelle können durch Aufrufen der [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) vorgenommen werden. 
  
Für Empfängertabellen wird eine andere Spalte festgelegt, je nachdem, ob die Nachricht übermittelt wurde. Die folgenden Eigenschaften bilden den erforderlichen Spaltensatz in Empfängertabellen:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Die optionalen Eigenschaften sind:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Gesendete Nachrichten sollten diese zusätzlichen Eigenschaften in ihrem erforderlichen Spaltensatz enthalten:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Abhängig von der Implementierung eines Anbieters befinden sich möglicherweise zusätzliche Spalten wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [ENTRYID](entryid.md)in der Tabelle.
  
Jeder Nachrichtenspeicheranbieter, der die Nachrichtenübertragung unterstützt – wie durch das STORE_SUBMIT_OK Bit angegeben wird, das in der **Eigenschaft PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) des Anbieters festgelegt wird – sollte Unterstützung für einen bestimmten Satz von Einschränkungen in einer Empfängertabellenimplementierung bieten. And , **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users. Nur die gleichen und nicht gleich operatoren müssen für die Eigenschaftseinschränkung unterstützt werden. Diese Einschränkungen müssen mit den folgenden Eigenschaften funktionieren:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

