---
title: QueryDef-Objekt (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301057"
---
# <a name="querydef-object-dao"></a><span data-ttu-id="b303e-102">QueryDef-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="b303e-102">QueryDef Object (DAO)</span></span>

<span data-ttu-id="b303e-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b303e-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="b303e-104">Ein **QueryDef**-Objekt ist eine gespeicherte Definition einer Abfrage in einer Datenbank des Microsoft Access-Datenbankmoduls.</span><span class="sxs-lookup"><span data-stu-id="b303e-104">A **QueryDef** object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="b303e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b303e-105">Remarks</span></span>

<span data-ttu-id="b303e-p101">Sie können das **QueryDef** -Objekt verwenden, um eine Abfrage zu definieren. Sie haben beispielsweise folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="b303e-p101">You can use the **QueryDef** object to define a query. For example, you can:</span></span>

- <span data-ttu-id="b303e-108">Verwenden der **SQL** -Eigenschaft, um die Abfragedefinition festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b303e-108">Use the **SQL** property to set or return the query definition.</span></span>

- <span data-ttu-id="b303e-109">Verwenden der **Parameters** -Auflistung des **QueryDef** -Objekts, um Abfrageparameter festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b303e-109">Use the **QueryDef** object's **Parameters** collection to set or return query parameters.</span></span>

- <span data-ttu-id="b303e-110">Verwenden der **Type** -Eigenschaft, um einen Wert zurückzugeben, der angibt, ob die Abfrage Datensätze aus einer vorhandenen Tabelle auswählt, eine neue Tabelle erstellt, Datensätze aus einer Tabelle in einer anderen Tabelle eingefügt, Datensätze löscht oder Datensätze aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b303e-110">Use the **Type** property to return a value indicating whether the query selects records from an existing table, makes a new table, inserts records from one table into another table, deletes records, or updates records.</span></span>

- <span data-ttu-id="b303e-111">Verwenden der **MaxRecords** -Eigenschaft, um die Anzahl der von einer Abfrage zurückgegebenen Datensätze zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="b303e-111">Use the **MaxRecords** property to limit the number of records returned from a query.</span></span>

- <span data-ttu-id="b303e-p102">Verwenden der **ODBCTimeout** -Eigenschaft, um anzugeben, wie lange gewartet werden soll, bevor die Abfrage Datensätze zurückgibt. Die **ODBCTimeout** -Eigenschaft gilt für alle Abfragen, die auf ODBC-Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b303e-p102">Use the **ODBCTimeout** property to indicate how long to wait before the query returns records. The **ODBCTimeout** property applies to any query that accesses ODBC data.</span></span>

- <span data-ttu-id="b303e-p103">Verwenden der **ReturnsRecords** -Eigenschaft, um anzugeben, dass die Abfrage Datensätze zurückgibt. Die **ReturnsRecords** -Eigenschaft gilt nur für SQL-Pass-Through-Abfragen.</span><span class="sxs-lookup"><span data-stu-id="b303e-p103">Use the **ReturnsRecords** property to indicate that the query returns records. The **ReturnsRecords** property is only valid on SQL pass-through queries.</span></span>

- <span data-ttu-id="b303e-116">Verwenden der **Connect** -Eigenschaft, um eine SQL-Pass-Through-Abfrage für eine ODBC-Datenbank durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="b303e-116">Use the **Connect** property to make an SQL pass-through query to an ODC database.</span></span>

<span data-ttu-id="b303e-p104">Sie können auch temporäre **QueryDef** -Objekte erstellen. Im Gegensatz zu dauerhaften **QueryDef** -Objekten werden temporäre **QueryDef** -Objekte nicht auf Datenträger gespeichert oder an die **QueryDefs** -Auflistung angefügt. Temporäre **QueryDef** -Objekte sind für Abfragen nützlich, die Sie während der Laufzeit wiederholt ausführen, jedoch nicht auf einem Datenträger speichern müssen, insbesondere, wenn Sie die SQL-Anweisungen zur Laufzeit erstellen.</span><span class="sxs-lookup"><span data-stu-id="b303e-p104">You can also create temporary **QueryDef** objects. Unlike permanent **QueryDef** objects, temporary **QueryDef** objects are not saved to disk or appended to the **QueryDefs** collection. Temporary **QueryDef** objects are useful for queries that you must run repeatedly during run time but do not not need to save to disk, particularly if you create their SQL statements during run time.</span></span>

<span data-ttu-id="b303e-p105">Sie können sich ein dauerhaftes **QueryDef** -Objekt in einem Microsoft Access-Arbeitsbereich als kompilierte SQL-Anweisung vorstellen. Wenn Sie eine Abfrage über ein dauerhaftes **QueryDef** -Objekt ausführen, wird die Abfrage schneller ausgeführt als die entsprechende SQL-Anweisung über die **OpenRecordset** -Methode. Dies liegt daran, das das Microsoft Access-Datenbankmodul die Abfrage vor der Ausführung nicht kompilieren muss.</span><span class="sxs-lookup"><span data-stu-id="b303e-p105">You can think of a permanent **QueryDef** object in a Microsoft Access workspace as a compiled SQL statement. If you execute a query from a permanent **QueryDef** object, the query will run faster than if you run the equivalent SQL statement from the **OpenRecordset** method. This is because the Microsoft Access database engine doesn't need to compile the query before executing it.</span></span>

<span data-ttu-id="b303e-p106">Die bevorzugte Methode zum Verwenden des systemeigenen SQL-Dialekts eines externen Datenbankmoduls, auf das über das Microsoft Access-Datenbankmodul zugegriffen wird, ist über **QueryDef** -Objekte. Sie können z. B. eine Microsoft SQL Server-Abfrage erstellen und in einem **QueryDef** -Objekt speichern. Wenn Sie eine SQL-Abfrage aus einem anderen als dem Microsoft Access-Datenbankmodul verwenden möchten, müssen Sie eine **Connect** -Eigenschaftenzeichenfolge angeben, die auf die externe Datenquelle verweist. Abfragen mit gültigen **Connect** -Eigenschaften umgehen das Microsoft Access-Datenbankmodul und übergeben die Abfrage direkt zur Verarbeitung an den externen Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="b303e-p106">The preferred way to use the native SQL dialect of an external database engine accessed through the Microsoft Access database engine is through **QueryDef** objects. For example, you can create a Microsoft SQL Server query and store it in a **QueryDef** object. When you need to use a non-Microsoft Access database engine SQL query, you must provide a **Connect** property string that points to the external data source. Queries with valid **Connect** properties bypass the Microsoft Access database engine and pass the query directly to the external database server for processing.</span></span>

<span data-ttu-id="b303e-127">Um ein neues **QueryDef**-Objekt zu erstellen, verwenden Sie die **CreateQueryDef**-Methode.</span><span class="sxs-lookup"><span data-stu-id="b303e-127">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="b303e-128">Wenn Sie in einem Microsoft Access-Arbeitsbereich eine Zeichenfolge für das name-Argument eingeben oder die **Name**-Eigenschaft des neuen **QueryDef**-Objekts explizit auf eine Zeichenfolge festlegen, deren Länge nicht null ist, erstellen Sie ein permanentes **QueryDef**-Objekt, das automatisch an die **QueryDefs**-Auflistung angehängt und auf dem Datenträger gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b303e-128">In a Microsoft Access workspace, if you supply a string for the  name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non-zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="b303e-129">Wenn Sie eine Zeichenfolge der Länge null als name-Argument eingeben oder die **Name**-Eigenschaft explizit auf eine Zeichenfolge der Länge null festlegen, führt dies zu einem temporären **QueryDef**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b303e-129">Supplying a zero-length string as the  name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="b303e-130">Verwenden Sie eine der folgenden Syntaxformen, um auf ein **QueryDef**-Objekt in einer Auflistung anhand seiner Ordnungszahl oder seiner Einstellung der **Name**-Eigenschaft zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="b303e-130">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="b303e-131">QueryDefs(0)</span><span class="sxs-lookup"><span data-stu-id="b303e-131">QueryDefs(0)</span></span>

<span data-ttu-id="b303e-132">QueryDefs("name")</span><span class="sxs-lookup"><span data-stu-id="b303e-132">QueryDefs("name")</span></span>

<span data-ttu-id="b303e-133">QueryDefs\!\[ name\]</span><span class="sxs-lookup"><span data-stu-id="b303e-133">QueryDefs\!\[ name\]</span></span>

<span data-ttu-id="b303e-134">Auf temporäre **QueryDef**-Objekte können Sie nur anhand der Objektvariablen verweisen, die Sie diesen zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="b303e-134">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

<span data-ttu-id="b303e-135">\*\*Link zur Verfügung gestellt von: \*\* [UtterAccess](https://www.utteraccess.com)-Community.</span><span class="sxs-lookup"><span data-stu-id="b303e-135">**Link provided by:Community Member Icon** The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="b303e-136">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="b303e-136">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="b303e-137">Abfragen: Dokument-SQL für Word</span><span class="sxs-lookup"><span data-stu-id="b303e-137">Queries: Document SQL to Word</span></span>](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a><span data-ttu-id="b303e-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b303e-138">Example</span></span>

<span data-ttu-id="b303e-p109">Mit diesem Beispiel wird ein neues **QueryDef**-Objekt erstellt, das an die **QueryDefs**-Auflistung des **Database**-Objekts der Northwind-Datenbank angehängt wird. Anschließend werden die **QueryDefs**-Auflistung und die **Properties**-Auflistung des neuen **QueryDef**-Objekts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b303e-p109">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="b303e-141">In diesem Beispiel wird die **CreateQueryDef**-Methode verwendet, um ein temporäres und ein dauerhaftes **QueryDef**-Objekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b303e-141">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="b303e-142">Die GetrstTemp-Funktion wird zur Ausführung dieses Verfahrens benötigt.</span><span class="sxs-lookup"><span data-stu-id="b303e-142">The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="b303e-143">Das folgende Beispiel zeigt, wie Sie die Structured Query Language (SQL)-Anweisung in einer gespeicherten Abfrage ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b303e-143">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

<span data-ttu-id="b303e-144">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b303e-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    ‘To change the Where clause in a saved query  
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
        Dim strSELECT As String, strWhere As String
        Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
        Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
            strGROUPBY, strHAVING)
    
        ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
            & strGROUPBY &""& strHAVING &""& strOrderBy
    
        Exit_Procedure:
            Exit Function
    
        Error_Handler:
            MsgBox (Err.Number & ": " & Err.Description)
            Resume Exit_Procedure
    
    End Function
```

