---
title: Long-Term Entry Identifiers
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
# <a name="long-term-entry-identifiers"></a>Long-Term Entry Identifiers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Dienstanbieter wird einem Objekt eine langfristige Eintrags-ID zugewiesen, wenn für ein Objekt ein Bezeichner mit einer längeren Lebensdauer erforderlich ist. Langfristige Eintrags-IDs sind immer wochen- oder monatelang gültig und können je nach Anbieter auf anderen Arbeitsstationen gültig sein. Die langfristigen Bezeichner, die von Adressbuchanbietern für benutzerdefinierte Empfänger erstellt werden, sind universell gültig. 
  
Langfristige Eintragsbezeichner werden Nachrichtenspeichern, Ordnern, Nachrichten, Adressbuchcontainern, Messagingbenutzern und Verteilerlisten zugewiesen. Wenn Clientanwendungen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) dieser Objekte aufrufen, wird immer eine langfristige Eintrags-ID zurückgegeben. 
  
Langfristige Eintragsbezeichner müssen für alle Nachrichtenspeicher im aktiven Profil eindeutig sein. Wenn eine Nachricht oder ein Ordner aus einem Nachrichtenspeicher in einen anderen kopiert wird, muss ihr daher ein neuer Eintragsbezeichner zugewiesen werden. Wenn ein Nachrichtenspeicherobjekt verschoben wird, bestimmt der Nachrichtenspeicheranbieter, der die Bewegung implementiert, ob der ursprüngliche Eintragsbezeichner gültig bleibt. Einige Dienstanbieter weisen verschobenen Objekten neue Eintragsbezeichner zu. Andere tun dies nicht. Wenn eine Änderung vor liegt, wird die neue Eintrags-ID in die Informationen einbezogen, die an Clients übergeben werden, wenn sie über die Änderung benachrichtigt werden. 
  
In der Regel implementieren Nachrichtenspeicheranbieter das folgende Verhalten beim Verschieben von Ordnern:
  
- Wenn ein Ordner von einem Nachrichtenspeicher in einen anderen Speicher eines anderen Typs verschoben wird, wird die Eintrags-ID garantiert geändert.
    
- Wenn ein Ordner von einem Nachrichtenspeicher in einen anderen Speicher desselben Typs verschoben wird, ändert sich der Eintragsbezeichner fast immer.
    
- Wenn ein Ordner an einen anderen Speicherort im gleichen Nachrichtenspeicher verschoben wird, kann sich die Eintrags-ID je nach Anbieter des Nachrichtenspeichers ändern.
    
Das Umbenennen eines Ordners ohne Ändern des übergeordneten Ordners führt in der Regel nicht dazu, dass sich der Eintragsbezeichner ändert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

