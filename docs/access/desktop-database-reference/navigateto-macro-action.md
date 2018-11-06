---
title: NavigateTo-Makroaktion
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7da3eb87e775a6b02694910cd017c9535fde1df7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998280"
---
# <a name="navigateto-macro-action"></a>NavigateTo-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können mit der **NavigierenZu** -Aktion das Anzeigen von Datenbankobjekten im Navigationsbereich steuern. Sie können beispielsweise die Kategorisierungsweise von Datenbankobjekten ändern und die Objekte filtern, sodass nur bestimmte Objekte angezeigt werden.

## <a name="setting"></a>Einstellung

Die **NavigierenZu** -Aktion hat folgende Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Category</strong></p></td>
<td><p>Erforderlich. Die Kategorie, gemäß der Objekte im Navigationsbereich angezeigt werden sollen. Klicken Sie im Feld <strong>Kategorie</strong> auf <strong>Objekttyp</strong>, <strong>Tabellen und Ansichten</strong>, <strong>Änderungsdatum</strong>, <strong>Erstellungsdatum</strong> oder <strong>Benutzerdefiniert</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Optional. <strong>Das Argument Grenzwerte der Objekte in der Kategorie</strong> im Navigationsbereich angezeigt werden. Wenn Sie das <strong>Gruppe</strong> Argument leer lassen, wird im Navigationsbereich alle Datenbankobjekte kategorisiert nach den Kriterien im Argument " <strong>Category"</strong> festgelegten angezeigt. In der folgenden Tabelle sind Beispiele gültiger Argumente <strong>Group</strong> für die verschiedenen <strong>Kategorie</strong> Argumente aufgeführt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

- Diese Aktion entspricht dem Auswählen von Kategorien und Gruppen aus der Titelleiste des Navigationsbereichs.

- Gültige Argumente vom Typ **Gruppe** hängen vom verwendeten Argument **Kategorie** ab. Wenn Sie für **Gruppe** ein ungültiges Argument eingeben, wird eine Fehlermeldung angezeigt.Die folgende Tabelle enthält Beispiele gültiger Argumente vom Typ **Gruppe** für jedes Argument vom Typ **Kategorie**.
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Argument "Kategorie"</p></th>
  <th><p>Beispiel für Argumente vom Typ "Gruppe"</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Objekttyp</p></td>
  <td><p>Tabellen, Formulare, Abfragen, Seiten, Makros, Module</p></td>
  </tr>
  <tr class="even">
  <td><p>Tabellen und Sichten</p></td>
  <td><p>Namen bestimmter Tabellen in der Datenbank</p></td>
  </tr>
  <tr class="odd">
  <td><p>Geändert am</p></td>
  <td><p>Heute, Gestern, Letzten Monat, Älter</p></td>
  </tr>
  <tr class="even">
  <td><p>Erstellt am</p></td>
  <td><p>Heute, Gestern, Letzten Monat, Älter</p></td>
  </tr>
  <tr class="odd">
  <td><p>Benutzerdefinierte Kategorie</p></td>
  <td><p>Namen von Gruppen, die Sie für die angegebene benutzerdefinierte Kategorie erstellt haben</p></td>
  </tr>
  </tbody>
  </table>

- Verwenden Sie zum Ausführen der **NavigierenZu** -Aktion in einem VBA-Modul die **NavigateTo** -Methode des **DoCmd** -Objekts.

> [!NOTE]
> Sie müssen zum Navigieren zur obersten Ebene einer Kategorie (beispielsweise Alle Tabellen, Alle Access-Objekte oder Alle Datumswerte) das Argument Gruppe leer lassen. Wenn beispielsweise das Argument Kategorie den Wert Objekttyp aufweist, wird durch Alle Access-Objekte als Argument Gruppe ein Fehler hervorgerufen.


