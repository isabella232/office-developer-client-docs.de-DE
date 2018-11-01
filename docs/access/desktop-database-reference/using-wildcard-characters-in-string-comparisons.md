---
title: Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen
TOCTitle: Using Wildcard Characters in String Comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c26b5e0a7e5448340cded61717ad27fb68aa827
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869624"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Verwenden von Platzhalterzeichen in Zeichenfolgenvergleichen


**Betrifft**: Access 2013, Office 2013

Der integrierte Mustervergleich ist ein vielseitiges Hilfsmittel, um Zeichenfolgenvergleiche anzustellen. In der folgenden Tabelle sind die Platzhalterzeichen aufgeführt, die Sie mit dem **Wie** -Operator verwenden können, sowie die Anzahl von übereinstimmenden Ziffern oder Zeichenfolgen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zeichen in <em>pattern</em></p></th>
<th><p>Übereinstimmungen in <em>Ausdruck</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? oder _ (Unterstrich)</p></td>
<td><p>Jedes einzelne Zeichen</p></td>
</tr>
<tr class="even">
<td><p>*oder %</p></td>
<td><p>Null oder mehr Zeichen</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Jede einzelne Ziffer (0 - 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>Zeichenliste</em>]</p></td>
<td><p>Ein beliebiges einzelnes Zeichen in <em>charlist</em></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>Zeichenliste</em>]</p></td>
<td><p>Ein beliebiges einzelnes Zeichen nicht in <em>charlist</em></p></td>
</tr>
</tbody>
</table>


Sie können eine Gruppe von einem oder mehreren Zeichen (*Charlist*) in Klammern eingeschlossen (\[ \]) auf beliebiges einzelnes Zeichen in *Ausdruck,* und *Charlist* fast alle Zeichen enthalten in ANSI-Zeichen festgelegt, einschließlich Ziffern. Können die Sonderzeichen Klammern (\[ ), Frage Mark (?), Nummernzeichen (\#), und ein Sternchen (\*) zu einer Übereinstimmung mit direkt nur, wenn in Klammern eingeschlossen. Die schließende Klammer kann nicht verwendet werden ( \]) innerhalb einer Gruppe entsprechend selbst, aber Sie können es außerhalb einer Gruppe als ein einzelnes Zeichen.

Zusätzlich zu einer Liste von Zeichen in Klammern eingeschlossen können *Charlist* einen Bereich von Zeichen angeben, mit einem Bindestrich (-) zum Trennen der Ober- und Untergrenze des Bereichs. Verwenden Sie beispielsweise \[A – Z\] in *Muster* ergibt eine Übereinstimmung, wenn die entsprechende Zeichenposition im *Ausdruck* Großbuchstaben im Bereich von A bis Z enthält. Sie können mehrere Bereiche innerhalb der Klammern einschließen, ohne zur Einschränkung die Bereiche. Beispielsweise \[a-zA-Z0-9\] entspricht einem alphanumerisches Zeichen.

Es ist wichtig zu beachten, dass die ANSI SQL-Platzhalter (%) und (\_) sind nur verfügbar, mit Microsoft® Jet Version 4.X und den Microsoft OLE DB-Anbieter für Jet. Wenn sie in Microsoft Access oder DAO verwendet werden, werden sie als Literale behandelt.

Nachfolgend sind andere wichtige Regeln für den Mustervergleich aufgeführt:

  - Ausrufezeichen (\!) am Anfang von *Charlist* bedeutet, der eine Übereinstimmung, wenn ein beliebiges Zeichen außer denen in *Charlist* im *Ausdruck*gefunden werden. Bei Verwendung außerhalb der Klammern führt das Ausrufezeichen zu einer Übereinstimmung mit einem anderen Ausrufezeichen.

  - Sie können Bindestrich (-) am Anfang (nach einem Ausrufezeichen, falls verwendet wird) oder am Ende des *Charlist* selbst abgleichen verwenden. An jeder anderen Position wird durch den Trennstrich ein Bereich von ANSI-Zeichen identifiziert.

  - Wenn Sie einen Bereich von Zeichen festlegen, müssen die Zeichen in aufsteigender Reihenfolge angegeben werden (A-Z oder 0-100). \[A – Z\] ist ein gültiges Muster, aber \[Z-A\] ist nicht.

  - Die Zeichenfolge \[ \] wird ignoriert. Es gilt eine Nullzeichenfolge ("").

