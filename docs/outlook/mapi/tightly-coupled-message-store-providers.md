---
title: Eng gekoppelte Nachrichten Store Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c9996dad1e9aa8c291f1cd593d9651994d86141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413227"
---
# <a name="tightly-coupled-message-store-providers"></a>Eng gekoppelte Nachrichten Store Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter können eng mit einem Transportanbieter gekoppelt werden. Eine enge Kopplung von MAPI-Dienstanbietern bedeutet, dass die beiden Anbieter so implementieren werden, dass der Speicheranbieter und der Transportanbieter kommunizieren können, um den Prozess des Sendens und Empfangens von Nachrichten effizienter zu gestalten. Dies hat den Vorteil, dass Leistungsverbesserungen dazu führen können, dass zwei Dienstanbieter direkt und nicht über einen MAPI-Spooler miteinander interagieren können. Um einen Nachrichtenspeicheranbieter eng mit einem Transportanbieter zu paaren, muss der Transportanbieter die Eintrags-ID des Nachrichtenspeicheranbieters in der **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) -Eigenschaft in der Zeile des Transportanbieters in der #A0 platzieren. Dadurch kann der MAPI-Spooler den Speicheranbieter mit dem Transportanbieter verbinden.
  
Es ist nicht erforderlich, dass ein Nachrichtenspeicheranbieter jemals eng mit einem anderen Dienstanbieter gekoppelt ist. Der häufigste Dienstanbieter, der eng mit einem Nachrichtenspeicheranbieter gekoppelt wird, ist ein Transportanbieter. Dies geschieht in der Regel so, dass das Senden und Empfangen von Nachrichten ohne Einbindung des MAPI-Spoolers durchgeführt werden kann. Wenn der Benutzer beispielsweise eine ausgehende Nachricht sendet, können der kombinierte Nachrichtenspeicheranbieter und der Transportanbieter sie direkt senden. Die kombinierten Dienstanbieter müssen den MAPI-Spooler nicht zuerst benachrichtigen, dass eine neue Nachricht zu verarbeiten ist, und dann warten, bis der MAPI-Spooler den Prozess der Übertragung der Nachricht vom Nachrichtenspeicheranbieter an den Transportanbieter initiiert. Dies hat besondere Vorteile, wenn ein serverbasierter Nachrichtenspeicher verwendet wird, indem der Netzwerkdatenverkehr zwischen dem Computer des Benutzers und dem Server minimiert wird.
  
Im Allgemeinen gibt es keine genau angegebenen Verfahren für Dienstanbieter mit enger Kopplung. Sie sollten jedoch die folgenden Richtlinien verwenden:
  
- Wenn der Grund für eine enge Kopplung von Dienstanbietern die Leistung ist, beachten Sie, dass die Kopplung Teile des MAPI-Subsystems aus den Prozessen entfernt, an denen diese Teile normalerweise beteiligt wären. Dies impliziert, dass die einzelnen Teile des kombinierten Dienstanbieters so miteinander interagieren sollten, dass sie die Interaktion simulieren, die sie normalerweise mit den Teilen des MAPI-Subsystems haben würden, die nicht verwendet werden.
    
- Wenn eng gekoppelte Dienstanbieter mit anderen MAPI-Komponenten interagieren, müssen sie immer noch genau so mit ihnen interagieren, wie sie es tun würden, wenn sie nicht eng gekoppelt wären. Wenn ein Benutzer beispielsweise einen kombinierten Nachrichtenspeicheranbieter und einen Transportanbieter als Standardnachrichtenspeicher verwendet, aber einen separaten Transportanbieter zum Senden von Nachrichten verwendet – wie dies passieren kann, wenn ein Benutzer einen Computer unterwegs nimmt und zu einem Remotetransportanbieter wechselt –, muss der Nachrichtenspeicherteil des eng gekoppelten Dienstanbieters weiterhin mit dem MAPI-Spooler interagieren, als wäre er ein eigenständiger Nachrichtenspeicheranbieter.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

