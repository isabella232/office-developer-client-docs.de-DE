---
title: QueryDef.Execute-Methode (DAO)
TOCTitle: Execute Method
ms:assetid: ad9e859e-c6fe-496c-a1f2-a000cf4bebcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821728(v=office.15)
ms:contentKeyID: 48547043
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052884
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 7ef7f61ef632617b8d64a3fd9c34e5887e50065c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302961"
---
# <a name="querydefexecute-method-dao"></a><span data-ttu-id="97200-102">QueryDef.Execute-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="97200-102">QueryDef.Execute Method (DAO)</span></span>

<span data-ttu-id="97200-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97200-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97200-104">Führt eine SQL-Anweisung für das angegebene Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="97200-104">Executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97200-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97200-105">Syntax</span></span>

<span data-ttu-id="97200-106">*expression* .Execute(***Options***)</span><span class="sxs-lookup"><span data-stu-id="97200-106">*expression* .Execute(***Options***)</span></span>

<span data-ttu-id="97200-107">*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="97200-107">*expression*  A variable that represents a **QueryDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="97200-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97200-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97200-109">Name</span><span class="sxs-lookup"><span data-stu-id="97200-109">Name</span></span></p></th>
<th><p><span data-ttu-id="97200-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="97200-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="97200-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="97200-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="97200-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97200-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97200-113"><em>Optionen</em></span><span class="sxs-lookup"><span data-stu-id="97200-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="97200-114">Optional</span><span class="sxs-lookup"><span data-stu-id="97200-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="97200-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="97200-115"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="97200-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97200-116">Remarks</span></span>

