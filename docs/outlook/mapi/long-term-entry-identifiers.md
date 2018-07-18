---
title: Langfristige Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792912"
---
# <a name="long-term-entry-identifiers"></a>Langfristige Eintragsbezeichner

  
  
**Betrifft**: Outlook 
  
Langfristige Eintrags-ID wird von einem Dienstanbieter zu einem Objekt zugewiesen, wenn ein Objekt einen Bezeichner mit längerer Lebensdauer erfordert. Langfristige-Eintragsbezeichner sind immer für Wochen oder Monate gültig und können auf anderen Arbeitsstationen, je nach den Anbieter gültig sein. Die langfristige Bezeichner von adressbuchanbietern implementierte für benutzerdefinierte Empfänger erstellt sind universell gültig. 
  
Langfristige-Eintragsbezeichner werden Nachrichtenspeicher, Ordner, Nachrichten, Address Book Containern, messaging-Benutzer und Verteilung Listen zugewiesen. Wenn Clientanwendungen die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode dieser Objekte aufrufen, ist es immer eine langfristige Eintrags-ID, die zurückgegeben wird. 
  
Langfristige-Eintragsbezeichner müssen für alle Nachrichtenspeicher in das aktive Profil eindeutig sein; aus diesem Grund, wenn eine Nachricht oder einen Ordner aus einem Informationsspeicher in eine andere kopiert werden, muss es eine neuen Eintrags-ID zugewiesen werden. Wenn eine Nachricht Store-Objekt verschoben wird, bestimmt der Nachricht Speicher-Anbieter, der die Verschiebung implementiert, ob die ursprüngliche Eintrags-ID gültig ist. Einige Dienstanbieter weisen Sie neue-Eintragsbezeichner verschobene Objekte; andere nicht. Wenn eine Änderung vorhanden ist, wird die neuen Eintrags-ID in die Informationen an die Clients übergeben wird, wenn sie, der die Verschiebung benachrichtigt werden enthalten sein. 
  
Nachricht Anbieter implementieren in der Regel das folgende Verhalten beim Verschieben von Ordnern:
  
- Wenn ein Ordner an einen anderen Informationsspeicher eines anderen Typs aus einem Informationsspeicher verschoben wird, wird die Eintrags-ID unbedingt ändern.
    
- Wenn Sie ein Ordner aus einem Informationsspeicher in einen anderen Speicher des gleichen Typs verschoben wird, ändert die Eintrags-ID fast immer.
    
- Wenn Sie ein Ordner an einen anderen Speicherort innerhalb der gleichen Nachrichtenspeicher verschoben wurde, die Eintrags-ID möglicherweise oder möglicherweise nicht geändert, je nach Anbieter die Nachricht.
    
Umbenennen eines Ordners in der Regel ohne seines übergeordneten Ordners bewirkt keine Eintrags-ID zu ändern. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eintragsbezeichner](mapi-entry-identifiers.md)

