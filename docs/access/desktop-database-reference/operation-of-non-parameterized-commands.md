---
title: Verwendung von nicht parametrisierten Befehlen
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c4c4938e823540eecdbb0492760767c45f1101e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562573"
---
# <a name="operation-of-non-parameterized-commands"></a>Verwendung von nicht parametrisierten Befehlen


**Gilt für**: Access 2013, Office 2013

Für nicht parametrisierte Befehle werden alle Providerbefehle ausgeführt, und die **Recordset** -Objekte werden während der Befehlsausführung erstellt. Wenn der Befehl synchron ausgeführt wird, werden alle **Recordset** -Objekte vollständig aufgefüllt. Wenn ein asynchroner Auffüllungsmodus ausgewählt wurde, hängt der Auffüllungsstatus der **Recordset** -Objekte vom Auffüllungsmodus und der Größe der **Recordset** -Objekte ab.

Beispielsweise könnte der *übergeordnete Befehl* ein **Recordset** von Kunden für ein Unternehmen aus einer Tabelle "Customers" zurückgeben, und der untergeordnete Befehl könnte ein **Recordset** von Bestellungen für alle Kunden aus einer *Orders-Tabelle* zurückgeben.

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them. Die Spalten werden in der *RELATE-Klausel* benannt, zuerst in der übergeordneten Spalte und dann in der *untergeordneten Spalte.* The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation. For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field. Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows. These orphaned rows are inaccessible without further reshaping.

Die Datenstrukturierung fügt eine Kapitelspalte an das übergeordnete **Recordset**-Objekt an. Die Werte in der Kapitelspalte sind Verweise auf Zeilen im untergeordneten **Recordset**-Objekt, die die RELATE-Klausel erfüllen. Das heißt, in der *übergeordneten Spalte* einer übergeordneten Zeile ist der gleiche Wert wie in der *untergeordneten Spalte* aller Zeilen des untergeordneten Kapitels vorhanden. Wenn mehrere TO-Klauseln in derselben RELATE-Klausel verwendet werden, werden sie implizit mithilfe eines AND-Operators zusammengefasst. Falls die übergeordneten Spalten in der RELATE-Klausel keinen Schlüssel für das übergeordnete **Recordset**-Objekt darstellen, kann eine einzelne untergeordnete Zeile mehrere übergeordnete Zeilen aufweisen.

Wenn Sie auf den Verweis in der Kapitelspalte zugreifen, ruft ADO automatisch das durch den Verweis dargestellte **Recordset** -Objekt ab. Beachten Sie, dass bei einem nicht parametrisierten Befehl das Kapitel nur eine Teilmenge der Zeilen darstellt, obwohl das gesamte untergeordnete **Recordset** -Objekt abgerufen wurde.

Wenn die angefügte Spalte keinen *Kapitelalias* enthält, wird automatisch ein Name generiert. Ein [Field](field-object-ado.md)-Objekt für die Spalte wird an die [Fields](fields-collection-ado.md)-Auflistung des **Recordset**-Objekts angefügt, und der Datentyp ist **adChapter**.

Weitere Informationen zum Navigieren in einem hierarchischen **Recordset** -Objekt finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).

