---
title: Empfängertabellen
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
# <a name="recipient-tables"></a>Empfängertabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Empfängertabelle enthält Informationen zu allen Empfängern für eine Nachricht. Nachrichtenspeicheranbieter implementieren Empfängertabellen, und Clientanwendungen verwenden sie. Clients greifen auf eine Empfängertabelle zu, indem sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) aufrufen oder die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufrufen, wenn sie vom Nachrichtenspeicheranbieter unterstützt wird. Clients greifen mit **OpenProperty** auf Empfängertabellen zu, indem **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) für das Eigenschaftstag und IID_IMAPITable für den Schnittstellenbezeichner angeben. Änderungen an einer Empfängertabelle können durch Aufrufen der [IMessage::ModifyRecipients-Methode vorgenommen](imessage-modifyrecipients.md) werden. 
  
Empfängertabellen haben einen anderen Spaltensatz, je nachdem, ob die Nachricht übermittelt wurde. Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in Empfängertabellen zusammen:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Die optionalen Eigenschaften sind:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Übermittelte Nachrichten sollten die folgenden zusätzlichen Eigenschaften in ihren erforderlichen Spaltensatz enthalten:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Abhängig von der Implementierung eines Anbieters können zusätzliche Spalten wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [ENTRYID](entryid.md)in der Tabelle enthalten sein.
  
Jeder Nachrichtenspeicheranbieter, der die Nachrichtenübertragung unterstützt – wie durch das **STORE_SUBMIT_OK-Bit** angegeben, das in der PR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft des Anbieters festgelegt ist – sollte Unterstützung für bestimmte Einschränkungen in einer Empfängertabelle bieten. And , **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users. Nur die Operatoren equal und not equal müssen für die Eigenschaftseinschränkung unterstützt werden. Diese Einschränkungen müssen mit den folgenden Eigenschaften funktionieren:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

