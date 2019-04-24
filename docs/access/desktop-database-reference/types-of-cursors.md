---
title: Cursortypen (Access-Desktop-Daten Bankreferenz)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314028"
---
# <a name="types-of-cursors"></a>Cursortypen


**Gilt für**: Access 2013, Office 2013

Als Faustregel gilt, dass Ihre Anwendung den einfachsten Cursor verwenden sollte, der den erforderlichen Datenzugriff ermöglicht. Jedes zusätzliche Cursormerkmal (Vorwärtscursor, schreibgeschützter Cursor, statischer Cursor, Bildlaufcursor, ungepufferter Cursor) hat einen Preis - in Bezug auf Clientarbeitsspeicher, Netzwerklast oder Leistung. In vielen Fällen generieren die Standardcursoroptionen einen komplexeren Cursor, als tatsächlich von der Anwendung benötigt wird.

Die Auswahl des Cursortyps hängt davon ab, wie das Resultset von der Anwendung verwendet wird, sowie von mehreren Designaspekten wie z. B. der Größe des Resultsets, dem Prozentsatz der wahrscheinlich verwendeten Daten, der Empfindlichkeit gegenüber Datenänderungen sowie den Leistungsanforderungen der Anwendung.

Im einfachsten Fall hängt die Cursorauswahl davon ab, ob Sie die Daten ändern oder einfach anzeigen müssen:

  - Wenn Sie keine Daten ändern, sondern lediglich einen Bildlauf in Resultsets ausführen müssen, verwenden Sie einen [Vorwärtscursor](forward-only-cursors.md) oder einen [statischen](static-cursors.md) Cursor.

  - Wenn ein umfangreiches Resultset vorliegt und nur ein paar Zeilen ausgewählt werden müssen, verwenden Sie einen [Keyset](keyset-cursors.md)cursor.

  - Wenn Sie für ein Resultset neueste Hinzufügungen, Änderungen und Löschvorgänge von allen gleichzeitigen Benutzern synchronisieren möchten, verwenden Sie einen [dynamischen](dynamic-cursors.md) Cursor.

Alle Cursortypen unterscheiden sich zwar voneinander. Sie sollten jedoch beachten, dass diese Cursortypen weniger unterschiedliche Ausprägungen darstellen, als einfach das Ergebnis sich überschneidender Merkmale und Optionen sind.

