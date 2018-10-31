---
title: Data Shaping (Access PC-Datenbank-Referenz)
TOCTitle: Data Shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 686c860ef9d8975b02391fedcea8f4b6f4e0b9bb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862296"
---
# <a name="data-shaping"></a>Data Shaping


**Betrifft**: Access 2013 | Office 2013

Mithilfe der Datenstrukturierung können Sie die Spalten eines strukturierten **Recordset** -Objekts, die Beziehungen zwischen den von den Spalten dargestellten Entitäten und die Art und Weise, in der das **Recordset** -Objekt mit Daten aufgefüllt wird, definieren.

Spalten eines strukturierten **Recordset** -Objekts können Daten von einem Datenprovider wie Microsoft SQL Server, Verweise auf andere **Recordset** -Objekte oder Werte enthalten, die aus einer Berechnung in einer Zeile eines **Recordset** -Objekts oder die aus einem für eine Spalte eines vollständigen **Recordset** -Objekts ausgeführten Vorgangs abgeleitetet sind. Sie können aber auch eine neu erstellte, leere Spalte sein.

Wenn Sie den Wert einer Spalte abrufen, die einen Verweis auf ein anderes **Recordset**-Objekt enthält, wird von ADO (ActiveX Data Objects) automatisch das eigentliche **Recordset**-Objekt zurückgegeben, für das der Verweis steht. Ein **Recordset**-Objekt, das ein anderes **Recordset**-Objekt enthält, wird als hierarchisches Recordset bezeichnet. Hierarchische Recordsets weisen eine Beziehung der *Über- und Unterordnung* auf, in der das *übergeordnete Recordset* das *untergeordnete Recordset* enthält. Der Verweis auf ein **Recordset**-Objekt ist eigentlich ein Verweis auf eine Teilmenge des untergeordneten Recordsets, die als *Kapitel* bezeichnet wird. Ein einzelnes übergeordnetes Recordset kann auf mehrere untergeordnete **Recordset**-Objekte verweisen.

Durch die Syntax des Strukturierungsbefehls können Sie programmgesteuert ein strukturiertes **Recordset** -Objekt erstellen. Dann können Sie programmgesteuert oder durch geeignete visuelle Steuerelemente auf Komponenten des **Recordset** -Objekts zugreifen. Ein Strukturierungsbefehl wird wie alle anderen ADO-Befehlstexte ausgegeben.

Mit der Syntax des Strukturierungsbefehls können Sie auf zwei Methoden hierarchische **Recordset** -Objekte erstellen. Bei der ersten Methode wird ein untergeordnetes **Recordset** -Objekt an ein übergeordnetes **Recordset** -Objekt angefügt. Das übergeordnete und das untergeordnete Recordset weisen üblicherweise zumindest eine gemeinsame Spalte auf: der Wert der Spalte in einer Zeile des übergeordneten Recordsets ist identisch mit dem Wert der Spalte in allen Zeilen des untergeordneten Recordsets.

Bei der zweiten Methode wird ein übergeordnetes Recordset-Objekt aus einem untergeordneten Recordset-Objekt generiert. Die Datensätze im untergeordneten Recordset-Objekt werden gruppiert (normalerweise mit der BY-Klausel), und für jede resultierende Gruppe im untergeordneten Recordset wird dem übergeordneten Recordset-Objekt eine Zeile hinzugefügt. Wird die BY-Klausel ausgelassen, bildet das untergeordnete Recordset-Objekt eine einzelne Gruppe, und das übergeordnete Recordset-Objekt enthält genau eine Zeile. Dies ist nützlich zum Berechnen von Gesamtsummenaggregaten für das vollständige untergeordnete Recordset-Objekt.

Unabhängig davon, wie das übergeordnete **Recordset** -Objekt gebildet wird, enthält es eine Kapitelspalte, mit der es einem untergeordneten **Recordset** -Objekt zugeordnet werden kann. Bei Bedarf kann das übergeordnete **Recordset** -Objekt auch Spalten aufweisen, die Aggregate (SUM, MIN, MAX usw.) für die Zeilen des untergeordneten Objekts enthalten. Übergeordnete und untergeordnete **Recordset** -Objekte können Spalten aufweisen, die einen Ausdruck in der Zeile im **Recordset** -Objekt enthalten. Zudem können Sie Spalten aufweisen, die neu und zunächst leer sind.

Sie können hierarchische **Recordset** -Objekte in einer beliebigen Tiefe schachteln (d. h., Sie können untergeordnete **Recordset** -Objekte von untergeordneten **Recordset** -Objekten erstellen usw.).

Sie können programmgesteuert oder durch geeignete visuelle Steuerelemente auf **Recordset** -Komponenten des strukturierten **Recordset** -Objekts zugreifen.

Beispiele für Strukturierungsbefehle und die daraus resultierenden Hierarchien finden Sie unter "Using the Data Shaping Service for OLE DB: A Closer Look".

Dieser Abschnitt enthält die folgenden Themen:

- [Umstrukturierung](reshaping.md)

- [Untergeordnete Aggregate](grandchild-aggregates.md)

- [Parametrisierte Befehle mit dazwischen liegenden COMPUTE-Befehlen](parameterized-commands-with-intervening-compute-commands.md)

- [Speichern hierarchischer Recordsets](persisting-hierarchical-recordsets.md)