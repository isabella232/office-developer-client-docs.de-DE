---
title: LockNavigationPane-Makroaktion
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717804"
---
# <a name="locknavigationpane-macro-action"></a>LockNavigationPane-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **SperrenNavigationsbereich** -Aktion können Sie verhindern, dass Benutzer Datenbankobjekte löschen können, die im Navigationsbereich angezeigt werden.

## <a name="setting"></a>Einstellung

Die **SperrenNavigationsbereich** -Aktion verfügt über folgendes Argument.

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
<td><p><strong>Lock</strong></p></td>
<td><p>Wählen Sie <strong>Ja</strong> zum Sperren des Navigationsbereichs aus, oder wählen Sie <strong>Nein</strong> zum Aufheben der Sperrung des Navigationsbereichs aus.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Durch Sperren des Navigationsbereichs werden Sie daran gehindert, Datenbankobjekte zu löschen oder in die Zwischenablage auszuschneiden. Es ist *nicht* verhindern, dass Sie einen der folgenden Vorgänge ausführen:

  - Kopieren von Datenbankobjekten in die Zwischenablage

  - Einfügen von Datenbankobjekten aus der Zwischenablage

  - Ein- oder Ausblenden des Navigationsbereichs

  - Auswählen verschiedener Organisationsschemas für den Navigationsbereich

  - Ein- oder Ausblenden von Abschnitten des Navigationsbereichs

Verwenden Sie zum Ausführen der **SperrenNavigationsbereich** -Aktion in einem VBA-Modul die **LockNavigationPane** -Methode des **DoCmd** -Objekts.

