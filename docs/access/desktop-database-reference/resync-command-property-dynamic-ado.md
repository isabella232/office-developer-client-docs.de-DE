---
title: Resync Command Dynamic-Eigenschaft (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa1fe05e6aa7edf04ad74864eb30a03403323c8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306580"
---
# <a name="resync-command-dynamic-property-ado"></a><span data-ttu-id="49d3e-102">Resync Command Dynamic-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="49d3e-102">Resync Command dynamic property (ADO)</span></span>

<span data-ttu-id="49d3e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49d3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49d3e-104">Es wird eine vom Benutzer bereitgestellte Befehlszeichenfolge angegeben, die von der [Resync](resync-method-ado.md)-Methode ausgegeben wird, um die Daten in der Tabelle, die in der dynamischen [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)-Eigenschaft genannt ist, zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="49d3e-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="49d3e-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="49d3e-105">Settings and return values</span></span>

<span data-ttu-id="49d3e-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **String** festgelegt oder zurückgegeben, bei dem es sich um eine Befehlszeichenfolge handelt.</span><span class="sxs-lookup"><span data-stu-id="49d3e-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d3e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49d3e-107">Remarks</span></span>

<span data-ttu-id="49d3e-p101">Das [Recordset](recordset-object-ado.md)-Objekt ist das Ergebnis einer für mehrere Basistabellen ausgeführten JOIN-Operation. Die betroffenen Zeilen hängen vom *AffectRecords*-Parameter der [Resync](resync-method-ado.md)-Methode ab. Die standardmäßige **Resync**-Methode wird ausgeführt, wenn die Eigenschaften [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) und **Resync Command** nicht festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="49d3e-p101">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables. The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method. The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="49d3e-p102">Die Befehlszeichenfolge der **Resync Command** -Eigenschaft ist ein parametrisierter Befehl oder eine gespeicherte Prozedur, der bzw. die die zu aktualisierende Zeile eindeutig identifiziert und eine einzelne Zeile zurückgibt, die die gleiche Anzahl und Reihenfolge der Spalten wie die zu aktualisierende Zeile enthält. Die Befehlszeichenfolge enthält einen Parameter für jede Primärschlüsselspalte in der **Unique Table** -Eigenschaft; andernfalls wird ein Laufzeitfehler zurückgegeben. Die Parameter werden automatisch mit Primärschlüsselwerten aus der zu aktualisierenden Zeile gefüllt.</span><span class="sxs-lookup"><span data-stu-id="49d3e-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="49d3e-114">Es folgen zwei auf SQL basierende Beispiele:</span><span class="sxs-lookup"><span data-stu-id="49d3e-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="49d3e-115">Das **Recordset** -Objekt wird durch einen Befehl definiert:</span><span class="sxs-lookup"><span data-stu-id="49d3e-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="49d3e-116">Die **Resync Command** -Eigenschaft wird festgelegt auf:</span><span class="sxs-lookup"><span data-stu-id="49d3e-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="49d3e-p103">Die **Unique Table**-Eigenschaft hat den Wert *Orders*, und der Primärschlüssel, *OrderID*, ist parametrisiert. Die Unterauswahl ist eine einfache Möglichkeit, um programmgesteuert sicherzustellen, dass die gleiche Anzahl und Reihenfolge von Spalten zurückgegeben wird wie mit dem ursprünglichen Befehl.</span><span class="sxs-lookup"><span data-stu-id="49d3e-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="49d3e-119">Das **Recordset** -Objekt wird mit einer gespeicherten Prozedur definiert:</span><span class="sxs-lookup"><span data-stu-id="49d3e-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="49d3e-120">Die folgende gespeicherte Prozedur sollte von der **Resync** -Methode ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="49d3e-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="49d3e-121">Die **Resync Command**-Eigenschaft wird festgelegt auf:</span><span class="sxs-lookup"><span data-stu-id="49d3e-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="49d3e-122">Die **Unique Table**-Eigenschaft hat wiederum den Wert *Orders*, und der Primärschlüssel, *OrderID*, ist parametrisiert.</span><span class="sxs-lookup"><span data-stu-id="49d3e-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="49d3e-123">**Resync Command** ist eine dynamische Eigenschaft, die an die [Properties](properties-collection-ado.md)-Auflistung des **Recordset**-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="49d3e-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

