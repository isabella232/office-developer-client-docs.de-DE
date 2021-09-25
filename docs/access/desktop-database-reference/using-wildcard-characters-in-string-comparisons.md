---
title: Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f46c1cd6ea03b671cf0048b0535d418742a6a673
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572648"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen

**Gilt für**: Access 2013, Office 2013

Der integrierte Mustervergleich ist ein vielseitiges Hilfsmittel, um Zeichenfolgenvergleiche anzustellen. In der folgenden Tabelle sind die Platzhalterzeichen aufgeführt, die Sie mit dem **Wie** -Operator verwenden können, sowie die Anzahl von übereinstimmenden Ziffern oder Zeichenfolgen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zeichen in <em>Muster</em></p></th>
<th><p>Übereinstimmungen in <em>Ausdruck</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? oder _ (Unterstrich)</p></td>
<td><p>Ein beliebiges Zeichen</p></td>
</tr>
<tr class="even">
<td><p>* oder %</p></td>
<td><p>Null oder mehr Zeichen</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Jede einzelne Ziffer (0 - 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>Zeichenliste</em>]</p></td>
<td><p>Jedes einzelne unter <em>Zeichenliste</em> angegebene Zeichen</p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p>Jedes einzelne Zeichen, das nicht unter <em>Zeichenliste</em> angegeben ist</p></td>
</tr>
</tbody>
</table>


Sie können eine Gruppe aus einem oder mehreren Zeichen (*Zeichenliste*) verwenden, die in Klammern ( ) eingeschlossen \[ \] *sind,* um mit jedem einzelnen Zeichen im Ausdruck übereinzugleichen, und *zeichenlist* kann fast alle Zeichen im ANSI-Zeichensatz enthalten, einschließlich Ziffern. Sie können die Sonderzeichen öffnende Klammer ( \[ ), Fragezeichen (?), Nummernzeichen ( \# ) und Sternchen ( ) \* verwenden, um sich selbst nur direkt zuzuordnen, wenn sie in Klammern eingeschlossen sind. Sie können die schließende Klammer ( ) innerhalb einer Gruppe nicht \] verwenden, um sich selbst abzugleichen, aber Sie können sie außerhalb einer Gruppe als einzelnes Zeichen verwenden.

Zusätzlich zu einer einfachen Liste von Zeichen, die in Klammern eingeschlossen sind, kann *charlist* einen Bereich von Zeichen angeben, indem ein Bindestrich (-) verwendet wird, um die oberen und unteren Grenzen des Bereichs zu trennen. Beispielsweise führt die Verwendung von \[ A-Z \] im *Muster* zu einer Übereinstimmung, wenn die entsprechende Zeichenposition im *Ausdruck* die Großbuchstaben im Bereich A bis Z enthält. Sie können mehrere Bereiche in die Klammern einschließen, ohne die Bereiche zu trennen. Beispielsweise \[ entspricht a-zA-Z0-9 \] einem alphanumerischen Zeichen.

Es ist wichtig zu beachten, dass die ANSI-SQL Platzhalter (%) und ( \_ ) nur mit Microsoft Jet Version 4.X und dem Microsoft OLE DB-Anbieter für Jet verfügbar sind. Wenn sie in Microsoft Access oder DAO verwendet werden, werden sie als Literale behandelt.

Nachfolgend sind andere wichtige Regeln für den Mustervergleich aufgeführt:

- Ein Ausrufezeichen ( \! ) am Anfang der *Zeichenliste* bedeutet, dass eine Übereinstimmung vorgenommen wird, wenn ein beliebiges Zeichen außer den Zeichen in *der Zeichenliste* im *Ausdruck* gefunden wird. Bei Verwendung außerhalb der Klammern führt das Ausrufezeichen zu einer Übereinstimmung mit einem anderen Ausrufezeichen.

- Sie können den Trennstrich (-) entweder am Anfang (nach einem Ausrufezeichen, wenn eines verwendet wird) oder am Ende der *Zeichenliste* verwenden, damit ein anderer Trennstrich gefunden wird. An jeder anderen Position wird durch den Trennstrich ein Bereich von ANSI-Zeichen identifiziert.

- Wenn Sie einen Bereich von Zeichen festlegen, müssen die Zeichen in aufsteigender Reihenfolge angegeben werden (A-Z oder 0-100). \[A-Z \] ist ein gültiges Muster, \[ Z-A \] jedoch nicht.

- Die Zeichenfolge \[ \] wird ignoriert; sie wird als leere Zeichenfolge ("") betrachtet.