<span data-ttu-id="97200-117">Sie können die folgenden **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)**-Konstanten für Options verwenden.</span><span class="sxs-lookup"><span data-stu-id="97200-117">You can use the following  RecordsetOptionEnum  constants for Options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97200-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="97200-118">Constant</span></span></p></th>
<th><p><span data-ttu-id="97200-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97200-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97200-120"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="97200-120"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-121">Verweigert anderen Benutzern die Schreibberechtigung (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97200-121">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97200-122"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="97200-122"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-123">(Standardeinstellung) Führt inkonsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97200-123">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97200-124"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="97200-124"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-125">Führt konsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97200-125">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97200-126"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="97200-126"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-p101">Führt eine SQL-Pass-Through-Abfrage aus. Wenn Sie diese Option festlegen, wird die SQL-Anweisung zur Verarbeitung an eine ODBC-Datenbank übergeben (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97200-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97200-129"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="97200-129"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-130">Führt ein Rollback für Updates aus, wenn ein Fehler auftritt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97200-130">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97200-131"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="97200-131"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-132">Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97200-132">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97200-133"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="97200-133"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-134">Führt die Abfrage asynchron aus (nur ODBCDirect-Connection- und -QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="97200-134">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97200-135"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="97200-135"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="97200-136">Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="97200-136">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="97200-p102">ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="97200-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="97200-p103">Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können die eine oder die andere, nicht jedoch beide in einer bestimmten Instanz von **OpenRecordset** verwenden. Die gemeinsame Verwendung von **dbConsistent** und **dbInconsistent** verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="97200-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="97200-p104">Verwenden Sie die **[RecordsAffected](querydef-recordsaffected-property-dao.md)**-Eigenschaft des **[Connection](connection-object-dao.md)**-, **[Database](database-object-dao.md)**- oder **[QueryDef](querydef-object-dao.md)**-Objekts, um die Anzahl der Datensätze zu bestimmen, die von der letzten **[Execute](querydef-execute-method-dao.md)**-Methode betroffen sind. Beispiel: **RecordsAffected** enthält die Anzahl von Datensätzen, die beim Ausführen einer Aktionsabfrage gelöscht, aktualisiert oder eingefügt werden. Wenn Sie eine Abfrage mit der **Execute**-Methode ausführen, wird die **RecordsAffected**-Eigenschaft des **QueryDef**-Objekts auf die Anzahl der betroffenen Datensätze festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97200-p104">Use the **[RecordsAffected](querydef-recordsaffected-property-dao.md)** property of the **[Connection](connection-object-dao.md)**, **[Database](database-object-dao.md)**, or **[QueryDef](querydef-object-dao.md)** object to determine the number of records affected by the most recent **[Execute](querydef-execute-method-dao.md)** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="97200-p105">Wenn Sie in einem Microsoft Access-Arbeitsbereich eine syntaktisch korrekte SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen, tritt bei der **Execute**-Methode kein Fehler auf, selbst wenn keine einzige Zeile geändert oder gelöscht werden kann. Verwenden Sie daher stets die **dbFailOnError**-Option, wenn Sie eine Update- oder Löschabfrage mit der **Execute** Methode ausführen. Diese Option generiert einen Laufzeitfehler und führt ein Rollback aller erfolgreichen Änderungen durch, wenn einer der betroffenen Datensätze gesperrt ist und nicht aktualisiert oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="97200-p105">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="97200-p106">In früheren Versionen des Microsoft Jet-Datenbankmoduls wurden SQL-Anweisungen automatisch in implizite Transaktionen eingebettet. Wenn bei der Ausführung eines Teils einer Anweisung ein **dbFailOnError**-Fehler auftrat, wurde ein Rollback für die gesamte Anweisung durchgeführt. Um die Leistung zu verbessern, wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie älteren DAO-Code aktualisieren, denken Sie daran, explizite Transaktionen um **Execute**-Anweisungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="97200-p106">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="97200-p107">Um eine optimale Leistung in einem Microsoft Access-Arbeitsbereich, insbesondere in einer Mehrbenutzerumgebung zu erzielen, schachteln Sie die **Execute**-Methode innerhalb einer Transaktion. Führen Sie die **[BeginTrans](workspace-begintrans-method-dao.md)**-Methode für das aktuelle **[Workspace](workspace-object-dao.md)**-Objekt aus, verwenden Sie dann die **Execute**-Methode, und schließen Sie die Transaktion durch Ausführen der **[CommitTrans](workspace-committrans-method-dao.md)**-Methode für das **Workspace**-Objekt ab. Dadurch werden die Änderungen auf Datenträger gespeichert und alle Sperrungen aufgehoben, die während der Ausführung der Abfrage festlegt wurden.</span><span class="sxs-lookup"><span data-stu-id="97200-p107">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **[BeginTrans](workspace-begintrans-method-dao.md)** method on the current **[Workspace](workspace-object-dao.md)** object, then use the **Execute** method, and complete the transaction by using the **[CommitTrans](workspace-committrans-method-dao.md)** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="97200-155">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97200-155">Example</span></span>

<span data-ttu-id="97200-p108">In diesem Beispiel demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="97200-p108">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

```vb
    Sub ExecuteX() 
     
       Dim dbsNorthwind As Database 
       Dim strSQLChange As String 
       Dim strSQLRestore As String 
       Dim qdfChange As QueryDef 
       Dim rstEmployees As Recordset 
       Dim errLoop As Error 
     
       ' Define two SQL statements for action queries. 
       strSQLChange = "UPDATE Employees SET Country = " & _ 
          "'United States' WHERE Country = 'USA'" 
       strSQLRestore = "UPDATE Employees SET Country = " & _ 
          "'USA' WHERE Country = 'United States'" 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Create temporary QueryDef object. 
       Set qdfChange = dbsNorthwind.CreateQueryDef("", _ 
          strSQLChange) 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "SELECT LastName, Country FROM Employees", _ 
          dbOpenForwardOnly) 
     
       ' Print report of original data. 
       Debug.Print _ 
          "Data in Employees table before executing the query" 
       PrintOutput rstEmployees 
        
       ' Run temporary QueryDef. 
       ExecuteQueryDef qdfChange, rstEmployees 
        
       ' Print report of new data. 
       Debug.Print _ 
          "Data in Employees table after executing the query" 
       PrintOutput rstEmployees 
     
       ' Run action query to restore data. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       dbsNorthwind.Execute strSQLRestore, dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstEmployees.Requery 
     
       ' Print report of restored data. 
       Debug.Print "Data after executing the query " & _ 
          "to restore the original information" 
       PrintOutput rstEmployees 
     
       rstEmployees.Close 
        
       Exit Sub 
        
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub ExecuteQueryDef(qdfTemp As QueryDef, _ 
       rstTemp As Recordset) 
     
       Dim errLoop As Error 
        
       ' Run the specified QueryDef object. Trap for errors, 
       ' checking the Errors collection if necessary. 
       On Error GoTo Err_Execute 
       qdfTemp.Execute dbFailOnError 
       On Error GoTo 0 
     
       ' Retrieve the current data by requerying the recordset. 
       rstTemp.Requery 
        
       Exit Sub 
     
    Err_Execute: 
     
       ' Notify user of any errors that result from 
       ' executing the query. 
       If DBEngine.Errors.Count > 0 Then 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
       End If 
        
       Resume Next 
     
    End Sub 
     
    Sub PrintOutput(rstTemp As Recordset) 
     
       ' Enumerate Recordset. 
       Do While Not rstTemp.EOF 
          Debug.Print "  " & rstTemp!LastName & _ 
             ", " & rstTemp!Country 
          rstTemp.MoveNext 
       Loop 
     
    End Sub 
```

<br/>

<span data-ttu-id="97200-158">Im folgenden Beispiel wird gezeigt, wie eine Parameterabfrage ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97200-158">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="97200-159">Die Parameter-Auflistung wird verwendet, um den Organization-Parameter der myActionQuery-Abfrage festzulegen, bevor die Abfrage ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97200-159">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="97200-160">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="97200-160">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
