---
title: MAPI-Objekt Kapselungshierarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6350202eb22edc478f7738bebf6d7f0bc4684ee0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566243"
---
# <a name="mapi-object-containment-hierarchy"></a>MAPI-Objekt Kapselungshierarchie
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Eingrenzung Beziehung zwischen Objekten gibt die Abhängigkeiten, die einige Objekte auf andere Objekte für den Zugriff haben. Für eine Clientanwendung ermöglicht den Zugriff auf bestimmte Objekte Zugriff auf andere. In einigen Fällen folgt die Eingrenzung Beziehung zwischen Objekten, die von einem Dienstanbieter implementiert eine logische Hierarchie. In anderen Fällen ist es frei wählbar. 
  
Ein Client muss Zugriff auf ein MAPI-Sitzung-Objekt abrufen, bevor es viele andere Objekte (beispielsweise Dienstanbieter und das MAPI-Adressbuch) verwenden kann.
  
Nachricht Store Kapselung basiert auf die hierarchische Beziehung zwischen Objekten im Nachrichtenspeicher: Nachrichtenspeicher-Objekts selbst, Ordner, Nachrichten und Anlagen. Anlagen sind logisch in Nachrichten, die Nachrichten in Ordnern und Ordner in der Nachrichtenspeicher enthalten. Die Beziehung Kapselung ermittelt diese logischen Hierarchie. Um den Zugriff auf eine Nachricht muss beispielsweise ein Client zunächst den Ordner zugreifen in dem die Nachricht enthalten ist. Profile und Status Objekte sind Beispiele für eine weitere beliebige Kapselung Beziehung. Beide dieser Objekte sind über die Sitzung verfügbar. 
  
Einige Objekte bereitstellen Containern nur Zugriff. Anlagen und Empfänger sind Beispiele für Objekte, deren Container solcher abhängig sind. Der nur Zugriff auf eine Anlage oder einen Empfänger erfolgt über die Nachricht, zu der es gehört. Andere Objekte weisen alternative Pfade. Diese Objekte werden binäre IDs, bezeichnet als Eintragsbezeichner, durch die-Dienstanbieter, die sie erstellen zugewiesen. Eintragsbezeichner können verwendet werden ihre Objekte direkt, Zugriff auf Clients für die Eingrenzung Struktur umgehen aktiviert werden. 
  
Die folgende Abbildung zeigt die MAPI-Kapselungshierarchie. Die Sitzung wird am oberen Rand der Struktur, da es in der Sitzung ist, dass ein Client alle anderen Objekte zugreift. Die nächste Ebene enthält die Nachricht Store Tabelle ein Table-Objekt, in der Eigenschaften für alle Anbieter die Nachricht in der aktuellen Sitzung und das Adressbuch Zugriff auf alle Address Book Anbieter bereitstellen aufgelistet. Das Nachricht Store Tabelle und Ihr-Adressbuch werden verwendet, um Zugriff auf die Objekte, die von bestimmten Dienstanbietern dargestellt im Kapselung Reihenfolge weiter implementiert.
  
**MAPI-Einschlusshierarchie**
  
![MAPI-Kapselungshierarchie] (media/amapi_41.gif "MAPI-Kapselungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

