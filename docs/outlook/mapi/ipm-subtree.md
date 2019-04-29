---
title: IPM-unterStruktur
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
# <a name="ipm-subtree"></a>IPM-unterStruktur

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI erstellt eine Baumstruktur von Ordnern unterhalb des Stammordners eines Nachrichtenspeichers für alle Clients, die Nachrichten an den Menschen senden und von diesen empfangen, statt aus dem Computer, Empfänger. Nachrichten, die zwischenmenschlichen Empfängern ausgetauscht werden, werden als zwischenmenschliche Nachrichten bezeichnet, und diese Struktur wird als zwischen Person (IPM, subtree) bezeichnet. 
  
Eine IPM-Unterstruktur für einen zustellspeicher besteht aus mindestens den folgenden Ordnern:
  
- Posteingang
    
- Postausgang
    
- Gesendete Elemente
    
- Gelöschte Elemente
    
Hierbei handelt es sich um die Standardnamen und-Rollen für jeden dieser Ordner; ein Client kann eigene Namen angeben, wenn die Standardnamen nicht geeignet sind. MAPI weist Standardnamen und Zuordnungen für diese Ordner zu, um zu verhindern, dass Nachrichten versehentlich ausgeblendet werden, wenn ein Client die Einrichtung von empfangenden Ordnern für Nachrichten vernachlässigt. 
  
In einem Microsoft Office Outlook-Kontext besteht eine IPM-Unterstruktur aus zusätzlichen Standardordnern für Kalender, Kontakte, Aufgaben, Notizen und Journal.
  
Der Posteingang enthält in der Regel eingehende Nachrichten, und der postAusgang enthält ausgehende Nachrichten (also Nachrichten, die darauf warten, gesendet zu werden). Der Ordner "Gesendete Elemente" enthält eine Kopie jeder gesendeten Nachricht, wenn der Client die **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft auf die Eintrags-ID dieses Ordners festgelegt hat. Der Ordner Gelöschte Elemente enthält Nachrichten, die zum Entfernen markiert sind. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

