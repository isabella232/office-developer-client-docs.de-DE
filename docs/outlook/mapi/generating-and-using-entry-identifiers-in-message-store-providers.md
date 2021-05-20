---
title: Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437679"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein neuer Ordner oder eine neue Nachricht in einem Nachrichtenspeicher erstellt wird, muss der Nachrichtenspeicheranbieter diesem Objekt einen Eintragsbezeichner zuweisen, damit Clientanwendungen darauf verweisen können. Nachrichtenspeicheranbieter können entweder die nicht mehr vorhandenen langfristigen Eintragsbezeichner gelöschter Objekte wiederverwenden oder neue Bezeichner erstellen. Für Nachrichtenspeicheranbieter gibt es keine Anforderung. Wenn dies jedoch möglich ist, sollte ein Nachrichtenspeicheranbieter immer neue langfristige Eintragsbezeichner für neue Objekte generieren, anstatt alte wieder zu verwenden. Es ist in Ordnung, kurzfristige Eintragsbezeichner wiederzuverwenden, wenn die Objekte, auf die sie verweisen, gelöscht werden.
  
Der Grund für diesen Löschvorgang ist, dass Clients Eintragsbezeichner zwischenspeichern können, manchmal über einen längeren Zeitraum. Wenn dies der Fall ist und der Nachrichtenspeicheranbieter eintragsbezeichner wiederverwendet, kann der Eintragsbezeichner auf ein anderes Objekt verweisen, wenn der Client den Eintragsbezeichner öffnet als beim ersten Erhalten der Eintrags-ID. Wenn der Nachrichtenspeicheranbieter keine Eintragsbezeichner wiederverwendet oder zumindest ein Schema zur Generierung von Eintragsbezeichnern verwendet, das sich nicht sehr lange wiederholt, kann dieses Problem nicht auftreten.
  
Auf ähnliche Weise sollten Nachrichtenspeicheranbieter versuchen, die Eintragsbezeichner für Ordner und Nachrichten zu erhalten, wenn sie im Nachrichtenspeicher verschoben werden. Wenn der Nachrichtenspeicheranbieter dies tun kann, werden Verweise auf Objekte im Speicher nicht ungültig, wenn das Objekt an einen anderen Speicherort im Speicher verschoben wird.
  
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

