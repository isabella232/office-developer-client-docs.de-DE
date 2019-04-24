---
title: QueryDef.SQL-Eigenschaft (DAO)
TOCTitle: SQL property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c51f0da8541cf0ba2790827c58a0b017bd6ed875
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300980"
---
# <a name="querydefsql-property-dao"></a><span data-ttu-id="9a2c4-102">QueryDef.SQL-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a2c4-102">QueryDef.SQL Property (DAO)</span></span>

<span data-ttu-id="9a2c4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a2c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a2c4-104">Legt die SQL-Anweisung fest, die die Abfrage definiert, die von einem **[QueryDef](querydef-object-dao.md)**-Objekt ausgeführt wird, oder gibt sie zurück.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-104">Sets or returns the SQL statement that defines the query executed by a **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a2c4-105">Syntax</span></span>

<span data-ttu-id="9a2c4-106">*Ausdruck* .SQL</span><span class="sxs-lookup"><span data-stu-id="9a2c4-106">expression  . SQL</span></span>

<span data-ttu-id="9a2c4-107">*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-107">*expression*  A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a2c4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a2c4-108">Remarks</span></span>

<span data-ttu-id="9a2c4-p101">Die **SQL**-Eigenschaft enthält die SQL-Anweisung, die festlegt, wie viele Datensätze ausgewählt, gruppiert und sortiert werden, wenn Sie die Abfrage ausführen. Sie können die Abfrage verwenden, um Datensätze auszuwählen, die in ein **[Recordset](recordset-object-dao.md)**-Objekt einbezogen werden sollen. Sie können auch Aktionsabfragen definieren, um Daten zu ändern, ohne Datensätze zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-p101">The **SQL** property contains the SQL statement that determines how records are selected, grouped, and ordered when you execute the query. You can use the query to select records to include in a **[Recordset](recordset-object-dao.md)** object. You can also define action queries to modify data without returning records.</span></span>

<span data-ttu-id="9a2c4-p102">Die in einer Abfrage verwendete SQL-Syntax muss dem SQL-Dialekt des Abfragemoduls entsprechen, der vom Typ des Arbeitsbereichs festgelegt wird. In einem Microsoft Access-Arbeitsbereich verwenden Sie den Microsoft Access SQL-Dialekt, außer Sie erstellen eine SQL Pass-Through-Abfrage. In diesem Fall sollten Sie den Dialekt des Servers verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-p102">The SQL syntax used in a query must conform to the SQL dialect of the query engine, which is determined by the type of workspace. In a Microsoft Access workspace, use the Microsoft Access SQL dialect, unless you create an SQL pass-through query, in which case you should use the dialect of the server.</span></span>

<span data-ttu-id="9a2c4-p103">Wenn die SQL-Anweisung Parameter für die Abfrage enthält, müssen Sie sie vor der Ausführung festlegen. Wenn Sie die Parameter nicht neu festlegen, werden bei jeder Ausführung der Abfrage jeweils dieselben Parameterwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-p103">If the SQL statement includes parameters for the query, you must set these before execution. Until you reset the parameters, the same parameter values are applied each time you execute the query.</span></span>

<span data-ttu-id="9a2c4-116">In einem Microsoft Access-Arbeitsbereich wird vorzugsweise ein **QueryDef**-Objekt verwendet, um SQL Pass-Through-Vorgänge auf ODBC-Datenquellen auszuführen, die mit einer Microsoft Access-Datenbank-Engine verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-116">In a Microsoft Access workspace, using a **QueryDef** object is the preferred way to perform SQL pass-through operations on Microsoft Access database engine-connected ODBC data sources.</span></span> <span data-ttu-id="9a2c4-117">Wenn Sie für die **[Connect](querydef-connect-property-dao.md)**-Eigenschaft des **QueryDef**-Objekts eine ODBC-Datenquelle festlegen, können Sie einen anderen SQL-Dialekt als Microsoft Access-Datenbank-SQL in der Abfrage verwenden und an den externen Server übergeben.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-117">By setting the **QueryDef** object's [**Connect**](querydef-connect-property-dao.md) property to an ODBC data source, you can use non–Microsoft–Access–database SQL in the query to be passed to the external server.</span></span> <span data-ttu-id="9a2c4-118">Sie können z. B. TRANSACT SQL-Anweisungen verwenden (mit Microsoft SQL Server- oder Sybase SQL Server-Datenbanken), die die Microsoft Access-Datenbank-Engine andernfalls nicht verarbeiten würde.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-118">For example, you can use TRANSACT SQL statements (with Microsoft SQL Server or Sybase SQL Server databases), which the Microsoft Access database engine would otherwise not process.</span></span>

> [!NOTE]
> <span data-ttu-id="9a2c4-119">Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Wert verkettet ist, bei dem es sich nicht um eine Ganzzahl handelt, und die Systemparameter ein anderes als das US-amerikanische Dezimaltrennzeichen festlegen, wie etwa ein Komma (z. B. `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`), tritt ein Fehler auf, wenn Sie versuchen, das **QueryDef**-Objekt in einer Microsoft Access-Datenbank auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-119">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice`strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`, and lngPrice = 125,50), an error will result when you try to execute the **QueryDef** object in a Microsoft Access database engine database.</span></span> <span data-ttu-id="9a2c4-120">Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-120">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="9a2c4-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a2c4-121">Example</span></span>

