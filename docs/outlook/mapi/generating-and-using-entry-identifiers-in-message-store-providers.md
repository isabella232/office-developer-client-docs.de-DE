---
title: Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6d5cc5899c911e3fbf9e47746d223ba6b5150130
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580202"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein neuer Ordner oder eine neue Nachricht in einem Nachrichtenspeicher erstellt wird, muss der Nachrichtenspeicheranbieter diesem Objekt einen Eintragsbezeichner zuweisen, damit Clientanwendungen darauf verweisen können. Nachrichtenspeicheranbieter können entweder die nicht mehr verwendeten langfristigen Eintragsbezeichner gelöschter Objekte wiederverwenden oder neue Bezeichner erstellen. Für Nachrichtenspeicheranbieter gibt es keine oder die andere Anforderung. Wenn dies jedoch machbar ist, sollte ein Nachrichtenspeicheranbieter immer neue langfristige Eintragsbezeichner für neue Objekte generieren, anstatt alte wiederzuverwenden. Es ist in Ordnung, kurzfristige Eintragsbezeichner wiederzuverwenden, wenn die Objekte, auf die sie sich beziehen, gelöscht werden.
  
Der Grund für diesen Löschvorgang ist, dass Clients Eintragsbezeichner zwischenspeichern können, manchmal über einen längeren Zeitraum. Wenn dies geschieht und der Nachrichtenspeicheranbieter Eintragsbezeichner wiederverwendet, kann der Eintragsbezeichner auf ein anderes Objekt verweisen, wenn der Client den Eintragsbezeichner öffnet als beim ersten Abrufen des Eintragsbezeichners. Wenn der Nachrichtenspeicheranbieter Eintragsbezeichner nicht wiederverwendet oder zumindest ein Eintrags-Id-Generierungsschema verwendet, das sich nicht sehr lange wiederholt, kann dieses Problem nicht auftreten.
  
Ebenso sollten Nachrichtenspeicheranbieter versuchen, Eintragsbezeichner für Ordner und Nachrichten beizubehalten, wenn sie in den Nachrichtenspeicher verschoben werden. Wenn der Nachrichtenspeicheranbieter dies tun kann, werden Verweise auf Objekte im Speicher nicht ungültig, wenn das Objekt an einen anderen Speicherort im Speicher verschoben wird.
  
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

