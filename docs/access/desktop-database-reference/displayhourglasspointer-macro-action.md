---
title: DisplayHourglassPointer-Makroaktion
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a5635b2b97066394b8596dbcdb50c84abf429719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293833"
---
# <a name="displayhourglasspointer-macro-action"></a>DisplayHourglassPointer-Makroaktion


**Gilt für**: Access 2013, Office 2013

Mit der **AnzeigenSanduhrzeiger** -Aktion können Sie den Mauszeiger so ändern, dass er in Form einer Sanduhr (oder eines anderen Symbols, das Sie ausgewählt haben) angezeigt wird, während ein Makro ausgeführt wird. Diese Aktion bietet einen visuellen Hinweis darauf, dass ein Makro ausgeführt wird. Dies ist besonders nützlich, wenn die Ausführung einer Makroaktion oder des Makros selbst sehr viel Zeit in Anspruch nimmt.

## <a name="setting"></a>Einstellung

Die **AnzeigenSanduhrzeiger**-Aktion hat das folgende Argument.

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
<td><p><strong>Sanduhr</strong></p></td>
<td><p>Klicken Sie im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator auf <strong>Ja</strong> (Symbol) oder <strong>Nein</strong> (zeigen Sie den normalen Mauszeiger) im Feld <strong>Sanduhr on</strong> im Bereich Action Arguments. Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie verwenden diese Aktion häufig, wenn Sie das Echo mithilfe der **Echo** -Aktion deaktiviert haben. Wenn Echo deaktiviert ist, werden die Bildschirmaktualisierungen von Access angehalten, bis das Makro abgeschlossen ist.

Access setzt das Argument **Sanduhr** automatisch auf **Nein** zurück, wenn die Makroausführung beendet ist.

> [!NOTE]
> - In Microsoft Windows handelt es sich um das Symbol, das Sie für **Ausgelastet** im Dialogfeld **Eigenschaften von Maus** der Windows-Systemsteuerung festgelegt haben. Die Standardeinstellung für alle Windows-Betriebssysteme ist ein animiertes Sanduhrsymbol.
> - Wenn Sie möchten, können Sie ein anderes Symbol auswählen.

Verwenden Sie die **Hourglass** -Methode des **DoCmd** -Objekts, um die **AnzeigenSanduhrzeiger** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

