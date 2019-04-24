---
title: Recordset.Index-Eigenschaft (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f475635424cfb9ed8ddab4025d6a944bdedd39fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300525"
---
# <a name="recordsetindex-property-dao"></a><span data-ttu-id="cffe7-102">Recordset.Index-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="cffe7-102">Recordset.Index Property (DAO)</span></span>

<span data-ttu-id="cffe7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cffe7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cffe7-104">Legt einen Wert fest, der den Namen des aktuellen **[Index](index-object-dao.md)**-Objekts in einem **[Recordset](recordset-object-dao.md)**-Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="cffe7-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cffe7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cffe7-105">Syntax</span></span>

<span data-ttu-id="cffe7-106">*Ausdruck* .Index</span><span class="sxs-lookup"><span data-stu-id="cffe7-106">expression  . Index</span></span>

<span data-ttu-id="cffe7-107">*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cffe7-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cffe7-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cffe7-108">Remarks</span></span>

<span data-ttu-id="cffe7-p101">Datensätze in Basistabellen werden nicht in einer bestimmten Reihenfolge gespeichert. Durch Festlegen der **Index**-Eigenschaft wird die Reihenfolge der von der Datenbank zurückgegebenen Datensätze geändert. Auf die Speicherreihenfolge der Datensätze hat dies keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="cffe7-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="cffe7-p102">Das angegebene **Index**-Objekt muss bereits definiert sein. Wenn Sie die **Index**-Eigenschaft auf ein **Index**-Objekt festlegen, das nicht vorhanden ist, oder wenn die **Index**-Eigenschaft nicht festgelegt ist, tritt bei Verwendung der **[Seek](recordset-seek-method-dao.md)**-Methode ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cffe7-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="cffe7-113">Untersuchen Sie die **Indexes**-Sammlung eines **TableDef**-Objekts, um zu bestimmen, welche **Index**-Objekte für **Recordset**-Objekte vom Typ "Tabelle" zur Verfügung stehen, die aus diesem **TableDef**-Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cffe7-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="cffe7-114">Sie können einen neuen Index für die Tabelle erstellen, indem Sie ein neues **Index**-Objekt erstellen, die zugehörigen Eigenschaften festlegen, es an die **Indexes**-Sammlung des zugrunde liegenden **TableDef**-Objekts anfügen und anschließend das **Recordset**-Objekt erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="cffe7-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="cffe7-p103">Datensätze, die von einem **Recordset**-Objekt vom Typ "Tabelle" zurückgegeben werden, können nur nach den Indizes angeordnet werden, die für das zugrunde liegende **TableDef**-Objekt definiert sind. Um Datensätze in einer anderen Reihenfolge zu sortieren, können Sie ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only" öffnen, indem Sie eine SQL-Anweisung mit einer ORDER BY-Klausel verwenden.</span><span class="sxs-lookup"><span data-stu-id="cffe7-p103">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object. To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> - <span data-ttu-id="cffe7-p104">Sie müssen keine Indizes für Tabellen erstellen. Bei großen Tabellen ohne Index kann der Zugriff auf einen bestimmten Datensatz oder das Erstellen eines **Recordset**-Objekts sehr lange dauern. Andererseits kann die Erstellung zu vieler Indizes Update-, Anfüge- und Löschvorgänge verlangsamen, da alle Indizes automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cffe7-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="cffe7-120">Datensätze, die aus Tabellen ohne Indizes gelesen werden, werden in keiner bestimmten Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cffe7-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="cffe7-121">Die **[Attributes](field-attributes-property-dao.md)**-Eigenschaft jedes **[Field](field-object-dao.md)**-Objekts im **Index**-Objekt bestimmt die Reihenfolge der Datensätze und folglich die geeigneten Methoden zum Zugreifen auf diesen Index.</span><span class="sxs-lookup"><span data-stu-id="cffe7-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="cffe7-122">Ein eindeutiger Index trägt zur Optimierung der Suche nach Datensätzen bei.</span><span class="sxs-lookup"><span data-stu-id="cffe7-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="cffe7-123">Indizes wirken sich nicht auf die physische Reihenfolge einer Basistabelle aus, sondern beeinflussen nur, wie vom **Recordset**-Objekt des Typs "Tabelle" auf die Datensätze zugegriffen wird, wenn ein bestimmter Index ausgewählt oder ein **Recordset** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="cffe7-123">Indexes don't affect the physical order of a base table, indexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>


## <a name="example"></a><span data-ttu-id="cffe7-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cffe7-124">Example</span></span>

<span data-ttu-id="cffe7-125">In diesem Beispiel wird die **Index**-Eigenschaft verwendet, um verschiedene Datensatzreihenfolgen für ein **Recordset** vom Typ "Tabelle" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cffe7-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="cffe7-126">Dieses Beispiel veranschaulicht die **Seek**-Methode, indem dem Benutzer erlaubt wird, nach einem Produkt anhand einer ID-Nummer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cffe7-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="cffe7-127">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der Seek-Methode einen Datensatz in einer verknüpften Tabelle finden.</span><span class="sxs-lookup"><span data-stu-id="cffe7-127">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="cffe7-128">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="cffe7-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
