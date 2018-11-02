---
title: Resync Command dynamische-Eigenschaft (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23d03c5c346b377333387a3be1c0f15bc091d235
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927942"
---
# <a name="resync-command-dynamic-property-ado"></a>Resync Command dynamische-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt eine vom Benutzer bereitgestellte Befehlszeichenfolge an, die von der [Resync](resync-method-ado.md)-Methode ausgegeben wird, um die Daten in der Tabelle zu aktualisieren, die in der dynamischen [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)-Eigenschaft genannt ist.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **String** festgelegt oder zurückgegeben, bei dem es sich um eine Befehlszeichenfolge handelt.

## <a name="remarks"></a>Hinweise

Das [Recordset](recordset-object-ado.md)-Objekt ist das Ergebnis einer für mehrere Basistabellen ausgeführten JOIN-Operation. Die betroffenen Zeilen hängen von der *AffectRecords* -Parameter der [Resync](resync-method-ado.md) -Methode. Die standardmäßige **Resync** -Methode wird ausgeführt, wenn die Eigenschaften [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) und **Resync Command** nicht festgelegt sind.

Die Befehlszeichenfolge der **Resync Command** -Eigenschaft ist ein parametrisierter Befehl oder eine gespeicherte Prozedur, der bzw. die die zu aktualisierende Zeile eindeutig identifiziert und eine einzelne Zeile zurückgibt, die die gleiche Anzahl und Reihenfolge der Spalten wie die zu aktualisierende Zeile enthält. Die Befehlszeichenfolge enthält einen Parameter für jede Primärschlüsselspalte in der **Unique Table** -Eigenschaft; andernfalls wird ein Laufzeitfehler zurückgegeben. Die Parameter werden automatisch mit Primärschlüsselwerten aus der zu aktualisierenden Zeile gefüllt.

Es folgen zwei auf SQL basierende Beispiele:

1.  Das **Recordset** -Objekt wird durch einen Befehl definiert:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    Die **Resync Command** -Eigenschaft wird festgelegt auf:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    Die **Unique Table**-Eigenschaft hat den Wert *Orders*, und der Primärschlüssel, *OrderID*, ist parametrisiert. Die Unterauswahl ist eine einfache Möglichkeit, um programmgesteuert sicherzustellen, dass die gleiche Anzahl und Reihenfolge von Spalten zurückgegeben wird wie mit dem ursprünglichen Befehl.

2. Das **Recordset** -Objekt wird mit einer gespeicherten Prozedur definiert:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    Die folgende gespeicherte Prozedur sollte von der **Resync** -Methode ausgeführt werden:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    Die **Resync Command** -Eigenschaft wird festgelegt auf:

    `"{call CustordersResync (?)}"`

Die **Unique Table**-Eigenschaft hat wiederum den Wert *Orders*, und der Primärschlüssel, *OrderID*, ist parametrisiert.

**Resync Command** ist eine dynamische Eigenschaft, die an die **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.

