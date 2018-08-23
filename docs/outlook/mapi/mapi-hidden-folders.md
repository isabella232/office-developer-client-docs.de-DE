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
ms.openlocfilehash: 70aeda8789665a3f35bf75f83f32a92dbeedc8de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589105"
---
# <a name="mapi-hidden-folders"></a>MAPI-ausgeblendet-Ordner

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Verborgene Ordner sind generische Ordner, die Clients im Stammordner des Nachrichtenspeichers, statt die Daten in den Stammordner einer Unterstruktur zwischen Personen Nachricht (IPM) erstellen. Da diese Ordner nicht in einer IPM-Unterstruktur platziert werden, werden sie in der Regel vom Anbieter Store Nachricht aus Sicht des Benutzers ausgeblendet. Verborgene Ordner enthalten in der Regel Informationen, die f�r den Nachrichtenspeicher relevant, aber f�r den Benutzer nicht relevant ist. Clients erstellen verborgene Ordner um beispielsweise das Speichern zus�tzlicher Informationen mit dem Rest der Ordnerhierarchie gespeichert werden soll.
  
MAPI erwartet, dass alle Clients anzeigen, erstellen, �ndern und L�schen von Ordnern in einer IPM-Unterstruktur m�glich. Unterst�tzung f�r das Arbeiten mit Ordnern in anderen Strukturen optional gilt. Allerdings sollten alle Nachrichtenspeicher als Standardspeicher verwendet werden kann und mit senden und Empfangen von Nachrichten k�nnen verborgene Ordner vollst�ndig unterst�tzt.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

