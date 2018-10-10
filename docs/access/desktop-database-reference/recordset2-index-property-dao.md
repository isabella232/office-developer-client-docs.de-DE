---
title: Recordset2.Index Property (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad875f1aba667924d5e00dc9990fd09b6826947d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474739"
---
# <a name="recordset2index-property-dao"></a><span data-ttu-id="1e6ad-102">Recordset2.Index Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e6ad-102">Recordset2.Index Property (DAO)</span></span>


<span data-ttu-id="1e6ad-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e6ad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1e6ad-104">Legt einen Wert fest, der den Namen des aktuellen **[Index](index-object-dao.md)** -Objekts in einem **[Recordset](recordset-object-dao.md)** -Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="1e6ad-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e6ad-105">Syntax</span></span>

<span data-ttu-id="1e6ad-106">*Ausdruck* . Index</span><span class="sxs-lookup"><span data-stu-id="1e6ad-106">*expression* .Index</span></span>

<span data-ttu-id="1e6ad-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6ad-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e6ad-108">Remarks</span></span>

<span data-ttu-id="1e6ad-p101">Datensätze in Basistabellen werden nicht in einer bestimmten Reihenfolge gespeichert. Durch Festlegen der **Index** -Eigenschaft wird die Reihenfolge der von der Datenbank zurückgegebenen Datensätze geändert. Auf die Speicherreihenfolge der Datensätze hat dies keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="1e6ad-p102">Das angegebene **Index** -Objekt muss bereits definiert sein. Wenn Sie die **Index** -Eigenschaft auf ein **Index** -Objekt festlegen, das nicht vorhanden ist, oder wenn die **Index** -Eigenschaft nicht festgelegt ist, tritt bei Verwendung der **[Seek](recordset2-seek-method-dao.md)** -Methode ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset2-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="1e6ad-113">Untersuchen Sie die **Indexes** -Sammlung eines **TableDef** -Objekts, um zu bestimmen, welche **Index** -Objekte für **Recordset** -Objekte vom Typ "Tabelle" zur Verfügung stehen, die aus diesem **TableDef** -Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="1e6ad-114">Sie können einen neuen Index für die Tabelle erstellen, indem Sie ein neues **Index** -Objekt erstellen, die zugehörigen Eigenschaften festlegen, es an die **Indexes** -Sammlung des zugrunde liegenden **TableDef** -Objekts anfügen und anschließend das **Recordset** -Objekt erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="1e6ad-115">Datensätze, die von einem **Recordset** -Objekt vom Typ "Tabelle" zurückgegeben werden, können nur nach den Indizes angeordnet werden, die für das zugrunde liegende **TableDef** -Objekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="1e6ad-116">Um Datensätze in einer anderen Reihenfolge zu sortieren, können Sie mithilfe einer SQL-Anweisung mit einer ORDER BY-Klausel einer Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="1e6ad-p104">Sie brauchen keine Indizes für Tabellen zu erstellen. Bei großen, nicht-indizierten Tabellen kann der Zugriff auf einen spezifischen Datensatz oder die Erstellung eines <STRONG>Recordset</STRONG>-Objekts einige Zeit in Anspruch nehmen. Andererseits werden Aktualisierungs-, Anhänge- und Löschvorgänge durch das Erstellen zu vieler Indizes verlangsamt, da alle Indizes automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a <STRONG>Recordset</STRONG> object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span></P>
> <LI>
> <P><span data-ttu-id="1e6ad-120">Datensätze, die aus Tabellen ohne Indizes eingelesen werden, werden in einer unbestimmten Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-120">Records read from tables without indexes are returned in no particular sequence.</span></span></P>
> <LI>
> <P><span data-ttu-id="1e6ad-121">Die <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> -Eigenschaft der einzelnen <STRONG><A href="field-object-dao.md">Field</A></STRONG> -Objekte im <STRONG>Index</STRONG>-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher die für den betreffenden Index zu verwendenden Zugriffsverfahren.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-121">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that index.</span></span></P>
> <LI>
> <P><span data-ttu-id="1e6ad-122">Mithilfe eines eindeutigen Indexes wird die Suche nach Datensätzen optimiert.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-122">A unique index helps optimize finding records.</span></span></P>
> <LI>
> <P><span data-ttu-id="1e6ad-123">Indizes haben keinen Einfluss auf die physikalische Reihenfolge einer Basistabelle. Indizes beeinflussen nur, wie ein Recordset-Objekt des Typs Tabelle auf Datensätze zugreift, wenn ein bestimmter Index gewählt wird oder ein Recordset-Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-123">Indexes don't affect the physical order of a base tableindexes affect only how the records are accessed by the table-type <STRONG>Recordset</STRONG> object when a particular index is chosen or when <STRONG>Recordset</STRONG> is opened.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="1e6ad-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1e6ad-124">Example</span></span>

<span data-ttu-id="1e6ad-125">In diesem Beispiel wird die **Index** -Eigenschaft verwendet, um verschiedene Datensatzreihenfolgen für ein **Recordset** vom Typ "Tabelle" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
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

<span data-ttu-id="1e6ad-126">Dieses Beispiel veranschaulicht die **Seek** -Methode, indem dem Benutzer erlaubt wird, anhand einer ID-Nummer nach einem Produkt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1e6ad-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
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
