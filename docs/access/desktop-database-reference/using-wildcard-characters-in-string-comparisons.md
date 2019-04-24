---
title: Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305936"
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
<td><p>*oder</p></td>
<td><p>Null oder mehr Zeichen</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Jede einzelne Ziffer (0 - 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>charlist</em>]</p></td>
<td><p>Jedes einzelne unter <em>Zeichenliste</em> angegebene Zeichen</p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p>Jedes einzelne Zeichen, das nicht unter <em>Zeichenliste</em> angegeben ist</p></td>
</tr>
</tbody>
</table>


Sie können eine Gruppe von einem oder mehreren Zeichen (*charlist*), die in eckigen\[ \]Klammern () eingeschlossen sind, verwenden, um ein beliebiges einzelnes Zeichen in Expression abzugleichen *,* und *charlist* kann fast alle Zeichen im ANSI-Zeichensatz enthalten, einschließlich Ziffern. Sie können die Sonderzeichen öffnende Klammer (\[ ), das Fragezeichen (?), das Nummern\#Zeichen () und das\*Sternchen () verwenden, um sich selbst direkt zuzuordnen, wenn Sie in eckigen Klammern eingeschlossen sind. Sie können die schließende Klammer ( \]) nicht in einer Gruppe verwenden, um sich selbst abzugleichen, aber Sie kann Sie außerhalb einer Gruppe als einzelnes Zeichen verwenden.

Zusätzlich zu einer einfachen Liste mit Zeichen, die in eckigen ** Klammern eingeschlossen sind, kann charlist einen Zeichentyp angeben, indem Sie einen Bindestrich (-) verwenden, um die obere und untere Grenze des Bereichs zu trennen. Wenn Sie beispielsweise \[A-Z\] in *Muster* verwenden, wird eine Übereinstimmung erzielt, wenn die entsprechende Zeichenposition in *Expression* einen der Großbuchstaben im Range A bis Z enthält. Sie können mehrere Bereiche in die eckigen Klammern einschließen, ohne die Bereiche zu begrenzen. Beispielsweise stimmt \[a-Za-z0-9\] mit einem alphanumerischen Zeichen überein.

Beachten Sie, dass die ANSI SQL-Platzhalterzeichen (%) und (\_) sind nur verfügbar mit Microsoft Jet, Version 4. X, und dem Microsoft OLE DB-Anbieter für Jet. Wenn sie in Microsoft Access oder DAO verwendet werden, werden sie als Literale behandelt.

Nachfolgend sind andere wichtige Regeln für den Mustervergleich aufgeführt:

- Ein Ausrufezeichen\!() am Anfang von *charlist* bedeutet, dass eine Übereinstimmung erzielt wird, wenn ein beliebiges Zeichen mit Ausnahme der Werte in *charlist* in *Expression*gefunden wird. Bei Verwendung außerhalb der Klammern führt das Ausrufezeichen zu einer Übereinstimmung mit einem anderen Ausrufezeichen.

- Sie können den Trennstrich (-) entweder am Anfang (nach einem Ausrufezeichen, wenn eines verwendet wird) oder am Ende der *Zeichenliste* verwenden, damit ein anderer Trennstrich gefunden wird. An jeder anderen Position wird durch den Trennstrich ein Bereich von ANSI-Zeichen identifiziert.

- Wenn Sie einen Bereich von Zeichen festlegen, müssen die Zeichen in aufsteigender Reihenfolge angegeben werden (A-Z oder 0-100). \[A-Z\] ist ein gültiges Muster, \[aber Z-\] a nicht.

- Die Zeichenfolge \[ \] wird ignoriert; Sie wird als Zeichenfolge der Länge NULL ("") betrachtet.

