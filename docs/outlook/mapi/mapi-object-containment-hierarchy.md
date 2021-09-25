---
title: HIERARCHIE DER MAPI-Objekteinschluss
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 321510daf0a978ad369965be983e4001970e24a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584136"
---
# <a name="mapi-object-containment-hierarchy"></a>HIERARCHIE DER MAPI-Objekteinschluss
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Aufnahmebeziehung zwischen Objekten gibt die Abhängigkeiten an, die einige Objekte für den Zugriff auf andere Objekte haben. Bei einer Clientanwendung ermöglicht der Zugriff auf bestimmte Objekte den Zugriff auf andere Objekte. In einigen Fällen folgt die Aufnahmebeziehung zwischen Objekten, die von einem Dienstanbieter implementiert werden, einer logischen Hierarchie. In anderen Fällen ist dies beliebig. 
  
Ein Client muss Zugriff auf ein MAPI-Sitzungsobjekt erhalten, bevor er viele andere Objekte verwenden kann (z. B. Dienstanbieter und das MAPI-Adressbuch).
  
Das Nachrichtenspeicher-Containment basiert auf der hierarchischen Beziehung zwischen Objekten im Nachrichtenspeicher: dem Nachrichtenspeicherobjekt selbst, Ordnern, Nachrichten und Anlagen. Logischerweise sind Anlagen in Nachrichten, Nachrichten in Ordnern und Ordnern im Nachrichtenspeicher enthalten. Die Aufnahmebeziehung entspricht dieser logischen Hierarchie. Um z. B. Zugriff auf eine Nachricht zu erhalten, muss ein Client zuerst auf den Ordner zugreifen, in dem die Nachricht enthalten ist. Profile und Statusobjekte sind Beispiele für eine willkürlichere Aufnahmebeziehung. Beide Objekte sind über die Sitzung verfügbar. 
  
Bei einigen Objekten bieten Container den einzigen Zugriff. Anlagen und Empfänger sind Beispiele für Objekte, die vollständig von ihren Containern abhängig sind. Der einzige Zugriff auf eine Anlage oder einen Empfänger erfolgt über die Nachricht, zu der sie gehört. Andere Objekte haben alternative Zugriffspfade. Diesen Objekten werden binäre Bezeichner, die als Eintragsbezeichner bezeichnet werden, von den Dienstanbietern zugewiesen, die sie erstellen. Eintragsbezeichner können verwendet werden, um direkt auf ihre Objekte zuzugreifen, sodass Clients die Aufnahmestruktur umgehen können. 
  
Die folgende Abbildung zeigt die MAPI-Aufnahmehierarchie. Die Sitzung befindet sich oben in der Struktur, da ein Client über die Sitzung Zugriff auf alle anderen Objekte erhält. Die nächste Ebene umfasst die Nachrichtenspeichertabelle, ein Tabellenobjekt, das Eigenschaften für alle Nachrichtenspeicheranbieter in der aktuellen Sitzung auflistet, und das Adressbuch, um Zugriff auf alle Adressbuchanbieter zu gewähren. Die Tabelle und das Adressbuch des Nachrichtenspeichers werden verwendet, um auf die objekte zuzugreifen, die von bestimmten Dienstanbietern implementiert werden, die als Nächstes in der Einschlussreihenfolge angezeigt werden.
  
**MAPI-Einschlusshierarchie**
  
![MAPI-Einschlusshierarchie](media/amapi_41.gif "MAPI-Einschlusshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

