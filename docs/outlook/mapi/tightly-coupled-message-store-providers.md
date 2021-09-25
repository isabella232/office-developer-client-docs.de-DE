---
title: Eng gekoppelte Nachrichtenanbieter Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9052228da750316c68f65d2489549d560ec0cc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578515"
---
# <a name="tightly-coupled-message-store-providers"></a>Eng gekoppelte Nachrichtenanbieter Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicheranbieter können eng mit einem Transportanbieter gekoppelt werden. Eine enge Verknüpfung von MAPI-Dienstanbietern bedeutet die Implementierung der beiden Anbieter, sodass der Speicheranbieter und der Transportanbieter kommunizieren können, um den Prozess des Sendens und Empfangens von Nachrichten effizienter zu gestalten. Dies hat den Vorteil, dass Leistungsverbesserungen auftreten können, wenn zwei Dienstanbieter direkt miteinander interagieren können, anstatt mithilfe von MAPI-Spooler. Um einen Nachrichtenspeicheranbieter eng mit einem Transportanbieter zu koppeln, muss der Transportanbieter den Eintragsbezeichner des Nachrichtenspeicheranbieters in der **Eigenschaft PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) in der Zeile des Transportanbieters in der MAPI-Statustabelle platzieren. Dadurch kann der MAPI-Spooler den Speicheranbieter mit dem Transportanbieter verbinden.
  
Es ist nicht erforderlich, dass ein Nachrichtenspeicheranbieter jemals eng mit einem anderen Dienstanbieter gekoppelt ist. Der häufigste Dienstanbieter, der eng mit einem Nachrichtenspeicheranbieter verbunden ist, ist ein Transportanbieter. Dies geschieht in der Regel so, dass das Senden und Empfangen von Nachrichten ohne Beteiligung des MAPI-Spoolers erreicht werden kann. Wenn der Benutzer beispielsweise eine ausgehende Nachricht sendet, können der kombinierte Nachrichtenspeicheranbieter und der Transportanbieter sie direkt senden. Die kombinierten Dienstanbieter müssen den MAPI-Spooler nicht zuerst benachrichtigen, dass eine neue Nachricht zu verarbeiten ist, und dann auf den MAPI-Spooler warten, um den Prozess der Übertragung der Nachricht vom Nachrichtenspeicheranbieter an den Transportanbieter zu initiieren. Dies hat besondere Vorteile, wenn ein serverbasierter Nachrichtenspeicher verwendet wird, indem der Netzwerkdatenverkehr zwischen dem Computer des Benutzers und dem Server minimiert wird.
  
Im Allgemeinen gibt es keine genau festgelegten Verfahren für Dienstanbieter, die eng gekoppelt sind. Sie sollten jedoch die folgenden Richtlinien verwenden:
  
- Wenn der Grund für eine enge Kopplung von Dienstanbietern die Leistung ist, beachten Sie, dass die Kopplung Teile des MAPI-Subsystems aus den Prozessen herausnimmt, an denen diese Teile normalerweise beteiligt sind. Dies bedeutet, dass die einzelnen Teile im kombinierten Dienstanbieter so miteinander interagieren sollten, dass die Interaktion simuliert wird, die sie normalerweise mit den Teilen des MAPI-Subsystems haben, die nicht verwendet werden.
    
- Wenn eng gekoppelte Dienstanbieter mit anderen MAPI-Komponenten interagieren, müssen sie trotzdem genau so mit ihnen interagieren, als wären sie nicht eng miteinander verbunden. Wenn ein Benutzer beispielsweise einen kombinierten Nachrichtenspeicheranbieter und einen Transportanbieter als Standardnachrichtenspeicher verwendet, aber einen separaten Transportanbieter verwendet, um Nachrichten zu senden , wie dies passieren kann, wenn ein Benutzer unterwegs einen Computer verwendet und zu einem Remotetransportanbieter wechselt, muss der Nachrichtenspeicherteil des eng gekoppelten Dienstanbieters weiterhin mit dem MAPI-Spooler interagieren, als wäre er ein eigenständiger Nachrichtenspeicheranbieter.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

