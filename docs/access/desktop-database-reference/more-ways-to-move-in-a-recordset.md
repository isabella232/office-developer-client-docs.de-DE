---
title: Weitere Möglichkeiten zum Navigieren in einem Recordset
TOCTitle: More Ways to Move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a9a98471a73f5e3471d55ba6e81689dd39a5934
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473220"
---
# <a name="more-ways-to-move-in-a-recordset"></a>Weitere Möglichkeiten zum Navigieren in einem Recordset

**Betrifft**: Access 2013 | Office 2013

Die folgenden vier Methoden werden zum Navigieren bzw. zum Verschieben des Fensterinhalts im Recordset-Objekt verwendet: MoveFirst, MoveLast, MoveNext und MovePrevious. (Einige dieser Methoden sind für Vorwärtscursor nicht verfügbar.)

**MoveFirst** ändert die aktuelle Datensatzposition auf den ersten Datensatz im **Recordset** -Objekt. **MoveLast** ändert die aktuelle Datensatzposition auf den letzten Datensatz im **Recordset** -Objekt. Zur Verwendung von **MoveFirst** oder **MoveLast** muss das **Recordset** -Objekt Lesezeichen oder die Rückwärtscursorbewegung unterstützen; andernfalls wird durch Aufrufen der Methode ein Fehler generiert.

**MoveNext** verschiebt die aktuelle Datensatzposition um eine Position vorwärts. Wenn Sie sich beim Aufrufen von **MoveNext** im letzten Datensatz befinden, wird **EOF** auf **True** festgelegt. **MovePrevious** verschiebt die aktuelle Datensatzposition um eine Position rückwärts. Wenn Sie sich beim Aufrufen von **MovePrevious** im ersten Datensatz befinden, wird **BOF** auf **True** festgelegt. Sie sollten bei Verwendung dieser Methoden die Eigenschaften **EOF** und **BOF** überprüfen und den Cursor auf eine gültige aktuelle Datensatzposition zurückverschieben, falls Sie sich über das Ende des **Recordset** -Objekts hinaus bewegen. Dies ist im Folgenden dargestellt:

```vb
. . . 
oRs.MoveNext 
If oRs.EOF Then oRs.MoveLast 
. . . 
```

Oder im Fall der **MovePrevious** -Methode:

```vb
. . . 
oRs.MovePrevious 
If oRs.BOF Then oRs.MoveFirst 
. . . 
```

Wenn **Recordset** -Objekt gefiltert oder sortiert wird und die Daten des aktuellen Datensatzes geändert wurden, ändert sich die Position möglicherweise ebenso. In solchen Fällen die **MoveNext** -Methode funktioniert normal, die jedoch werden verschoben Beachten Sie, dass die Position einen Datensatz nach vorn von der neuen Position, nicht die alte Position. Beispielsweise werden Daten in den aktuellen Datensatz geändert, so, dass der Datensatz an das Ende der sortierten **Recordset-Objekt**verschoben wird bedeutet, dass ADO aufrufende **MoveNext** führt Festlegen des aktuellen Datensatzes an die Position nach dem letzten Datensatz in der ** Recordset** (**EOF** = **True**).

Das Verhalten der verschiedenen Move-Methoden des Recordset-Objekts hängt bis zu einem gewissen Grad von den Daten innerhalb des Recordset-Objekts ab. Neue Datensätze, die dem Recordset-Objekt hinzugefügt werden, werden zunächst in einer bestimmten Reihenfolge hinzugefügt, die durch die Datenquelle definiert wird und implizit oder explizit von den Daten im neuen Datensatz abhängen kann. Wenn Sie z. B. eine Sortierung oder Verknüpfung innerhalb der Abfrage vornehmen, mit der das Recordset-Objekt aufgefüllt wird, wird der neue Datensatz an der entsprechenden Stelle innerhalb des Recordset-Objekts eingefügt. Falls beim Erstellen des Recordset-Objekts die Reihenfolge nicht explizit angegeben wird, können Änderungen an der Implementierung der Datenquelle dazu führen, dass die Reihenfolge der zurückgegebenen Zeilen versehentlich geändert wird. Darüber hinaus können die Funktionen zum Sortieren, Filtern und Bearbeiten des Recordset-Objekts die Reihenfolge und möglicherweise die Zeilen, die im Recordset angezeigt werden, beeinflussen.

Deshalb hängen **MoveNext**, **MovePrevious**, **MoveFirst**, **MoveLast** und **Move** von anderen Vorgängen ab, die im gleichen **Recordset** -Objekt ausgeführt werden. ADO versucht immer, die aktuelle Position beizubehalten, bis Sie diese explizit ändern. Manchmal sind aber die Auswirkungen von Änderungen auf eine nachfolgende Navigation schwer nachzuvollziehen. Wenn Sie z. B. **MoveFirst** zum Positionieren in der ersten Zeile eines sortierten **Recordset** -Objekts aufrufen und die Sortierung von aufsteigend in absteigend ändern, befinden Sie sich weiterhin in derselben Zeile - nun ist dies jedoch die letzte Zeile im **Recordset** -Objekt. Mit **MoveFirst** gelangen Sie zu einer anderen Zeile (die neue erste Zeile).

Ein weiteres Beispiel: Wenn Sie sich in einer bestimmten Zeile in der Mitte eines **Recordset** -Objekts befinden und **Delete** und anschließend **MoveNext** aufrufen, befinden Sie sich nun im Datensatz, der unmittelbar auf den gelöschten Datensatz folgt. Durch Aufrufen von **MovePrevious** wird der Datensatz vor dem gelöschten Datensatz zum aktuellen Datensatz, weil der gelöschte Datensatz nicht mehr zur aktiven Mitgliedschaft des **Recordset** -Objekts zählt.

Es ist besonders schwierig, im Hinblick auf das Ändern von Daten im aktuellen Datensatz für alle Anbieter eine konsistente Navigationssyntax für Methoden zu definieren, mit denen die Navigation relativ zum aktuellen Datensatz erfolgt – **MovePrevious**, **MoveNext** und **Move** . Wenn Sie z. B. ein sortiertes, gefiltertes **Recordset**-Objekt verwenden und die Daten im aktuellen Datensatz so ändern, dass sie sich vor allen anderen Datensätzen befinden, die geänderten Daten aber nicht mehr mit dem Filter übereinstimmen, ist nicht klar, an welche Position Sie mit **MoveNext** gelangen sollten. Die sicherste Schlussfolgerung ist, dass die relative Bewegung innerhalb eines **Recordset**-Objekts riskanter als die absolute Bewegung ist (z. B. mit **MoveFirst** oder **MoveLast**), wenn Daten geändert werden, während Datensätze bearbeitet, hinzugefügt oder gelöscht werden. Das Sortieren und Filtern sollte auf einem Primärschlüssel oder einer Primär-ID basieren, weil diese Art von Wert unverändert bleiben sollte.

