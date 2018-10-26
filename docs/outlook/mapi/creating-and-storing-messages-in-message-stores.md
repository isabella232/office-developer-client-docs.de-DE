---
title: Erstellen und Speichern von Nachrichten in Nachrichtenspeichern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589175"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Erstellen und Speichern von Nachrichten in Nachrichtenspeichern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie Ihr Nachrichtenspeicheranbieter Nachrichten in dem zugrunde liegenden Speichermechanismus erstellt und speichert, ist im Wesentlichen von dem zugrunde liegenden Speichermechanismus selbst abhängig. Im Allgemeinen müssen Sie nur Code schreiben, um die Eigenschaften einer Nachricht und deren Werte zu speichern.
  
Wenn der Nachrichtenspeicheranbieter eine neue Nachricht erstellt, muss der Anbieter die Nachricht mit den erforderlichen Eigenschaften für Nachrichten erstellen. Eine Liste dieser Eigenschaften ist in der Dokumentation für die [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)-Schnittstelle zu finden. Danach fügen Clientanwendungen weitere Eigenschaften mit [IMAPIProp](imapipropiunknown.md)-Methoden hinzu. 
  
Wenn der Nachrichtenspeicheranbieter eine Nachricht im zugrunde liegenden Speichermechanismus speichert, muss der Anbieter die Eigenschaften der Nachricht durchlaufen und diese im zugrunde liegenden Speichermechanismus speichern, damit diese vollständig wiederhergestellt werden können, wenn die Nachricht später geöffnet wird.
  
MAPI erfordert, dass die Eigenschaften in [IMessage](imessageimapiprop.md)-Schnittstellen abgewickelt werden, was bedeutet, dass daran vorgenommene Änderungen erst dauerhaft sind, wenn die [IMAPIProp::SaveChanges](imapiprop-savechanges.md)-Methode im Nachrichtenobjekt aufgerufen wird. Der Nachrichtenspeicheranbieter ist für das Implementieren dieses Verhaltens verantwortlich. Dies ist in der Regel nicht schwierig. Es bedeutet einfach, dass Eigenschaften im Arbeitsspeicher gehalten werden, während sie geändert werden, und dass sie im zugrunde liegenden Speichermechanismus gespeichert werden, wenn **SaveChanges** aufgerufen wird. 
  
Einige Eigenschaften in Nachrichtenobjekten haben bezüglich der **SaveChanges**-Methode eine besondere Semantik für Clientanwendungen: 
  
- Einige Eigenschaften sollten Lese-/Schreibzugriff haben, bevor **SaveChanges** aufgerufen wird, danach aber schreibgeschützt sein. **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) wird beispielsweise von der Clientanwendung festgelegt, die die Nachricht erstellt ( und verfügt daher über Lese-/Schreibzugriff), kann aber nach dem ersten Aufruf von **SaveChanges** nicht geändert werden.
    
- Einige Eigenschaften haben spezielle Beziehungen zu Eigenschaften in dem Ordner, in dem sie sich befinden, oder zu **IMAPIFolder**-Methoden. Die **PR_MESSAGE_FLAGS**-Eigenschaft weist beispielsweise eine Beziehung zu den Flags auf, die im [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)-Aufruf verwendet werden. 
    
- Einige Eigenschaften sind möglicherweise erst verfügbar, wenn **SaveChanges** zum ersten Mal aufgerufen wird. Die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft ist beispielsweise erst verfügbar, wenn **SaveChanges** aufgerufen wird. 
    
- Einige Eigenschaften können spezielle Beziehungen zu anderen Eigenschaften des Nachrichtenobjekts haben. Beispielsweise wird die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft in der Regel von der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in Nachrichtenspeicheranbietern abgeleitet, die Nachrichten im Rich Text Format unterstützen.
    
- Einige Eigenschaften werden von mehr als einem Objekttyp im Zusammenhang mit Nachrichtenspeicheranbietern verwendet. Beispielsweise ist die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft in Ordner- und Nachrichtenobjekten sowie in Nachrichtenspeicheranbietern erforderlich.
    
Es liegt in der Verantwortung des Nachrichtenspeicheranbieters, die korrekte Semantik für derartige Eigenschaften zu implementieren.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Nachrichten in Nachrichtenspeichern](implementing-messages-in-message-stores.md)

