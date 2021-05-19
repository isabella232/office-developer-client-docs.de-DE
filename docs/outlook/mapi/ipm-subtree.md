---
title: IPM-Unterstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421221"
---
# <a name="ipm-subtree"></a>IPM-Unterstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI erstellt eine Struktur von Ordnern unterhalb des Stammordners eines Nachrichtenspeichers für alle Clients, die Nachrichten an Empfänger senden und nachrichten von menschlichen empfängern anstelle von Computern empfangen. Nachrichten, die zwischen menschlichen Empfängern ausgetauscht werden, werden als zwischenpersönliche Nachrichten bezeichnet, und diese Struktur wird als zwischenpersönliche Nachricht oder IPM-Unterstruktur bezeichnet. 
  
Eine IPM-Unterstruktur für einen Übermittlungsspeicher besteht aus mindestens den folgenden Ordnern:
  
- Posteingang
    
- Postausgang
    
- Gesendete Elemente
    
- Gelöschte Elemente
    
Dies sind die Standardnamen und Rollen für jeden dieser Ordner. Ein Client kann eigene Namen angeben, wenn die Standardnamen nicht geeignet sind. MAPI weist diesen Ordnern Standardnamen und Zuordnungen zu, damit Nachrichten nicht versehentlich ausgeblendet werden, wenn ein Client keine Empfangsordner für Nachrichten einrichten will. 
  
In einem Microsoft Office Outlook besteht eine IPM-Unterstruktur aus zusätzlichen Standardordnern für Kalender, Kontakte, Aufgaben, Notizen und Journal.
  
Der Posteingang enthält in der Regel eingehende Nachrichten, und der Posteingang enthält ausgehende Nachrichten (d. h. Nachrichten, die auf das Senden warten). Der Ordner "Gesendete Elemente" enthält eine Kopie jeder gesendeten Nachricht, wenn der Client die **eigenschaft PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) auf den Eintragsbezeichner dieses Ordners festgelegt hat. Der Ordner "Gelöschte Elemente" enthält Nachrichten, die zum Entfernen markiert sind. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

