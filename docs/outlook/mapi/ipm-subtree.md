---
title: IPM-Unterstruktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 89f29feffa4cbcfc5a9b4351f12d616ae45532c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561411"
---
# <a name="ipm-subtree"></a>IPM-Unterstruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
DIE MAPI erstellt eine Struktur von Ordnern unterhalb des Stammordners eines Nachrichtenspeichers für alle Clients, die Nachrichten an Empfänger senden und nachrichten von Personen und nicht von Computern empfangen. Nachrichten, die zwischen menschlichen Empfängern ausgetauscht werden, werden als zwischenmenschliche Nachrichten bezeichnet, und diese Struktur wird als zwischenmenschliche Nachricht oder IPM-Unterstruktur bezeichnet. 
  
Eine IPM-Unterstruktur für einen Übermittlungsspeicher besteht aus mindestens den folgenden Ordnern:
  
- Posteingang
    
- Postausgang
    
- Gesendete Elemente
    
- Gelöschte Elemente
    
Dies sind die Standardnamen und Rollen für jeden dieser Ordner. Ein Client kann eigene Namen angeben, wenn die Standardnamen nicht geeignet sind. DIE MAPI weist diesen Ordnern Standardnamen und Zuordnungen zu, um zu verhindern, dass Nachrichten versehentlich ausgeblendet werden, wenn ein Client nicht bereit ist, Empfangsordner für Nachrichten einzurichten. 
  
In einem Microsoft Office Outlook Kontext besteht eine IPM-Unterstruktur aus zusätzlichen Standardordnern für Kalender, Kontakte, Aufgaben, Notizen und Journale.
  
Der Posteingang enthält in der Regel eingehende Nachrichten, und der Postausgang enthält ausgehende Nachrichten (d. b. Nachrichten, die auf das Senden warten). Der Ordner "Gesendete Elemente" enthält eine Kopie jeder gesendeten Nachricht, wenn der Client die **Eigenschaft PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) auf den Eintragsbezeichner dieses Ordners festgelegt hat. Der Ordner "Gelöschte Elemente" enthält Nachrichten, die zum Entfernen markiert sind. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

