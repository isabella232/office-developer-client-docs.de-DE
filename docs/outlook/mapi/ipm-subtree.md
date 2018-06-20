---
title: IPM-Unterstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792740"
---
# <a name="ipm-subtree"></a>IPM-Unterstruktur

  
  
**Betrifft**: Outlook 
  
MAPI erstellt eine Struktur von Ordnern unter den Stammordner eines Nachrichtenspeichers für alle Clients, die Nachrichten senden und Empfangen von Nachrichten von Menschen, statt die Computer, die Empfänger. Nachrichten zwischen Empfängern human ausgetauscht werden, werden als Nachrichten zwischen Personen, und diese Struktur ist bezeichnet als zwischen Personen Nachricht oder IPM, subtree. 
  
Eine IPM-Unterstruktur für einen übermittlungsspeicher besteht aus mindestens die folgenden Ordner:
  
- Posteingang
    
- Postausgang
    
- Gesendete Elemente
    
- Gelöschte Elemente
    
Dies sind die Standardnamen und die Rollen für jedes dieser Ordner. ein Client kann einen eigenen Namen angeben, wenn die Standardnamen nicht geeignet sind. MAPI weist den Standardnamen und Zuordnungen für diese Ordner zu verhindern, dass Nachrichten versehentlich ausgeblendet wird, wenn ein Client bildschirmaktualisierung Empfang von Ordnern für Nachrichten herstellen. 
  
In einem Microsoft Office Outlook-Kontext besteht aus eine IPM-Unterstruktur zusätzliche Standardordner für Kalender, Kontakte, Aufgaben, Notizen und Journal.
  
Posteingang enthält normalerweise eingehende Nachrichten, und im Ordner Postausgang enthält ausgehende Nachrichten (d. h., Nachrichten gesendet werden). Ordner Gesendete Objekte enthält eine Kopie jeder gesendeten Nachricht, wenn der Client die Eintrags-ID dieses Ordners die **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))-Eigenschaft festgelegt wurde. Ordner Gelöschte Elemente enthält Nachrichten, die zur Löschung markiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

