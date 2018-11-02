---
title: Database.CreateQueryDef-Methode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e6a6fe546f862f2452ac992c140a63959e48a6b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919745"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="9be4f-102">Database.CreateQueryDef-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="9be4f-102">Database.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="9be4f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9be4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9be4f-104">Erstellt ein neues **[QueryDef](querydef-object-dao.md)** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9be4f-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be4f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9be4f-105">Syntax</span></span>

<span data-ttu-id="9be4f-106">*Ausdruck* . CreateQueryDef (***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="9be4f-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="9be4f-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9be4f-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="9be4f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9be4f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9be4f-109">Name</span><span class="sxs-lookup"><span data-stu-id="9be4f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9be4f-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="9be4f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="9be4f-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9be4f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="9be4f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9be4f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9be4f-113">Name</span><span class="sxs-lookup"><span data-stu-id="9be4f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="9be4f-114">Optional</span><span class="sxs-lookup"><span data-stu-id="9be4f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="9be4f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9be4f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9be4f-116">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="9be4f-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9be4f-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="9be4f-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="9be4f-118">Optional</span><span class="sxs-lookup"><span data-stu-id="9be4f-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="9be4f-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9be4f-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9be4f-p101">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), bei er es sich um eine SQL Anweisung handelt, die die <strong>QueryDef</strong> definiert. Wenn dieses Argument ausgelassen wird, können Sie die <strong>QueryDef</strong> durch Festlegen ihrer <strong><a href="querydef-sql-property-dao.md">SQL</a></strong>-Eigenschaft definieren, bevor oder nachdem Sie sie an eine Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="9be4f-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9be4f-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9be4f-122">Return value</span></span>

<span data-ttu-id="9be4f-123">QueryDef-Objekt</span><span class="sxs-lookup"><span data-stu-id="9be4f-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="9be4f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9be4f-124">Remarks</span></span>

<span data-ttu-id="9be4f-125">Wenn Sie in einem Microsoft Access-Arbeitsbereich beim Erstellen eines **QueryDef**-Objekts für den Namen einen anderen Wert angeben als eine leere Zeichenfolge, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)** -Auflistung angefügt.</span><span class="sxs-lookup"><span data-stu-id="9be4f-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="9be4f-126">Wenn das durch Name angegebene Objekt bereits ein Mitglied der **QueryDefs** -Auflistung ist, tritt ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="9be4f-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="9be4f-127">Sie können eine temporäre **QueryDef-Objekt** erstellen, indem Sie eine leere Zeichenfolge für das Namenargument verwenden, wenn Sie die **CreateQueryDef** -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="9be4f-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="9be4f-128">Sie können aber auch die **[Name](querydef-name-property-dao.md)** -Eigenschaft eines neu erstellten **QueryDef**-Objekts auf eine leere Zeichenfolge ("") festlegen.</span><span class="sxs-lookup"><span data-stu-id="9be4f-128">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="9be4f-129">Temporäre **QueryDef**-Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen mehrmals verwenden möchten, ohne dass Sie neue permanente Objekte in der **QueryDefs**-Auflistung erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="9be4f-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="9be4f-130">Sie können ein temporäres **QueryDef**-Objekt nicht an jede Auflistung anfügen, da eine leere Zeichenfolge kein gültiger Name für ein permanentes **QueryDef**-Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="9be4f-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="9be4f-131">Sie haben jedoch immer die Möglichkeit, die **Name**- und **SQL**-Eigenschaften des neu erstellten **QueryDef**-Objekts festzulegen und anschließend das **QueryDef**-Objekt an die **QueryDefs**-Auflistung anzufügen.</span><span class="sxs-lookup"><span data-stu-id="9be4f-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="9be4f-132">Verwenden Sie zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt die **[Execute](querydef-execute-method-dao.md)** - oder **[OpenRecordset](database-openrecordset-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="9be4f-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="9be4f-133">Das Verwenden eines **QueryDef**-Objekts ist die empfohlene Methode für SQL Pass-Through-Abfragen in ODBC-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="9be4f-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="9be4f-134">Um ein **QueryDef** -Objekt aus einer **QueryDefs** -Auflistung in einer Datenbank des Microsoft Access-Datenbankmoduls zu entfernen, führen Sie die **[Delete](querydefs-delete-method-dao.md)** -Methode für die Auflistung aus.</span><span class="sxs-lookup"><span data-stu-id="9be4f-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="9be4f-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9be4f-135">Example</span></span>

<span data-ttu-id="9be4f-p104">In diesem Beispiel wird die **CreateQueryDef** -Methode verwendet, um ein temporäres und ein dauerhaftes **QueryDef** -Objekt zu erstellen und auszuführen. Die GetrstTemp-Funktion wird zur Ausführung dieses Verfahrens benötigt.</span><span class="sxs-lookup"><span data-stu-id="9be4f-p104">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="9be4f-p105">Dieses Beispiel verwendet die **CreateQueryDef** - und **OpenRecordset** -Methode sowie die **SQL** -Eigenschaft zum Abfragen der Tabelle mit Titeln in der Microsoft SQL Server-Beispieldatenbank „Publikationen" und zum Zurückgeben des Titels und der Titel-ID des Bestsellers. Anschließend wird die Tabelle mit Autoren abgefragt, und der Benutzer wird angewiesen, einen Bonusscheck an jeden Autor zu senden, der auf dem jeweiligen Tantiemenanteil des Autors basiert (der Gesamtbonus beträgt 1.000 $, und jeder Autor soll einen Prozentsatz dieses Betrags erhalten).</span><span class="sxs-lookup"><span data-stu-id="9be4f-p105">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="9be4f-140">Das folgende Beispiel zeigt, wie Sie eine Parameterabfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="9be4f-140">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="9be4f-141">Eine Abfrage namens **MyQuery** wird mit zwei Parameter, mit dem Namen Param1 und Param2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="9be4f-141">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="9be4f-142">Hierzu wird die SQL-Eigenschaft der Abfrage auf eine SQL-Anweisung (Structured Query Language) festgelegt, die die Parameter definiert.</span><span class="sxs-lookup"><span data-stu-id="9be4f-142">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="9be4f-143">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9be4f-143">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
