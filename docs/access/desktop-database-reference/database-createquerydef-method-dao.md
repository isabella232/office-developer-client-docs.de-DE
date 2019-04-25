---
title: Database.CreateQueryDef-Methode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c19ef8ab8ef2e937ba7467b3695f9aa5780c21c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294981"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="aa471-102">Database.CreateQueryDef-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa471-102">Database.CreateQueryDef Method (DAO)</span></span>

<span data-ttu-id="aa471-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa471-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa471-104">Erstellt ein neues **[QueryDef](querydef-object-dao.md)**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="aa471-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa471-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa471-105">Syntax</span></span>

<span data-ttu-id="aa471-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="aa471-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="aa471-107">*Ausdruck* Eine Variable, die ein **Database**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa471-107">*expression*  A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa471-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa471-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa471-109">Name</span><span class="sxs-lookup"><span data-stu-id="aa471-109">Name</span></span></p></th>
<th><p><span data-ttu-id="aa471-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="aa471-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="aa471-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aa471-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="aa471-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa471-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa471-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="aa471-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="aa471-114">Optional</span><span class="sxs-lookup"><span data-stu-id="aa471-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="aa471-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="aa471-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="aa471-116">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), die die neue <strong>QueryDef</strong> eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="aa471-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa471-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="aa471-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="aa471-118">Optional</span><span class="sxs-lookup"><span data-stu-id="aa471-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="aa471-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="aa471-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="aa471-120">Eine <strong>Variant</strong> (Untertyp <strong>String</strong>), bei der es sich um eine SQL-Anweisung handelt, die die <strong>QueryDef</strong> definiert.</span><span class="sxs-lookup"><span data-stu-id="aa471-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="aa471-121">Wenn dieses Argument ausgelassen wird, können Sie die <strong>QueryDef</strong> durch Festlegen ihrer <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> -Eigenschaft definieren, bevor oder nachdem Sie sie an eine Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="aa471-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="aa471-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa471-122">Return value</span></span>

<span data-ttu-id="aa471-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="aa471-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="aa471-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa471-124">Remarks</span></span>

<span data-ttu-id="aa471-125">Wenn Sie in einem Microsoft Access-Arbeitsbereich bei der Erstellung einer **QueryDef** einen anderen Wert als eine Zeichenfolge der Länge 0 (null) für den Namen angeben, wird das resultierende **QueryDef**-Objekt automatisch an die **[QueryDefs](querydefs-collection-dao.md)**-Auflistung angefügt.</span><span class="sxs-lookup"><span data-stu-id="aa471-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="aa471-126">Wenn das von name angegebene Objekt bereits ein Mitglied der **QueryDefs**-Auflistung ist, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="aa471-126">If the object specified by  name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="aa471-127">Sie können eine temporäre **QueryDef** erstellen, indem Sie beim Ausführen der CreateQueryDef-Methode eine Zeichenfolge der Länge 0 (null) für das **name**-Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa471-127">You can create a temporary **QueryDef** by using a zero-length string for the  name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="aa471-128">Ein andere Methode besteht darin, die **[Name](querydef-name-property-dao.md)** -Eigenschaft einer neu erstellten **QueryDef** auf eine Zeichenfolge der Länge 0 ("") festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aa471-128">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="aa471-129">Temporäre **QueryDef** -Objekte sind nützlich, wenn Sie dynamische SQL-Anweisungen wiederholt verwenden möchten, ohne neue dauerhafte Objekte in der **QueryDefs** -Auflistung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa471-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="aa471-130">Sie können eine temporäre **QueryDef** nicht an eine Auflistung anfügen, da eine Zeichenfolge der Länge 0 (null) kein gültiger Name für ein dauerhaftes **QueryDef** -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="aa471-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="aa471-131">Sie können immer die Eigenschaften **Name** und **SQL** des neu erstellten **QueryDef** -Objekts festlegen und die **QueryDef** anschließend an die **QueryDefs** -Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="aa471-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="aa471-132">Zum Ausführen der SQL-Anweisung in einem **QueryDef**-Objekt verwenden Sie die **[Execute](querydef-execute-method-dao.md)**- oder die **[OpenRecordset](database-openrecordset-method-dao.md)**-Methode.</span><span class="sxs-lookup"><span data-stu-id="aa471-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="aa471-133">Die Verwendung eines **QueryDef**-Objekts ist das bevorzugte Verfahren zum Ausführen von SQL-Pass-Through-Abfragen mit ODBC-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="aa471-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="aa471-134">Um ein **QueryDef**-Objekt aus einer **QueryDefs**-Auflistung in einer Datenbank des Microsoft Access-Datenbankmoduls zu entfernen, führen Sie die **[Delete](querydefs-delete-method-dao.md)**-Methode für die Auflistung aus.</span><span class="sxs-lookup"><span data-stu-id="aa471-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="aa471-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa471-135">Example</span></span>

<span data-ttu-id="aa471-136">In diesem Beispiel wird die **CreateQueryDef**-Methode verwendet, um ein temporäres und ein dauerhaftes **QueryDef**-Objekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="aa471-136">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="aa471-137">Die GetrstTemp-Funktion wird zur Ausführung dieses Verfahrens benötigt.</span><span class="sxs-lookup"><span data-stu-id="aa471-137">The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="aa471-p105">In diesem Beispiel werden die **CreateQueryDef**- und die **OpenRecordset**-Methode sowie die **SQL**-Eigenschaft verwendet, um die Tabelle der Titel in der Microsoft SQL Server-Beispieldatenbank "Pubs" abzufragen und den Titel und die Titel-ID des Bestsellers zurückzugeben. Anschließend wird die Tabelle der Autoren abgefragt, und der Benutzer wird angewiesen, einen Bonusscheck an jeden Autor zu senden, der auf dem jeweiligen Tantiemenanteil des Autors basiert (der Gesamtbonus beträgt 1.000 $, und jeder Autor soll einen Prozentsatz dieses Betrags erhalten).</span><span class="sxs-lookup"><span data-stu-id="aa471-p105">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="aa471-140">Im folgenden Beispiel wird gezeigt, wie eine Parameterabfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="aa471-140">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="aa471-141">Eine Abfrage mit dem Namen **myQuery** wird mit zwei Parametern, Param1 und Param2, erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa471-141">A query named myQuery is created with two parameters, named  Param1 and  Param2.</span></span> <span data-ttu-id="aa471-142">Zu diesem Zweck wird die SQL-Eigenschaft der Abfrage auf eine SQL-Anweisung (Structured Query Language) festgelegt, die die Parameter definiert.</span><span class="sxs-lookup"><span data-stu-id="aa471-142">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="aa471-143">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="aa471-143">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
