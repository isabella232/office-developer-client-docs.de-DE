---
title: Weitere Möglichkeiten zum Verschieben in ein Recordset
TOCTitle: More ways to move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d671ba680992f17cf8eab8d36559cb4b88d3b43c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552808"
---
# <a name="more-ways-to-move-in-a-recordset"></a>Weitere Möglichkeiten zum Verschieben in ein Recordset

**Gilt für**: Access 2013, Office 2013

The following four methods are used to move around, or scroll, in the **Recordset**: [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). (Some of these methods are unavailable on forward-only cursors.)

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

Wenn **Recordset** -Objekt gefiltert oder sortiert wird und die Daten des aktuellen Datensatzes geändert wurden, ändert sich die Position möglicherweise ebenso. In solchen Fällen funktioniert die **MoveNext-Methode** normal, beachten Sie jedoch, dass die Position um einen Datensatz von der neuen Position nach vorne verschoben wird, nicht von der alten Position. Wenn Sie beispielsweise die Daten im aktuellen Datensatz so ändern, dass der Datensatz an das Ende des sortierten **Recordsets** verschoben wird, bedeutet dies, dass das Aufrufen von **MoveNext** dazu führt, dass ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im **Recordset** **(EOF**  =  **True)** festlegt.

The behavior of the various Move methods of the **Recordset** object depends, to some extent, on the data within the **Recordset**. New records added to the **Recordset** are initially added in a particular order, which is defined by the data source and may be dependent implicitly or explicitly on the data in the new record. For example, if a sort or a join is done within the query that populates the **Recordset**, the new record will be inserted in the appropriate place within the **Recordset**. If ordering is not explicitly specified when creating the **Recordset**, changes in the data source implementation may cause the ordering of the returned rows to change inadvertently. In addition, the sorting, filtering, and editing functions of the **Recordset** can affect the order and possibly which rows in the recordset will be visible.

Deshalb hängen **MoveNext**, **MovePrevious**, **MoveFirst**, **MoveLast** und **Move** von anderen Vorgängen ab, die im gleichen **Recordset** -Objekt ausgeführt werden. ADO versucht immer, die aktuelle Position beizubehalten, bis Sie diese explizit ändern. Manchmal sind aber die Auswirkungen von Änderungen auf eine nachfolgende Navigation schwer nachzuvollziehen. Wenn Sie z. B. **MoveFirst** zum Positionieren in der ersten Zeile eines sortierten **Recordset** -Objekts aufrufen und die Sortierung von aufsteigend in absteigend ändern, befinden Sie sich weiterhin in derselben Zeile - nun ist dies jedoch die letzte Zeile im **Recordset** -Objekt. Mit **MoveFirst** gelangen Sie zu einer anderen Zeile (die neue erste Zeile).

Ein weiteres Beispiel: Wenn Sie sich in einer bestimmten Zeile in der Mitte eines **Recordset** -Objekts befinden und **Delete** und anschließend **MoveNext** aufrufen, befinden Sie sich nun im Datensatz, der unmittelbar auf den gelöschten Datensatz folgt. Durch Aufrufen von **MovePrevious** wird der Datensatz vor dem gelöschten Datensatz zum aktuellen Datensatz, weil der gelöschte Datensatz nicht mehr zur aktiven Mitgliedschaft des **Recordset** -Objekts zählt.

Es ist besonders schwierig, im Hinblick auf das Ändern von Daten im aktuellen Datensatz für alle Anbieter eine konsistente Navigationssyntax für Methoden zu definieren, mit denen die Navigation relativ zum aktuellen Datensatz erfolgt – **MovePrevious**, **MoveNext** und **Move** . Wenn Sie z. B. ein sortiertes, gefiltertes **Recordset**-Objekt verwenden und die Daten im aktuellen Datensatz so ändern, dass sie sich vor allen anderen Datensätzen befinden, die geänderten Daten aber nicht mehr mit dem Filter übereinstimmen, ist nicht klar, an welche Position Sie mit **MoveNext** gelangen sollten. Die sicherste Schlussfolgerung ist, dass die relative Bewegung innerhalb eines **Recordset**-Objekts riskanter als die absolute Bewegung ist (z. B. mit **MoveFirst** oder **MoveLast**), wenn Daten geändert werden, während Datensätze bearbeitet, hinzugefügt oder gelöscht werden. Das Sortieren und Filtern sollte auf einem Primärschlüssel oder einer Primär-ID basieren, weil diese Art von Wert unverändert bleiben sollte.

