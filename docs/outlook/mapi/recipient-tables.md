---
title: Empfänger Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795345"
---
# <a name="recipient-tables"></a>Empfänger Tabellen

  
  
**Betrifft**: Outlook 
  
Die Empfänger Tabelle enthält Informationen zu allen Empfängern für eine Nachricht. Nachricht Anbieter implementieren Empfänger Tabellen und Clientanwendungen verwenden. Clients tätigen eines Anrufs an die [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode zum Öffnen einer Empfänger Tabelle oder unterstützt, wenn die Nachricht vom Anbieter Speichern der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode. Clients Zugriff auf Empfänger Tabellen mit **OpenProperty** angeben **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) für die Eigenschaftentag und IID_IMAPITable für den Schnittstellenbezeichner. Änderungen, die einer Tabelle Empfänger können durch Aufrufen der Methode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) vorgenommen werden. 
  
Empfänger Tabellen ist eine andere Spalte festlegen, je nachdem, ob die Nachricht gesendet wurde. Die folgenden Eigenschaften bilden die erforderliche Spalte in Empfänger Tabellen festzulegen:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Die optionalen Eigenschaften sind:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Gesendete Nachrichten sollte diese zusätzlichen Eigenschaften in einen Satz erforderliche Spalte enthalten:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Je nach der Implementierung eines Anbieters möglicherweise zusätzliche Spalten, wie **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) und [ENTRYID](entryid.md), in der Tabelle.
  
Eine beliebige Nachricht Speicher-Anbieter, der Nachrichtenübermittlung unterstützt – wie das STORE_SUBMIT_OK Bit festgelegt wird, in der Anbieter **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft angegeben – bieten Unterstützung für eine bestimmte Gruppe von Einschränkungen in einer Implementierung eines Empfängers Tabelle. **Und**, **oder**, vorhanden, und Suchkriterien in Eigenschaft gehören zu den Arten von Einschränkungen, die an Empfänger Tabelle Benutzer verfügbar sein soll. Nur die Operatoren gleich und ungleich müssen in der eigenschaftseinschränkung unterstützt werden. Diese Einschränkung Zusammenarbeit müssen mit den folgenden Eigenschaften:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

