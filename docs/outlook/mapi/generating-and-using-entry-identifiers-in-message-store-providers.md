---
title: Generieren und Verwenden von Eintragsbezeichner in Nachricht speichern-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 10634305130b0f465482cce025018d4929350513
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565452"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Generieren und Verwenden von Eintragsbezeichner in Nachricht speichern-Anbieter

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einen neuen Ordner oder Nachricht in einem Nachrichtenspeicher erstellt wird, hat der Nachricht Speicheranbieter dieses Objekt eines Eintrags-ID zugewiesen, sodass Clientanwendungen darauf verweisen können. Nachricht-Anbieter können die außer Kraft gesetzten langfristige-Eintragsbezeichner von gelöschten Objekten wiederverwenden oder erstellen neue IDs. Es gibt keine Anforderung unidirektional oder das andere für die Nachricht-Anbieter. jedoch, wenn es möglich ist, sollte eine Nachricht Speicheranbieter immer neue langfristige Eintragsbezeichner für neue Objekte, sondern Wiederverwenden von alten generieren. Es ist kein Problem kurzfristige-Eintragsbezeichner wiederverwendet, wenn die Objekte, denen sie referenzieren gelöscht werden.
  
Der Grund für diese Löschung ist, dass Clients Eintragsbezeichner, manchmal für längere Zeit zwischengespeichert werden können. Wenn in diesem Fall der Nachricht Speicheranbieter Eintragsbezeichner wiederverwenden, ist es möglich, für die Eintrags-ID für ein anderes Objekt zu verweisen, wenn der Client die Eintrags-ID öffnet, als wenn es zuerst die Eintrags-ID abgerufen. Wenn die Nachricht Informationsdienst nicht Eintragsbezeichner wieder verwenden – oder mindestens ein Eintrag Bezeichner Generation Schema verwendet, die nicht sehr lange wiederholt wird – dieses Problem kann nicht ausgeführt werden.
  
In ähnlicher Weise sollten Nachricht Anbieter Eintragsbezeichner für Ordner und Nachrichten beibehalten, wenn sie im Nachrichtenspeicher verschoben werden. Wenn der Nachricht Speicheranbieter dies möglich ist, werden Verweise auf Objekte im Speicher nicht ungültig, wenn das Objekt an eine andere Position im Speicher verschoben wird.
  
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

