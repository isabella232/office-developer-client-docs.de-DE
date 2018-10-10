---
title: DatensatzAktualisieren-Makroaktion
TOCTitle: RefreshRecord Macro Action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 91c49ca4d453418a02d55163a023e853fadd5773
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474125"
---
# <a name="refreshrecord-macro-action"></a>DatensatzAktualisieren-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Mit der **DatensatzAktualisieren** -Aktion können Sie die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Datensätzen in der aktuellen Gruppe aktualisieren.

## <a name="remarks"></a>Hinweise

Mit der **DatensatzAktualisieren** -Aktion werden nur Änderungen an Datensätzen in der aktuellen Gruppe angezeigt. Da die Datenbank mit der **DatensatzAktualisieren** -Aktion nicht erneut abgefragt wird, werden in die aktuelle Gruppe keine Datensätze aufgenommen, die hinzugefügt wurden, oder Datensätze daraus entfernt, die gelöscht wurden, seit die Datenbank das letzte Mal abgefragt wurde. Zudem werden Datensätze, die nicht mehr den Kriterien der Abfrage oder des Filters entsprechen, nicht entfernt. Wenn Sie eine erneute Abfrage der Datenbank ausführen möchten, verwenden Sie die **[AktualisierenDaten](requery-macro-action.md)** -Methode. Wenn die Datenquelle für ein Formular erneut abgefragt wird, entspricht die aktuelle Gruppe von Datensätze den gesamten Daten in der Datenquelle.

Das Verhalten dieser Makroaktion hängt davon ab, ob Sie diese in einer Clientdatenbank oder einer Webdatenbank abfragen.

## <a name="client-database"></a>Clientdatenbank

In einer Clientdatenbank können Sie mit der **DatensatzAktualisieren** -Aktion die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Daten in der aktuellen Gruppe aktualisieren. Zu den Änderungen zählen solche des aktuellen Benutzers oder anderer Benutzer in einer Mehrbenutzerumgebung. Dies entspricht der **[Aktualisieren](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** -Methode.

Mit der **DatensatzAktualisieren** -Makroaktion wird in einer Clientdatenbank Folgendes ausgeführt:

1.  Die Datensatzquelle für das aktive Formular oder Datenblatt wird mit den Änderungen an Zeilen in der aktuellen Gruppe aktualisiert. Bei verknüpften ODBC-Tabellen werden Änderungen an Datensätzen in der aktuellen Gruppe aus der Datenquelle abgerufen.

2.  Aktualisiert die aktuelle Gruppe, um die Änderungen widerzuspiegeln. Wenn eine Zeile in der Datenquelle gelöscht wurde, wird es geändert, um anzeigen \#gelöscht.

3.  Aktualisiert das aktive Formular oder Datenblatt, um alle geänderten Datensätze und alle \#Datensätze, die in der aktuellen Gruppe gelöscht.

4.  Alle Unterformulare und Unterberichte im aktiven Formular oder Datenblatt werden erneut abgefragt.

## <a name="web-database"></a>Webdatenbank

In einer Webdatenbank können Sie mit der **DatensatzAktualisieren** -Aktion die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Datensätzen in der aktuellen Gruppe aktualisieren. Zu den Änderungen zählen solche des aktuellen Benutzers oder anderer Benutzer.

Mit der **DatensatzAktualisieren** -Makroaktion wird in einer Webdatenbank Folgendes ausgeführt:

1.  Für alle Basistabellen in der aktuellen Gruppe werden Änderungen vom Server abgerufen. Bei verknüpften ODBC-Tabellen werden Änderungen an Datensätzen in der aktuellen Gruppe aus der Datenquelle abgerufen.

2.  Aktualisiert die aktuelle Gruppe, um die Änderungen widerzuspiegeln. Wenn eine Zeile in der aktuellen Gruppe gelöscht wurde, wird es geändert, um anzeigen \#gelöscht.

3.  Aktualisiert das aktive Formular oder Datenblatt an alle geänderten Datensätze und alle \#Datensätze, die in der aktuellen Gruppe gelöscht.

4.  Alle Unterformulare und Unterberichte im aktiven Formular oder Datenblatt werden erneut abgefragt.

