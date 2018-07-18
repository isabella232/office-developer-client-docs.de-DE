---
title: Erstellen und Speichern von Nachrichten in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 32cfae36fb519654c1fb92d2f3b688c966f9288f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791485"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Erstellen und Speichern von Nachrichten in Nachrichtenspeicher

  
  
**Betrifft**: Outlook 
  
Wie Ihre Nachricht Speicheranbieter erstellt und speichert Nachrichten in der zugrunde liegende Speichermechanismus h�ngt stark von der zugrunde liegende Speichermechanismus selbst. Im Allgemeinen m�ssen Sie nur Code schreiben, um die Eigenschaften einer Nachricht und deren Werte beibehalten.
  
Wenn die Nachricht speichern Anbieter erstellt eine neue Nachricht, muss des Anbieters die Nachricht mit den erforderlichen Eigenschaften f�r Nachrichten zu erstellen. Eine Liste dieser Eigenschaften finden Sie in der Dokumentation f�r die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) Schnittstelle. Anschlie�end hinzuf�gen-Clientanwendungen alle zus�tzlichen Eigenschaften mit [IMAPIProp](imapipropiunknown.md) Methoden. 
  
Wenn die Nachricht speichern Anbieter speichert eine Nachricht an die zugrunde liegende Speichermechanismus, muss der Anbieter Eigenschaften der Meldung durchlaufen, und speichern Sie sie in der zugrunde liegende Speichermechanismus, so, dass sie vollst�ndig wiederhergestellt werden k�nnen, wenn die Nachricht sp�ter ge�ffnet wird.
  
MAPI erfordert, dass die Eigenschaften f�r [IMessage](imessageimapiprop.md) Schnittstellen durchgef�hrt werden, was bedeutet, dass �nderungen vorgenommen werden, bis die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, auf das Objekt "Message aufgerufen wird" nicht dauerhaft entfernt werden. Der Nachricht Speicheranbieter ist verantwortlich f�r die Implementierung dieses Verhalten. Dies ist in der Regel nicht schwierig. Es bedeutet ganz einfach Eigenschaften im Arbeitsspeicher gedr�ckt halten, w�hrend sie ge�ndert werden und deren Aufnahme in der zugrunde liegende Speichermechanismus, wenn **SaveChanges** aufgerufen wird. 
  
Einige Eigenschaften f�r Nachrichtenobjekte, die haben spezielle Semantik f�r Clientanwendungen in Bezug auf die **SaveChanges** -Methode, wie folgt: 
  
- Einige Eigenschaften sollte Lese-/Schreibzugriff, bevor **SaveChanges**, aber schreibgesch�tzt danach aufgerufen wird. Beispielsweise **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) zunächst von der Clientanwendung, die die Nachricht erstellt (und somit besteht Lese-/Schreibzugriff) festgelegt ist, aber nicht nach dem ersten Aufruf von **SaveChanges**geändert werden.
    
- Einige Eigenschaften haben spezielle Beziehungen zu Eigenschaften f�r den Ordner, den sie in oder **IMAPIFolder** Methoden sind. Beispielsweise bezieht sich die **PR_MESSAGE_FLAGS** -Eigenschaft auf die Kennzeichen f�r den Anruf [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) verwendet. 
    
- Einige Eigenschaften m�glicherweise nicht verf�gbar, bis **SaveChanges** zum ersten Mal aufgerufen wird. Zum Beispiel die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) möglicherweise nicht zur Verfügung, bis **SaveChanges** aufgerufen wird. 
    
- Einige Eigenschaften haben besondere Beziehungen mit anderen Eigenschaften auf Message-Objekts. Beispielsweise wird die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft in der Regel aus der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) in der Nachricht Anbieter abgeleitet, die Nachrichten im Rich Text Format unterstützen.
    
- Einige Eigenschaften werden von mehr als eine Objekttyp im Zusammenhang mit e-Mail-Speicher verwendet. Beispielsweise ist die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft auf den Ordner und die Nachricht, dass Objekte sowie Nachricht Speichern von Objekten erforderlich.
    
Es ist Aufgabe des Anbieters Nachricht an die richtige Semantik f�r solche Eigenschaften implementieren.
  
## <a name="see-also"></a>Siehe auch



[Implementieren von Nachrichten in Nachrichtenspeicher](implementing-messages-in-message-stores.md)

