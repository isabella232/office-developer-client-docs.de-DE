---
title: Resync Command (dynamische Eigenschaft) (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 30707140284c4c4fda157e276e62666f0344ad14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872004"
---
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="e9b2a-102">Resync Command (dynamische Eigenschaft) (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9b2a-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="e9b2a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9b2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9b2a-104">Gibt eine vom Benutzer bereitgestellte Befehlszeichenfolge an, die von der [Resync](resync-method-ado.md)-Methode ausgegeben wird, um die Daten in der Tabelle zu aktualisieren, die in der dynamischen [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)-Eigenschaft genannt ist.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e9b2a-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e9b2a-105">Settings and return values</span></span>

<span data-ttu-id="e9b2a-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **String** festgelegt oder zurückgegeben, bei dem es sich um eine Befehlszeichenfolge handelt.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b2a-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9b2a-107">Remarks</span></span>

<span data-ttu-id="e9b2a-108">Das [Recordset](recordset-object-ado.md)-Objekt ist das Ergebnis einer für mehrere Basistabellen ausgeführten JOIN-Operation.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="e9b2a-109">Die betroffenen Zeilen hängen von der *AffectRecords* -Parameter der [Resync](resync-method-ado.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="e9b2a-110">Die standardmäßige **Resync** -Methode wird ausgeführt, wenn die Eigenschaften [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) und **Resync Command** nicht festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="e9b2a-p102">Die Befehlszeichenfolge der **Resync Command** -Eigenschaft ist ein parametrisierter Befehl oder eine gespeicherte Prozedur, der bzw. die die zu aktualisierende Zeile eindeutig identifiziert und eine einzelne Zeile zurückgibt, die die gleiche Anzahl und Reihenfolge der Spalten wie die zu aktualisierende Zeile enthält. Die Befehlszeichenfolge enthält einen Parameter für jede Primärschlüsselspalte in der **Unique Table** -Eigenschaft; andernfalls wird ein Laufzeitfehler zurückgegeben. Die Parameter werden automatisch mit Primärschlüsselwerten aus der zu aktualisierenden Zeile gefüllt.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="e9b2a-114">Es folgen zwei auf SQL basierende Beispiele:</span><span class="sxs-lookup"><span data-stu-id="e9b2a-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="e9b2a-115">Das **Recordset** -Objekt wird durch einen Befehl definiert:</span><span class="sxs-lookup"><span data-stu-id="e9b2a-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="e9b2a-116">Die **Resync Command** -Eigenschaft wird festgelegt auf:</span><span class="sxs-lookup"><span data-stu-id="e9b2a-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="e9b2a-p103">Die **Unique Table**-Eigenschaft hat den Wert *Orders*, und der Primärschlüssel, *OrderID*, ist parametrisiert. Die Unterauswahl ist eine einfache Möglichkeit, um programmgesteuert sicherzustellen, dass die gleiche Anzahl und Reihenfolge von Spalten zurückgegeben wird wie mit dem ursprünglichen Befehl.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="e9b2a-119">Das **Recordset** -Objekt wird mit einer gespeicherten Prozedur definiert:</span><span class="sxs-lookup"><span data-stu-id="e9b2a-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="e9b2a-120">Die folgende gespeicherte Prozedur sollte von der **Resync** -Methode ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="e9b2a-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="e9b2a-121">Die **Resync Command** -Eigenschaft wird festgelegt auf:</span><span class="sxs-lookup"><span data-stu-id="e9b2a-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="e9b2a-122">Die **Unique Table**-Eigenschaft hat wiederum den Wert *Orders*, und der Primärschlüssel, *OrderID*, ist parametrisiert.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="e9b2a-123">**Resync Command** ist eine dynamische Eigenschaft, die an die **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9b2a-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

