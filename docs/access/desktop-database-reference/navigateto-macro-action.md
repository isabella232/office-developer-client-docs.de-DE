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
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288602"
---
# <a name="navigateto-macro-action"></a>NavigateTo-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können mit der **NavigierenZu** -Aktion das Anzeigen von Datenbankobjekten im Navigationsbereich steuern. Sie können beispielsweise die Kategorisierungsweise von Datenbankobjekten ändern und die Objekte filtern, sodass nur bestimmte Objekte angezeigt werden.

## <a name="setting"></a>Einstellung

Die **NavigierenZu**-Aktion hat folgende Argumente.

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
<td><p><strong>Kategorie</strong></p></td>
<td><p>Erforderlich. Die Kategorie, gemäß der Objekte im Navigationsbereich angezeigt werden sollen. Klicken Sie im Feld <strong>Kategorie</strong> auf <strong>Objekttyp</strong>, <strong>Tabellen und Ansichten</strong>, <strong>Änderungsdatum</strong>, <strong>Erstellungsdatum</strong> oder <strong>Benutzerdefiniert</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Group</strong></p></td>
<td><p>Optional. Durch das Argument <strong>Gruppe</strong> wird beschränkt, welche Objekte im Navigationsbereich angezeigt werden. Wenn Sie das Argument <strong>Gruppe</strong> leer lassen, werden im Navigationsbereich alle Datenbankobjekte angezeigt, die nach den Kriterien kategorisiert werden, die Sie im <strong>Category</strong> -Argument angeben. In der folgenden Tabelle werden Beispiele gültiger Argumente vom Typ <strong>Gruppe</strong> für die zahlreichen Argumente vom Typ <strong>Kategorie</strong> gezeigt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

- Diese Aktion ähnelt der Auswahl von Kategorien und Gruppen in der Titelleiste des Navigationsbereichs.

- Gültige Argumente vom Typ **Gruppe** hängen vom verwendeten Argument **Kategorie** ab. Wenn Sie für **Gruppe** ein ungültiges Argument eingeben, wird eine Fehlermeldung angezeigt.Die folgende Tabelle enthält Beispiele gültiger Argumente vom Typ **Gruppe** für jedes Argument vom Typ **Kategorie**.
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>Argument "Category"</p></th>
  <th><p>Beispiel für Argumente "Group"</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>Objekttyp</p></td>
  <td><p>Tabellen; Formulare; Abfragen; Seiten; Makros; Module</p></td>
  </tr>
  <tr class="even">
  <td><p>Tabellen und Sichten</p></td>
  <td><p>Namen bestimmter Tabellen in der Datenbank</p></td>
  </tr>
  <tr class="odd">
  <td><p>Geändert am</p></td>
  <td><p>Heute; Gestern; Letzten Monat; Älter</p></td>
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

- Verwenden Sie zum Ausführen der **NavigierenZu**-Aktion in einem VBA-Modul die **NavigateTo**-Methode des **DoCmd**-Objekts.

> [!NOTE]
> To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.


