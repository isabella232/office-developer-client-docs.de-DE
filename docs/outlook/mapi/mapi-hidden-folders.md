---
title: MAPI-ausgeblendet-Ordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cb09c8b3406632f97b128a1bed8a5f0a88298d2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561236"
---
# <a name="mapi-hidden-folders"></a>MAPI-ausgeblendet-Ordner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verborgene Ordner sind generische Ordner, die Clients im Stammordner des Nachrichtenspeichers, statt die Daten in den Stammordner einer Unterstruktur zwischen Personen Nachricht (IPM) erstellen. Da diese Ordner nicht in einer IPM-Unterstruktur platziert werden, werden sie in der Regel vom Anbieter Store Nachricht aus Sicht des Benutzers ausgeblendet. Verborgene Ordner enthalten in der Regel Informationen, die f�r den Nachrichtenspeicher relevant, aber f�r den Benutzer nicht relevant ist. Clients erstellen verborgene Ordner um beispielsweise das Speichern zus�tzlicher Informationen mit dem Rest der Ordnerhierarchie gespeichert werden soll.
  
MAPI erwartet, dass alle Clients anzeigen, erstellen, �ndern und L�schen von Ordnern in einer IPM-Unterstruktur m�glich. Unterst�tzung f�r das Arbeiten mit Ordnern in anderen Strukturen optional gilt. Allerdings sollten alle Nachrichtenspeicher als Standardspeicher verwendet werden kann und mit senden und Empfangen von Nachrichten k�nnen verborgene Ordner vollst�ndig unterst�tzt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

