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
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345819"
---
# <a name="mapi-object-containment-hierarchy"></a>MAPI-Objekt Kapselungshierarchie
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Kapselungsbeziehung zwischen Objekten gibt die Abhängigkeiten an, die einige Objekte für andere Objekte für Access aufweisen. Für eine Clientanwendung ermöglicht der Zugriff auf bestimmte Objekte den Zugriff auf andere. In einigen Fällen folgt die Kapselungsbeziehung zwischen von einem Dienstanbieter implementierten Objekten einer logischen Hierarchie. In anderen Fällen ist es willkürlich. 
  
Ein Client muss Zugriff auf ein MAPI-Sitzungsobjekt erhalten, bevor es viele andere Objekte verwenden kann (beispielsweise Dienstanbieter und das MAPI-Adressbuch).
  
Die Nachrichtenspeicher Kapselung basiert auf der hierarchischen Beziehung zwischen Objekten im Nachrichtenspeicher: dem Nachrichtenspeicherobjekt selbst, Ordnern, Nachrichten und Anlagen. Logischerweise sind Anlagen in Nachrichten, Nachrichten in Ordnern und Ordnern im Nachrichtenspeicher enthalten. Die Kapselungsbeziehung entspricht dieser logischen Hierarchie. Um beispielsweise auf eine Nachricht zugreifen zu können, muss der Client zunächst auf den Ordner zugreifen, in dem die Nachricht enthalten ist. Profile und Status-Objekte sind Beispiele für eine beliebige Kapselungsbeziehung. Beide Objekte stehen über die Sitzung zur Verfügung. 
  
Bei einigen Objekten bieten Container den einzigen Zugriff. Anlagen und Empfänger sind Beispiele für Objekte, die vollständig von ihren Containern abhängig sind. Der einzige Zugriff auf eine Anlage oder einen Empfänger erfolgt über die Nachricht, zu der Sie gehört. Andere Objekte weisen alternative Zugriffspfade auf. Diesen Objekten werden von den Dienstanbietern, die Sie erstellen, binäre Bezeichner (als Eintrags-IDs bezeichnet) zugewiesen. Eintrags-IDs können verwendet werden, um direkt auf Ihre Objekte zuzugreifen, sodass Clients die Kapselungs Struktur umgehen. 
  
Die folgende Abbildung zeigt die MAPI-Kapselungshierarchie. Die Sitzung befindet sich am Anfang der Struktur, da der Client über die Sitzung Zugriff auf alle anderen Objekte erhält. Die nächste Ebene enthält die Nachrichtenspeichertabelle, ein Table-Objekt, in dem die Eigenschaften für alle Nachrichtenspeicher Anbieter in der aktuellen Sitzung aufgeführt sind, und das Adressbuch für den Zugriff auf alle Adressbuchanbieter. Die Nachrichtenspeichertabelle und das Adressbuch werden verwendet, um auf die von bestimmten Dienstanbietern implementierten Objekte zuzugreifen, die im nächsten in der Containment-Reihenfolge angezeigt werden.
  
**MAPI-Einschlusshierarchie**
  
![MAPI-Kapselungshierarchie] (media/amapi_41.gif "MAPI-Kapselungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

