---
title: Eng gekoppelten Nachrichtenspeicher-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83ebb739302ca0e12604b9eaf854f273554826ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795724"
---
# <a name="tightly-coupled-message-store-providers"></a>Eng gekoppelten Nachrichtenspeicher-Anbieter

  
  
**Betrifft**: Outlook 
  
Nachricht Anbieter können eng mit eines Transportdienstes verknüpft sein. Wodurch eng MAPI Service Provider bedeutet, dass zwei Anbieter implementieren, beispielsweise, dass der Anbieter und Adressbuchhierarchie kommunizieren können, um das Senden und Empfangen von Nachrichten effizienter zu machen. Der Vorteil dabei ist, dass Leistungssteigerungen führen können, wenn zwei Dienstanbieter miteinander direkt und nicht über MAPI-Warteschlange interagieren können. Um eine Nachrichtenanbieter eng mit eines Transportdienstes gekoppelt, muss der Adressbuchhierarchie der Nachricht Informationsdienst Eintrags-ID in der Eigenschaft **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) in der Adressbuchhierarchie platziert. Zeile in der Tabelle MAPI-Status. Auf diese Weise MAPI-Warteschlange zum der Adressbuchhierarchie Speicheranbieter herstellen können.
  
Es ist nicht erforderlich, dass eine Nachricht Speicheranbieter jemals eng mit einem anderen Anbieter verknüpft sein. Der am häufigsten verwendete Dienstanbieter eng mit einem Nachrichtenanbieter gekoppelt ist eines Transportdienstes. Dies erfolgt normalerweise, sodass senden und Empfangen von Nachrichten ohne im Zusammenhang mit der MAPI-Warteschlange durchgeführt werden kann. Beispielsweise, wenn der Benutzer eine ausgehende Nachricht sendet, können der kombinierten Nachrichtenanbieter und Adressbuchhierarchie direkt senden. Die kombinierte-Dienstanbieter müssen nicht MAPI-Warteschlange zuerst zu benachrichtigen, dass eine neue Nachricht zu verarbeiten und warten Sie MAPI-Warteschlange die Übertragung der Nachricht vom Anbieter für die Nachricht an der Adressbuchhierarchie initiieren vorhanden ist. Dies hat bestimmte Vorteile, wenn ein serverbasierte Nachrichtenspeicher durch Minimierung des Netzwerkverkehrs zwischen dem Computer des Benutzers und dem Server verwendet wird.
  
Im Allgemeinen sind gibt es keine gut angegebenen Prozeduren für wodurch eng-Dienstanbieter. Sie sollten jedoch die folgenden Richtlinien verwenden:
  
- Ist der Grund für wodurch eng Dienstanbieter Leistung, beachten Sie, dass die Kopplung Teile des MAPI-Subsystems nicht genügend Prozesse annimmt, an denen die Teile normalerweise beteiligt werden würde. Dies bedeutet, dass die einzelnen Teile in der kombinierten Dienstanbieter miteinander in einer Weise interagieren soll, die die Interaktion simuliert, die sie normalerweise mit den Teilen der MAPI-Subsystems hätten, die nicht verwendet werden.
    
- Wenn eng gekoppelten-Dienstanbietern interagieren mit anderen Komponenten MAPI muss weiterhin Interaktion mit ihnen genau wie würden sie nicht eng verknüpft wurden. Beispielsweise, wenn ein Benutzer eine kombinierte Nachrichtenanbieter und Adressbuchhierarchie als ihren Standard-Nachrichtenspeicher verwendet, aber wird mithilfe ein separaten Transportdienstes zum Senden von Nachrichten – wie auftreten können, wenn ein Benutzer einen Computer auf Reisen hat und zu einer remote-Transport-Kurs wechselt Ovider – der Bereich Message Store des Dienstanbieters eng gekoppelten muss weiterhin mit MAPI-Warteschlange interagieren, als ob es sich um einen Anbieter für eigenständige Nachricht anmelden.
    
## <a name="see-also"></a>Siehe auch



[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

