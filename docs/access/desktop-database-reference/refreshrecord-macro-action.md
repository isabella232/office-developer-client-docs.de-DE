---
title: RefreshRecord-Makroaktion
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 1f1592282635cc27486562ca26c31bcea4f3b4e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611693"
---
# <a name="refreshrecord-macro-action"></a>RefreshRecord-Makroaktion


**Gilt für**: Access 2013, Office 2013

Mit der **DatensatzAktualisieren** -Aktion können Sie die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Datensätzen in der aktuellen Gruppe aktualisieren.

## <a name="remarks"></a>HinwBemerkungeneise

Mit der **DatensatzAktualisieren** -Aktion werden nur Änderungen an Datensätzen in der aktuellen Gruppe angezeigt. Da die Datenbank mit der **DatensatzAktualisieren** -Aktion nicht erneut abgefragt wird, werden in die aktuelle Gruppe keine Datensätze aufgenommen, die hinzugefügt wurden, oder Datensätze daraus entfernt, die gelöscht wurden, seit die Datenbank das letzte Mal abgefragt wurde. Zudem werden Datensätze, die nicht mehr den Kriterien der Abfrage oder des Filters entsprechen, nicht entfernt. Wenn Sie eine erneute Abfrage der Datenbank ausführen möchten, verwenden Sie die **[AktualisierenDaten](requery-macro-action.md)** -Methode. Wenn die Datenquelle für ein Formular erneut abgefragt wird, entspricht die aktuelle Gruppe von Datensätze den gesamten Daten in der Datenquelle.

Das Verhalten dieser Makroaktion hängt davon ab, ob Sie diese in einer Clientdatenbank oder einer Webdatenbank abfragen.

## <a name="client-database"></a>Clientdatenbank

In einer Clientdatenbank können Sie mit der **DatensatzAktualisieren** -Aktion die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Daten in der aktuellen Gruppe aktualisieren. Zu den Änderungen zählen solche des aktuellen Benutzers oder anderer Benutzer in einer Mehrbenutzerumgebung. Dies entspricht der **[Aktualisieren](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** -Methode.

Mit der **DatensatzAktualisieren** -Makroaktion wird in einer Clientdatenbank Folgendes ausgeführt:

1.  Die Datensatzquelle für das aktive Formular oder Datenblatt wird mit den Änderungen an Zeilen in der aktuellen Gruppe aktualisiert. Bei verknüpften ODBC-Tabellen werden Änderungen an Datensätzen in der aktuellen Gruppe aus der Datenquelle abgerufen.

2.  Updates the current set to reflect the changes. Wenn eine Zeile in der Datensatzquelle gelöscht wurde, wird sie so geändert, dass \# gelöscht angezeigt wird.

3.  Aktualisiert das aktive oder Datenblatt so, dass alle geänderten und gelöschten Datensätze im aktuellen Satz angezeigt \# werden.

4.  Alle Unterformulare und Unterberichte im aktiven Formular oder Datenblatt werden erneut abgefragt.

## <a name="web-database"></a>Webdatenbank

In einer Webdatenbank können Sie mit der **DatensatzAktualisieren** -Aktion die zugrunde liegende Datensatzquelle für das aktive Formular oder Datenblatt mit den Änderungen an den Datensätzen in der aktuellen Gruppe aktualisieren. Zu den Änderungen zählen solche des aktuellen Benutzers oder anderer Benutzer.

Mit der **DatensatzAktualisieren** -Makroaktion wird in einer Webdatenbank Folgendes ausgeführt:

1.  Für alle Basistabellen in der aktuellen Gruppe werden Änderungen vom Server abgerufen. Bei verknüpften ODBC-Tabellen werden Änderungen an Datensätzen in der aktuellen Gruppe aus der Datenquelle abgerufen.

2.  Updates the current set to reflect the changes. Wenn eine Zeile im aktuellen Satz gelöscht wurde, wird sie so geändert, dass gelöscht angezeigt \# wird.

3.  Aktualisiert das aktive Formular oder Datenblatt, um alle geänderten und \# gelöschten Datensätze im aktuellen Satz anzuzeigen.

4.  Alle Unterformulare und Unterberichte im aktiven Formular oder Datenblatt werden erneut abgefragt.

