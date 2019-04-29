---
title: Langfristige EintragsBezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409223"
---
# <a name="long-term-entry-identifiers"></a>Langfristige EintragsBezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein langfristiger Eintragsbezeichner wird einem Objekt von einem Dienstanbieter zugewiesen, wenn für ein Objekt ein Bezeichner mit einer längeren Lebensdauer erforderlich ist. Langfristige Eintrags-IDs sind immer für Wochen oder Monate gültig und können auf anderen Arbeitsstationen abhängig vom Anbieter gültig sein. Die langfristigen Bezeichner, die von Adressbuch Anbietern für benutzerdefinierte Empfänger erstellt wurden, sind universell gültig. 
  
Langfristige Eintrags-IDs werden Nachrichten speichern, Ordnern, Nachrichten, Adressbuch Containern, Messaging Benutzern und Verteilerlisten zugewiesen. Wenn Clientanwendungen die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode dieser Objekte aufrufen, wird immer eine langfristige Eintrags-ID zurückgegeben. 
  
Langfristige Eintrags-IDs müssen für alle Nachrichtenspeicher im aktiven Profil eindeutig sein. Wenn eine Nachricht oder ein Ordner aus einem Nachrichtenspeicher in einen anderen kopiert wird, muss daher eine neue Eintrags-ID zugewiesen werden. Wenn ein Nachrichtenspeicherobjekt verschoben wird, bestimmt der Nachrichtenspeicher Anbieter, der die Verschiebung implementiert, ob der ursprüngliche Eintragsbezeichner gültig bleibt. Einige Dienstanbieter weisen verschobene Objekte neue Eintrags-IDs zu; andere nicht. Wenn eine Änderung vorliegt, wird die neue Eintrags-ID in die Informationen eingeschlossen, die an Clients übergeben werden, wenn Sie über die Verschiebung benachrichtigt werden. 
  
In der Regel implementieren Nachrichtenspeicher Anbieter beim Verschieben von Ordnern das folgende Verhalten:
  
- Wenn ein Ordner aus einem Nachrichtenspeicher in einen anderen Speicher eines anderen Typs verschoben wird, wird die Eintrags-ID garantiert geändert.
    
- Wenn ein Ordner aus einem Nachrichtenspeicher in einen anderen Speicher desselben Typs verschoben wird, ändert sich die Eintrags-ID fast immer.
    
- Wenn ein Ordner an einen anderen Speicherort innerhalb desselben Nachrichtenspeichers verschoben wird, ändert sich möglicherweise die Eintrags-ID je nach Nachrichtenspeicher Anbieter.
    
Wenn Sie einen Ordner umbenennen, ohne den übergeordneten Ordner zu ändern, wird der Eintragsbezeichner in der Regel nicht geändert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintrags-IDs](mapi-entry-identifiers.md)

