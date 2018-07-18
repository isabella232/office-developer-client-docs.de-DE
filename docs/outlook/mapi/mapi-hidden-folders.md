---
title: MAPI-ausgeblendet-Ordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 81b53bc138a64da673d6723e60fd90b086174efe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793004"
---
# <a name="mapi-hidden-folders"></a>MAPI-ausgeblendet-Ordner

  
  
**Betrifft**: Outlook 
  
Verborgene Ordner sind generische Ordner, die Clients im Stammordner des Nachrichtenspeichers, statt die Daten in den Stammordner einer Unterstruktur zwischen Personen Nachricht (IPM) erstellen. Da diese Ordner nicht in einer IPM-Unterstruktur platziert werden, werden sie in der Regel vom Anbieter Store Nachricht aus Sicht des Benutzers ausgeblendet. Verborgene Ordner enthalten in der Regel Informationen, die f�r den Nachrichtenspeicher relevant, aber f�r den Benutzer nicht relevant ist. Clients erstellen verborgene Ordner um beispielsweise das Speichern zus�tzlicher Informationen mit dem Rest der Ordnerhierarchie gespeichert werden soll.
  
MAPI erwartet, dass alle Clients anzeigen, erstellen, �ndern und L�schen von Ordnern in einer IPM-Unterstruktur m�glich. Unterst�tzung f�r das Arbeiten mit Ordnern in anderen Strukturen optional gilt. Allerdings sollten alle Nachrichtenspeicher als Standardspeicher verwendet werden kann und mit senden und Empfangen von Nachrichten k�nnen verborgene Ordner vollst�ndig unterst�tzt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

