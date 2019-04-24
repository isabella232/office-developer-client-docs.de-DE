---
title: Erstellen und Speichern von Nachrichten in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7c923a330c542dff8b1bbc476461ccd21680a5b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332900"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Erstellen und Speichern von Nachrichten in Nachrichtenspeichern

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie Ihr Nachrichtenspeicheranbieter Nachrichten in dem zugrunde liegenden Speichermechanismus erstellt und speichert, ist im Wesentlichen von dem zugrunde liegenden Speichermechanismus selbst abhängig. Im Allgemeinen müssen Sie nur Code schreiben, um die Eigenschaften einer Nachricht und deren Werte zu speichern.
  
Wenn die Nachricht speichern Anbieter erstellt eine neue Nachricht, muss des Anbieters die Nachricht mit den erforderlichen Eigenschaften f�r Nachrichten zu erstellen. Eine Liste dieser Eigenschaften finden Sie in der Dokumentation f�r die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) Schnittstelle. Anschlie�end hinzuf�gen-Clientanwendungen alle zus�tzlichen Eigenschaften mit [IMAPIProp](imapipropiunknown.md) Methoden. 
  
Wenn die Nachricht speichern Anbieter speichert eine Nachricht an die zugrunde liegende Speichermechanismus, muss der Anbieter Eigenschaften der Meldung durchlaufen, und speichern Sie sie in der zugrunde liegende Speichermechanismus, so, dass sie vollst�ndig wiederhergestellt werden k�nnen, wenn die Nachricht sp�ter ge�ffnet wird.
  
MAPI erfordert, dass die Eigenschaften f�r [IMessage](imessageimapiprop.md) Schnittstellen durchgef�hrt werden, was bedeutet, dass �nderungen vorgenommen werden, bis die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, auf das Objekt "Message aufgerufen wird" nicht dauerhaft entfernt werden. Der Nachricht Speicheranbieter ist verantwortlich f�r die Implementierung dieses Verhalten. Dies ist in der Regel nicht schwierig. Es bedeutet ganz einfach Eigenschaften im Arbeitsspeicher gedr�ckt halten, w�hrend sie ge�ndert werden und deren Aufnahme in der zugrunde liegende Speichermechanismus, wenn **SaveChanges** aufgerufen wird. 
  
Einige Eigenschaften f�r Nachrichtenobjekte, die haben spezielle Semantik f�r Clientanwendungen in Bezug auf die **SaveChanges** -Methode, wie folgt: 
  
- Einige Eigenschaften sollten Lese-/Schreibzugriff haben, bevor **SaveChanges** aufgerufen wird, danach aber schreibgeschützt sein. **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) wird beispielsweise von der Clientanwendung festgelegt, die die Nachricht erstellt ( und verfügt daher über Lese-/Schreibzugriff), kann aber nach dem ersten Aufruf von **SaveChanges** nicht geändert werden.
    
- Einige Eigenschaften haben spezielle Beziehungen zu Eigenschaften in dem Ordner, in dem sie sich befinden, oder zu **IMAPIFolder**-Methoden. Die **PR_MESSAGE_FLAGS**-Eigenschaft weist beispielsweise eine Beziehung zu den Flags auf, die im [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)-Aufruf verwendet werden. 
    
- Einige Eigenschaften sind möglicherweise erst verfügbar, wenn **SaveChanges** zum ersten Mal aufgerufen wird. Die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft ist beispielsweise erst verfügbar, wenn **SaveChanges** aufgerufen wird. 
    
- Einige Eigenschaften können spezielle Beziehungen zu anderen Eigenschaften des Nachrichtenobjekts haben. Beispielsweise wird die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft in der Regel von der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in Nachrichtenspeicheranbietern abgeleitet, die Nachrichten im Rich Text Format unterstützen.
    
- Einige Eigenschaften werden von mehr als einem Objekttyp im Zusammenhang mit Nachrichtenspeicheranbietern verwendet. Beispielsweise ist die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft in Ordner- und Nachrichtenobjekten sowie in Nachrichtenspeicheranbietern erforderlich.
    
Es liegt in der Verantwortung des Nachrichtenspeicheranbieters, die korrekte Semantik für derartige Eigenschaften zu implementieren.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Nachrichten in Nachrichtenspeichern](implementing-messages-in-message-stores.md)

