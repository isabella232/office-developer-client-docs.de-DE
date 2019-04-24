---
title: Datenstrukturierung (Access Desktop Database Reference)
TOCTitle: Data shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad507ac8c963f1d6ead7bc3bf444e694d83f90e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295037"
---
# <a name="data-shaping"></a>Datenmodellierung

**Gilt für**: Access 2013, Office 2013

Mithilfe der Datenstrukturierung können Sie die Spalten eines strukturierten **Recordset** -Objekts, die Beziehungen zwischen den von den Spalten dargestellten Entitäten und die Art und Weise, in der das **Recordset** -Objekt mit Daten aufgefüllt wird, definieren.

Spalten eines strukturierten **Recordset**-Objekts können Daten von einem Datenprovider wie Microsoft SQL Server, Verweise auf andere **Recordset**-Objekte oder Werte enthalten, die aus einer Berechnung in einer Zeile eines **Recordset**-Objekts oder die aus einem für eine Spalte eines vollständigen **Recordset**-Objekts ausgeführten Vorgangs abgeleitetet sind. Sie können aber auch eine neu erstellte, leere Spalte sein.

Wenn Sie den Wert einer Spalte abrufen, die einen Verweis auf ein anderes **Recordset**-Objekt enthält, wird von ADO (ActiveX Data Objects) automatisch das eigentliche **Recordset**-Objekt zurückgegeben, für das der Verweis steht. Ein **Recordset**-Objekt, das ein anderes **Recordset**-Objekt enthält, wird als hierarchisches Recordset bezeichnet. Hierarchische Recordsets weisen eine Beziehung der *Über- und Unterordnung* auf, in der das *übergeordnete Recordset* das *untergeordnete Recordset* enthält. Der Verweis auf ein **Recordset**-Objekt ist eigentlich ein Verweis auf eine Teilmenge des untergeordneten Recordsets, die als *Kapitel* bezeichnet wird. Ein einzelnes übergeordnetes Recordset kann auf mehrere untergeordnete **Recordset**-Objekte verweisen.

Durch die Syntax des Strukturierungsbefehls können Sie programmgesteuert ein strukturiertes **Recordset** -Objekt erstellen. Dann können Sie programmgesteuert oder durch geeignete visuelle Steuerelemente auf Komponenten des **Recordset** -Objekts zugreifen. Ein Strukturierungsbefehl wird wie alle anderen ADO-Befehlstexte ausgegeben.

Mit der Syntax des Strukturierungsbefehls können Sie auf zwei Methoden hierarchische **Recordset** -Objekte erstellen. Bei der ersten Methode wird ein untergeordnetes **Recordset** -Objekt an ein übergeordnetes **Recordset** -Objekt angefügt. Das übergeordnete und das untergeordnete Recordset weisen üblicherweise zumindest eine gemeinsame Spalte auf: der Wert der Spalte in einer Zeile des übergeordneten Recordsets ist identisch mit dem Wert der Spalte in allen Zeilen des untergeordneten Recordsets.

The second way generates a parent **Recordset** from a child **Recordset**. The records in the child **Recordset** are grouped, typically using the BY clause, and one row is added to the parent **Recordset** for each resulting group in the child. If the BY clause is omitted, the child **Recordset** will form a single group and the parent **Recordset** will contain exactly one row. This is useful for computing "grand total" aggregates over the entire child **Recordset**.

Unabhängig davon, wie das übergeordnete **Recordset** -Objekt gebildet wird, enthält es eine Kapitelspalte, mit der es einem untergeordneten **Recordset** -Objekt zugeordnet werden kann. Bei Bedarf kann das übergeordnete **Recordset** -Objekt auch Spalten aufweisen, die Aggregate (SUM, MIN, MAX usw.) für die Zeilen des untergeordneten Objekts enthalten. Übergeordnete und untergeordnete **Recordset** -Objekte können Spalten aufweisen, die einen Ausdruck in der Zeile im **Recordset** -Objekt enthalten. Zudem können Sie Spalten aufweisen, die neu und zunächst leer sind.

Sie können hierarchische **Recordset** -Objekte in einer beliebigen Tiefe schachteln (d. h., Sie können untergeordnete **Recordset** -Objekte von untergeordneten **Recordset** -Objekten erstellen usw.).

Sie können programmgesteuert oder durch geeignete visuelle Steuerelemente auf **Recordset** -Komponenten des strukturierten **Recordset** -Objekts zugreifen.

Beispiele für Strukturierungsbefehle und die daraus resultierenden Hierarchien finden Sie unter "Using the Data Shaping Service for OLE DB: A Closer Look".

Dieser Abschnitt enthält die folgenden Themen:

- [Umstrukturierung](reshaping.md)
- [Enkel-Aggregat](grandchild-aggregates.md)
- [Parametrisierte Befehle mit dazwischenliegenden COMPUTE-Befehlen](parameterized-commands-with-intervening-compute-commands.md)
- [Speichern von hierarchische Recordsets](persisting-hierarchical-recordsets.md)
