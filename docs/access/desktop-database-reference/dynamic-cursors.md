---
title: Dynamische Cursor (Access Desktop Database Reference)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293637"
---
# <a name="dynamic-cursors"></a>Dynamischer Cursor


**Gilt für**: Access 2013, Office 2013

Dynamische Cursor erkennen alle Änderungen, die an den Zeilen im Resultset vorgenommen werden, unabhängig davon, ob die Änderungen innerhalb des Cursors oder durch andere Benutzer außerhalb des Cursors vorgenommen werden. Alle Einfügungs-, Aktualisierungs- und Löschanweisungen aller Benutzer sind über den Cursor sichtbar. Der dynamische Cursor kann alle Änderungen, die an den Zeilen, der Reihenfolge und den Werten im Resultset nach dem Öffnen des Cursors vorgenommen werden, erkennen. Aktualisierungen außerhalb des Cursors sind erst nach einem Commit sichtbar (außer für die Transaktionsisolationsstufe des Cursors ist "uncommitted" festgelegt).

Angenommen, ein dynamischer Cursor ruft zwei Zeilen und eine andere Anwendung ab und aktualisiert die eine Zeile und löscht die andere Zeile. Falls der dynamische Cursor dann diese Zeilen abruft, wird die gelöschte Zeile nicht gefunden, aber die neuen Werte für die aktualisierte Zeile werden angezeigt.

Der dynamische Cursor ist gut geeignet, falls die Anwendung alle gleichzeitigen Aktualisierungen, die von anderen Benutzern vorgenommen werden, erkennen muss. Verwenden Sie **adOpenDynamic** für **CursorTypeEnum**, um anzugeben, dass Sie einen dynamischen Cursor in ADO verwenden möchten.

[Vorwärtscursor](forward-only-cursors.md) | [Statische Cursor](static-cursors.md) | [Keysetcursor](keyset-cursors.md)

