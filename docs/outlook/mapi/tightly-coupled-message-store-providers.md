---
title: Eng gekoppelte Nachrichtenspeicher Anbieter
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
# <a name="tightly-coupled-message-store-providers"></a>Eng gekoppelte Nachrichtenspeicher Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtenspeicher Anbieter können eng mit einem Transportanbieter gekoppelt werden. Die enge Kopplung von MAPI-Dienstanbietern beinhaltet die Implementierung der beiden Anbieter, sodass der Informationsspeicher Anbieter und der Transportanbieter kommunizieren können, um das Senden und empfangen von Nachrichten effizienter zu gestalten. Der Vorteil besteht darin, dass die Leistungsverbesserungen dazu führen können, dass zwei Dienstanbieter direkt miteinander interagieren können und nicht über MAPI-Spooler. Um einen Nachrichtenspeicher Anbieter eng mit einem Transportanbieter zu koppeln, muss der Transportanbieter den Eintragsbezeichner des Nachrichtenspeicher Anbieters in der **PR_OWN_STORE_ENTRYID** ([pidtagownstoreentryid (](pidtagownstoreentryid-canonical-property.md))-Eigenschaft des Transportanbieters platzieren. Zeile in der MAPI-Statustabelle. Dadurch kann MAPI-Spooler den Speicheranbieter mit dem Transportanbieter verbinden.
  
Es ist nicht erforderlich, dass ein Nachrichtenspeicher Anbieter immer eng mit einem anderen Dienstanbieter verbunden wird. Der häufigste Dienstanbieter, der eng mit einem Nachrichtenspeicher Anbieter gekoppelt ist, ist ein Transportanbieter. Dies geschieht normalerweise, damit das Senden und empfangen von Nachrichten ohne Einbeziehung der MAPI-Spooler durchgeführt werden kann. Wenn der Benutzer beispielsweise eine ausgehende Nachricht sendet, kann er vom kombinierten Nachrichtenspeicher Anbieter und-Transportanbieter direkt gesendet werden. Die kombinierten Dienstanbieter müssen MAPI-Spooler nicht zuerst Benachrichtigen, dass eine neue Nachricht zur Verarbeitung vorhanden ist, und dann warten, bis MAPI-Spooler den Prozess der Übertragung der Nachricht vom Nachrichtenspeicher Anbieter an den Transportanbieter initiiert. Dies hat besondere Vorteile, wenn ein serverbasierter Nachrichtenspeicher verwendet wird, indem der Netzwerkdatenverkehr zwischen dem Computer des Benutzers und dem Server minimiert wird.
  
Im Allgemeinen gibt es keine genau festgelegten Verfahren für die enge Kopplung von Dienstanbietern. Sie sollten jedoch die folgenden Richtlinien verwenden:
  
- Wenn der Grund für die enge Kopplung von Dienstanbietern die Leistung ist, beachten Sie, dass die Kopplung Teile des MAPI-Subsystems aus den Prozessen abnimmt, an denen diese Teile normalerweise beteiligt wären. Dies impliziert, dass die einzelnen Teile des kombinierten Dienstanbieters miteinander interagieren sollen, um die Interaktion zu simulieren, die Sie normalerweise mit den Teilen des MAPI-Subsystems haben, die nicht verwendet werden.
    
- Wenn eng gekoppelte Dienstanbieter mit anderen MAPI-Komponenten interagieren, müssen Sie weiterhin mit ihnen interagieren, wenn Sie nicht eng gekoppelt wären. Wenn ein Benutzer beispielsweise einen kombinierten Nachrichtenspeicher Anbieter und-Transportanbieter als Standardnachrichtenspeicher verwendet, aber einen separaten Transportanbieter zum Senden von Nachrichten verwendet, kann dies passieren, wenn ein Benutzer einen Computer auf den Weg bringt und zu einem Remote Transport-PR wechselt. ovider – der Nachrichtenspeicher Teil des eng gekoppelten Dienstanbieters muss weiterhin mit dem MAPI-Spooler interagieren, als ob es sich um einen eigenständigen Nachrichtenspeicher Anbieter handelt.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