<span data-ttu-id="9a2c4-122">In diesem Beispiel wird die **SQL**-Eigenschaft veranschaulicht, indem die **SQL**-Eigenschaft eines temporären **QueryDef**-Objekts festgelegt und geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-122">This example demonstrates the **SQL** property by setting and changing the **SQL** property of a temporary **QueryDef** and comparing the results.</span></span> <span data-ttu-id="9a2c4-123">Zum Ausführen dieser Prozedur ist die SQLOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-123">The SQLOutput function is required for this procedure to run.</span></span>

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="9a2c4-p107">Im folgenden Beispiel wird die **CopyQueryDef**-Methode verwendet, um eine Kopie eines **QueryDef**-Objekts anhand eines vorhandenen **Recordset**-Objekts zu erstellen. Die Kopie wird verändert, indem der **SQL**-Eigenschaft eine Klausel hinzugefügt wird. Wenn Sie ein dauerhaftes **QueryDef**-Objekt erstellen, können der **SQL**-Eigenschaft Leerzeichen, Semikolons oder Zeilenvorschübe hinzugefügt werden. Diese zusätzlichen Zeichen müssen entfernt werden, bevor die neuen Klauseln in die SQL-Anweisung eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-p107">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the **SQL** property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the **SQL** property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="9a2c4-126">Dieses Beispiel zeigt eine mögliche Verwendung von CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="9a2c4-126">This example shows a possible use of CopyQueryNew().</span></span> 
     
```vb
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="9a2c4-p108">In diesem Beispiel werden die **CreateQueryDef**- und die **OpenRecordset**-Methode sowie die **SQL**-Eigenschaft verwendet, um die Tabelle der Titel in der Microsoft SQL Server-Beispieldatenbank "Pubs" abzufragen und den Titel und die Titel-ID des Bestsellers zurückzugeben. Anschließend wird die Tabelle der Autoren abgefragt, und der Benutzer wird angewiesen, einen Bonusscheck an jeden Autor zu senden, der auf dem jeweiligen Tantiemenanteil des Autors basiert (der Gesamtbonus beträgt 1.000 $, und jeder Autor soll einen Prozentsatz dieses Betrags erhalten).</span><span class="sxs-lookup"><span data-stu-id="9a2c4-p108">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb
    Sub ClientServerX2() 
     
       Dim dbsCurrent As Database 
       Dim qdfBestSellers As QueryDef 
       Dim qdfBonusEarners As QueryDef 
       Dim rstTopSeller As Recordset 
       Dim rstBonusRecipients As Recordset 
       Dim strAuthorList As String 
     
       ' Open a database from which QueryDef objects can be  
       ' created. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a temporary QueryDef object to retrieve 
       ' data from a Microsoft SQL Server database. 
       Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
       With qdfBestSellers 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT title, title_id FROM titles " & _ 
             "ORDER BY ytd_sales DESC" 
          Set rstTopSeller = .OpenRecordset() 
          rstTopSeller.MoveFirst 
       End With 
     
       ' Create a temporary QueryDef to retrieve data from 
       ' a Microsoft SQL Server database based on the results from 
       ' the first query. 
       Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
       With qdfBonusEarners 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT * FROM titleauthor " & _ 
             "WHERE title_id = '" & _ 
             rstTopSeller!title_id & "'" 
          Set rstBonusRecipients = .OpenRecordset() 
       End With 
     
       ' Build the output string. 
       With rstBonusRecipients 
          Do While Not .EOF 
             strAuthorList = strAuthorList & "  " & _ 
                !au_id & ":  $" & (10 * !royaltyper) & vbCr 
             .MoveNext 
          Loop 
       End With 
     
       ' Display results. 
       MsgBox "Please send a check to the following " & _ 
          "authors in the amounts shown:" & vbCr & _ 
          strAuthorList & "for outstanding sales of " & _ 
          rstTopSeller!Title & "." 
     
       rstTopSeller.Close 
       dbsCurrent.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="9a2c4-129">Im folgenden Beispiel wird gezeigt, wie eine Parameterabfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-129">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="9a2c4-130">Eine Abfrage mit dem Namen **myQuery** wird mit zwei Parametern, Param1 und Param2, erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-130">A query named myQuery is created with two parameters, named  Param1 and  Param2.</span></span> <span data-ttu-id="9a2c4-131">Zu diesem Zweck wird die SQL-Eigenschaft der Abfrage auf eine SQL-Anweisung (Structured Query Language) festgelegt, die die Parameter definiert.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-131">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="9a2c4-132">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9a2c4-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="9a2c4-133">Das folgende Beispiel zeigt, wie Sie die SQL-Anweisung (Structured Query Language) in einer gespeicherten Abfrage ersetzen.</span><span class="sxs-lookup"><span data-stu-id="9a2c4-133">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

```vb
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
