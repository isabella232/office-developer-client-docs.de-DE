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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299811"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Generieren und Verwenden von Eintragsbezeichnern für Nachrichtenspeicheranbieter

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein neuer Ordner oder eine Nachricht in einem Nachrichtenspeicher erstellt wird, muss der Nachrichtenspeicher Anbieter diesem Objekt eine Eintrags-ID zuweisen, damit Clientanwendungen darauf verweisen können. Nachrichtenspeicher Anbieter können die nicht mehr existierenden Eintrags-IDs von gelöschten Objekten oder neue Bezeichner wieder verwenden. Für Nachrichtenspeicher Anbieter gibt es keine oder eine andere Anforderung. Wenn es jedoch möglich ist, sollte ein Nachrichtenspeicher Anbieter immer neue langfristige Eintragsbezeichner für neue Objekte generieren, statt alte zu verwenden. Es ist in Ordnung, kurzfristige Eintrags-IDs wiederzuverwenden, wenn die Objekte, auf die Sie verweisen, gelöscht werden.
  
Der Grund für diesen Löschvorgang besteht darin, dass Clients Eingabe-IDs Zwischenspeichern können, manchmal über längere Zeiträume hinweg. Wenn dies der Fall ist und der Nachrichtenspeicher Anbieter Eingabe-IDs wieder verwendet, ist es möglich, dass die Eintrags-ID auf ein anderes Objekt verweist, wenn der Client die Eintrags-ID öffnet, als wenn der Eintragsbezeichner zum ersten mal abgerufen wurde. Wenn der Nachrichtenspeicher Anbieter Eintrags-IDs nicht wieder verwendet oder zumindest ein Generierungsschema für die Eintrags-ID, das für einen sehr langen Zeitraum nicht wiederholt wird, kann dieses Problem nicht auftreten.
  
Entsprechend sollten Nachrichtenspeicher Anbieter versuchen, Eintragsbezeichner für Ordner und Nachrichten beizubehalten, wenn Sie im Nachrichtenspeicher verschoben werden. Wenn der Nachrichtenspeicher Anbieter dies kann, werden Verweise auf Objekte im Speicher nicht ungültig, wenn das Objekt an einen anderen Speicherort im Speicher verschoben wird.
  
## <a name="see-also"></a>Siehe auch

- [Nachrichtenspeicher-Features](message-store-features.md)

