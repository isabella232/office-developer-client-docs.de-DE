---
title: SperrenNavigationsbereich-Makroaktion
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870331"
---
# <a name="locknavigationpane-macro-action"></a>SperrenNavigationsbereich-Makroaktion


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

