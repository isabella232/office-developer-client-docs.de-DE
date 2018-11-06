---
title: Database.Execute-Methode (DAO)
TOCTitle: Execute method
ms:assetid: 9294d530-f70f-e1ed-3990-ce128de4378b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197654(v=office.15)
ms:contentKeyID: 48546378
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13568f689d9e5b4e4533969192de7af65ea1f8ec
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997826"
---
# <a name="databaseexecute-method-dao"></a><span data-ttu-id="2b366-102">Database.Execute-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b366-102">Database.Execute method (DAO)</span></span>

<span data-ttu-id="2b366-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b366-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b366-104">Führt eine Aktionsabfrage oder eine SQL-Anweisung für das angegebene Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="2b366-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b366-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b366-105">Syntax</span></span>

<span data-ttu-id="2b366-106">*Ausdruck* . Führen Sie (***Abfrage***, ***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="2b366-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="2b366-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b366-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b366-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b366-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b366-109">Name</span><span class="sxs-lookup"><span data-stu-id="2b366-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2b366-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="2b366-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2b366-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2b366-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2b366-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b366-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b366-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="2b366-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="2b366-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b366-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2b366-115"><strong>Zeichenfolge</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-115"><strong>String</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b366-116"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="2b366-116"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="2b366-117">Optional</span><span class="sxs-lookup"><span data-stu-id="2b366-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="2b366-118"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-118"><strong>Variant</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b366-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b366-119">Remarks</span></span>

<span data-ttu-id="2b366-120">Sie können die folgenden **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** -Konstanten für Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b366-120">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b366-121">Konstante</span><span class="sxs-lookup"><span data-stu-id="2b366-121">Constant</span></span></p></th>
<th><p><span data-ttu-id="2b366-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b366-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b366-123"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-123"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-124">Verweigert anderen Benutzern die Schreibberechtigung (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2b366-124">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b366-125"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-125"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-126">(Standardeinstellung) Führt inkonsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2b366-126">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b366-127"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-127"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-128">Führt konsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2b366-128">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b366-129"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-129"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-p101">Führt eine SQL-Pass-Through-Abfrage aus. Wenn Sie diese Option festlegen, wird die SQL-Anweisung zur Verarbeitung an eine ODBC-Datenbank übergeben (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2b366-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b366-132"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-132"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-133">Führt ein Rollback für Updates aus, wenn ein Fehler auftritt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2b366-133">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b366-134"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-134"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-135">Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2b366-135">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b366-136"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-136"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-137">Führt die Abfrage asynchron aus (nur ODBCDirect-Connection- und -QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="2b366-137">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b366-138"><strong>Bei der Ausführung</strong></span><span class="sxs-lookup"><span data-stu-id="2b366-138"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="2b366-139">Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="2b366-139">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="2b366-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="2b366-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="2b366-p103">[!HINWEIS] Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können eins von beiden, jedoch nicht beide in einer angegebenen Instanz von **OpenRecordset** verwenden. Durch die Verwendung der **dbConsistent** - und **dbInconsistent** -Konstanten wird ein Fehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="2b366-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="2b366-p104">Die **Execute**-Methode gilt nur für Aktionsabfragen. Wenn Sie **Execute** mit einem anderen Abfragetyp verwenden, tritt ein Fehler auf. Da bei einer Aktionsabfrage keine Datensätze zurückgegeben werden, gibt **Execute** kein **Recordset**-Objekt zurück. (Das Durchführen einer SQL Pass-Through-Abfrage in einem ODBCDirect-Arbeitsbereich gibt keinen Fehler zurück, wenn kein **Recordset** zurückgegeben wird.)</span><span class="sxs-lookup"><span data-stu-id="2b366-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="2b366-p105">Mit der **RecordsAffected**-Eigenschaft des **Connection**-, **Database**- oder **QueryDef**-Objekts können Sie die Anzahl von Datensätzen bestimmen, die von der aktuellsten **Execute**-Methode betroffen sind. So umfasst **RecordsAffected** beispielsweise die Anzahl von Datensätzen, die beim Ausführen einer Aktionsabfrage gelöscht, aktualisiert oder eingefügt wurden. Wenn Sie zum Ausführen einer Abfrage die **Execute**-Methode verwenden, ist die **RecordsAffected**-Eigenschaft des **QueryDef**-Objekts auf die Anzahl von betroffenen Datensätzen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b366-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="2b366-p106">Wenn Sie in einem Microsoft Access-Arbeitsbereich eine syntaktisch richtige SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen, schlägt die **Execute**-Methode nicht fehl, auch wenn keine einzelne Zeile geändert oder gelöscht werden kann. Daher sollten Sie immer mit der **dbFailOnError**-Option arbeiten, wenn Sie mit der **Execute**-Methode eine Aktualisierung ausführen oder eine Abfrage löschen. Mit dieser Option wird ein Laufzeitfehler generiert, und für alle erfolgreichen Änderungen wird ein Rollback durchgeführt, wenn einer der betroffenen Datensätze gesperrt ist und nicht aktualisiert oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b366-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="2b366-p107">In früheren Versionen des Microsoft Jet-Datenbankmoduls wurden SQL-Anweisungen automatisch in implizite Transaktionen eingebettet. Würde ein Teil einer mit **dbFailOnError** ausgeführten Anweisung fehlschlagen, würde für die Anweisung ein Rollback durchgeführt. Zur Leistungssteigerung wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie älteren DAO-Code aktualisieren, sollten Sie auf jeden Fall explizite Transaktionen bei **Execute**-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b366-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="2b366-p108">Um die beste Leistung in einem Microsoft Access-Arbeitsbereich zu erzielen, insbesondere in einer Mehrbenutzerumgebung, schachteln Sie die **Execute** -Methode innerhalb einer Transaktion. Verwenden Sie die **BeginTrans** -Methode bei dem aktuellen **Workspace** -Objekt, und anschließend die **Execute** -Methode, und vervollständigen Sie die Transaktion mithilfe der **CommitTrans** -Methode im **Arbeitsbereich**. Dadurch werden die Änderungen auf einem Datenträger gespeichert und während der Ausführung der Abfrage eingesetzte Sperren aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="2b366-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

## <a name="example"></a><span data-ttu-id="2b366-162">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b366-162">Example</span></span>

<span data-ttu-id="2b366-p109">In diesem Beispiel demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="2b366-p109">This example demonstrates the **Execute** method when run from both a **QueryDef** object and a **Database** object. The ExecuteQueryDef and PrintOutput procedures are required for this procedure to run.</span></span>

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
     Debug.Print " " & rstTemp!LastName & _ 
     ", " & rstTemp!Country 
     rstTemp.MoveNext 
     Loop 
     
    End Sub
```
