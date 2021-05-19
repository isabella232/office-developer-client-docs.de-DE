---
title: Hierarchie der Eindämmung von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426926"
---
# <a name="mapi-object-containment-hierarchy"></a>Hierarchie der Eindämmung von MAPI-Objekten
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Containmentbeziehung zwischen Objekten gibt die Abhängigkeiten an, die einige Objekte für den Zugriff auf andere Objekte aufweisen. Für eine Clientanwendung ermöglicht der Zugriff auf bestimmte Objekte den Zugriff auf andere. In einigen Fällen folgt die Eindämmungsbeziehung zwischen Objekten, die von einem Dienstanbieter implementiert werden, einer logischen Hierarchie. In anderen Fällen ist dies willkürlich. 
  
Ein Client muss Zugriff auf ein MAPI-Sitzungsobjekt erhalten, bevor er viele andere Objekte verwenden kann (z. B. Dienstanbieter und das MAPI-Adressbuch).
  
Die Nachrichtenspeicher-Eindämmung basiert auf der hierarchischen Beziehung zwischen Objekten im Nachrichtenspeicher: dem Nachrichtenspeicherobjekt selbst, Ordnern, Nachrichten und Anlagen. Logischerweise sind Anlagen in Nachrichten, Nachrichten in Ordnern und Ordnern im Nachrichtenspeicher enthalten. Die Containmentbeziehung entspricht dieser logischen Hierarchie. Um beispielsweise auf eine Nachricht zugreifen zu können, muss ein Client zuerst auf den Ordner zugreifen, in dem die Nachricht enthalten ist. Profile und Statusobjekte sind Beispiele für eine beliebigere Eindämmungsbeziehung. Beide Objekte sind über die Sitzung verfügbar. 
  
Bei einigen Objekten bieten Container den einzigen Zugriff. Anlagen und Empfänger sind Beispiele für Objekte, die vollständig von ihren Containern abhängig sind. Der einzige Zugriff auf eine Anlage oder einen Empfänger besteht über die Nachricht, zu der sie gehört. Andere Objekte verfügen über alternative Zugriffspfade. Diesen Objekten werden von den Dienstanbietern, die sie erstellen, binäre Bezeichner zugewiesen, die als Eingabebezeichner bezeichnet werden. Eingabebezeichner können verwendet werden, um direkt auf ihre Objekte zu zugreifen, sodass Clients die Eindämmungsstruktur umgehen können. 
  
Die folgende Abbildung zeigt die MAPI-Eindämmungshierarchie. Die Sitzung befindet sich ganz oben in der Struktur, da ein Client über die Sitzung Zugriff auf alle anderen Objekte erhält. Die nächste Ebene umfasst die Tabelle des Nachrichtenspeichers, ein Tabellenobjekt, das Eigenschaften für alle Nachrichtenspeicheranbieter in der aktuellen Sitzung auflistet, und das Adressbuch, um allen Adressbuchanbietern Zugriff zu bieten. Die Tabelle und das Adressbuch des Nachrichtenspeichers werden verwendet, um auf die objekte zu zugreifen, die von bestimmten Dienstanbietern implementiert wurden (siehe weiter unten in der Eindämmungsreihenfolge).
  
**MAPI-Einschlusshierarchie**
  
![MAPI-Eindämmungshierarchie](media/amapi_41.gif "MAPI-Eindämmungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

