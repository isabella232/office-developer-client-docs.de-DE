---
title: Verwenden von nicht parametrisierten Befehlen
TOCTitle: Operation of Non-Parameterized Commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f45bb8e148fe2ba252b2620d41685006302cfdb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473458"
---
# <a name="operation-of-non-parameterized-commands"></a>Verwenden von nicht parametrisierten Befehlen


**Betrifft**: Access 2013 | Office 2013

Für nicht parametrisierte Befehle werden alle Providerbefehle ausgeführt, und die **Recordset** -Objekte werden während der Befehlsausführung erstellt. Wenn der Befehl synchron ausgeführt wird, werden alle **Recordset** -Objekte vollständig aufgefüllt. Wenn ein asynchroner Auffüllungsmodus ausgewählt wurde, hängt der Auffüllungsstatus der **Recordset** -Objekte vom Auffüllungsmodus und der Größe der **Recordset** -Objekte ab.

Beispielsweise könnte mit dem übergeordneten Befehl ein Recordset-Objekt mit Kunden für eine Firma aus der Customers-Tabelle zurückgegeben werden, und mit dem untergeordneten Befehl könnte ein Recordset-Objekt mit Bestellungen für alle Kunden aus der Orders-Tabelle zurückgegeben werden.

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

Für nicht parametrisierte hierarchische Beziehungen müssen jedes übergeordnete und untergeordnete **Recordset** -Objekt eine Spalte gemeinsam, um diese zu verknüpfen. Die Spalten in der *übergeordneten Spalte* -Klausel verknüpfen heißen erste und klicken Sie dann auf *untergeordnete-Spalte*. Die Spalten möglicherweise unterschiedliche Namen in ihre jeweiligen **Recordset** -Objekte, aber müssen dieselben Informationen, um anzugeben, eine sinnvolle Beziehung verweisen. Beispielsweise konnten **Kunden** und **Orders** **Recordset** -Objekte beide ein Feld CustomerID verfügen. Da die Mitgliedschaft des untergeordneten **Recordset-Objekts** durch den Anbieterbefehl bestimmt wird, ist es möglich, für das untergeordnete **Recordset** verwaiste Zeilen enthalten. Diese verwaisten Zeilen werden ohne weitere Umstrukturierung kann nicht zugegriffen.

Die Datenstrukturierung fügt eine Kapitelspalte an das übergeordnete **Recordset** -Objekt an. Die Werte in der Kapitelspalte sind Verweise auf Zeilen im untergeordneten **Recordset** -Objekt, die die RELATE-Klausel erfüllen. D. h., wird der gleiche Wert in der *übergeordneten Spalte* einer übergeordneten Zeile wie in der *untergeordneten Spalte* aller Zeilen des untergeordneten Kapitels befindet. Wenn mehrere TO-Klauseln in derselben RELATE-Klausel verwendet werden, werden sie implizit mithilfe eines AND-Operators zusammengefasst. Falls die übergeordneten Spalten in der RELATE-Klausel keinen Schlüssel für das übergeordnete **Recordset** -Objekt darstellen, kann eine einzelne untergeordnete Zeile mehrere übergeordnete Zeilen aufweisen.

Wenn Sie auf den Verweis in der Kapitelspalte zugreifen, ruft ADO automatisch das durch den Verweis dargestellte **Recordset** -Objekt ab. Beachten Sie, dass bei einem nicht parametrisierten Befehl das Kapitel nur eine Teilmenge der Zeilen darstellt, obwohl das gesamte untergeordnete **Recordset** -Objekt abgerufen wurde.

Wenn die angefügte Spalte keinen *Kapitelalias* enthält, wird automatisch ein Name generiert. Ein [Field](field-object-ado.md)-Objekt für die Spalte wird an die [Fields](fields-collection-ado.md)-Auflistung des **Recordset**-Objekts angefügt, und der Datentyp ist **adChapter**.

Weitere Informationen zum Navigieren in einem hierarchischen **Recordset** -Objekt finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).

