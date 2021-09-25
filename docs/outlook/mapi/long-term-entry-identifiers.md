---
title: Long-Term Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eeb134dd883c2f8b4687be0feb83c88e6b45eb05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571534"
---
# <a name="long-term-entry-identifiers"></a>Long-Term Eintragsbezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein langfristiger Eintragsbezeichner wird einem Objekt von einem Dienstanbieter zugewiesen, wenn ein Objekt einen Bezeichner mit einer längeren Lebensdauer erfordert. Langfristige Eintragsbezeichner sind je nach Anbieter immer für Wochen oder Monate gültig und können auf anderen Arbeitsstationen gültig sein. Die langfristigen Bezeichner, die von Adressbuchanbietern für benutzerdefinierte Empfänger erstellt werden, sind universell gültig. 
  
Langfristige Eintragsbezeichner werden Nachrichtenspeichern, Ordnern, Nachrichten, Adressbuchcontainern, Messagingbenutzern und Verteilerlisten zugewiesen. Wenn Clientanwendungen die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) dieser Objekte aufrufen, wird immer ein langfristiger Eintragsbezeichner zurückgegeben. 
  
Langfristige Eintragsbezeichner müssen in allen Nachrichtenspeichern im aktiven Profil eindeutig sein. Wenn eine Nachricht oder ein Ordner aus einem Nachrichtenspeicher in einen anderen kopiert wird, muss ihr daher ein neuer Eintragsbezeichner zugewiesen werden. Wenn ein Nachrichtenspeicherobjekt verschoben wird, bestimmt der Nachrichtenspeicheranbieter, der die Verschiebung implementiert, ob der ursprüngliche Eintragsbezeichner gültig bleibt. Einige Dienstanbieter weisen verschobenen Objekten neue Eintragsbezeichner zu. andere nicht. Wenn eine Änderung vorliegt, wird der neue Eintragsbezeichner in die Informationen einbezogen, die an clients übergeben werden, wenn sie über die Verschiebung benachrichtigt werden. 
  
In der Regel implementieren Nachrichtenspeicheranbieter beim Verschieben von Ordnern das folgende Verhalten:
  
- Wenn ein Ordner von einem Nachrichtenspeicher in einen anderen Speicher eines anderen Typs verschoben wird, wird der Eintragsbezeichner garantiert geändert.
    
- Wenn ein Ordner von einem Nachrichtenspeicher in einen anderen Speicher desselben Typs verschoben wird, ändert sich der Eintragsbezeichner fast immer.
    
- Wenn ein Ordner an einen anderen Speicherort innerhalb desselben Nachrichtenspeichers verschoben wird, ändert sich der Eintragsbezeichner je nach Nachrichtenspeicheranbieter möglicherweise oder nicht.
    
Das Umbenennen eines Ordners ohne Änderung des übergeordneten Ordners führt in der Regel nicht dazu, dass sich der Eintragsbezeichner ändert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

