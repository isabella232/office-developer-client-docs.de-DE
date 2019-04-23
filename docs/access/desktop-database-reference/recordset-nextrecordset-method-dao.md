---
title: Recordset. NextRecordset-Methode (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 39e508830b41e7b3f74f548451a30132723d210f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284497"
---
# <a name="recordsetnextrecordset-method-dao"></a><span data-ttu-id="9de2b-102">Recordset. NextRecordset-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="9de2b-102">Recordset.NextRecordset method (DAO)</span></span>


<span data-ttu-id="9de2b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9de2b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9de2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9de2b-104">Syntax</span></span>

<span data-ttu-id="9de2b-105">*Ausdruck* . NextRecordset</span><span class="sxs-lookup"><span data-stu-id="9de2b-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="9de2b-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9de2b-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9de2b-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9de2b-107">Return value</span></span>

<span data-ttu-id="9de2b-108">Boolesch</span><span class="sxs-lookup"><span data-stu-id="9de2b-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="9de2b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9de2b-109">Remarks</span></span>

<span data-ttu-id="9de2b-110">In einem ODBCDirect-Arbeitsbereich können Sie ein **[Recordset](recordset-object-dao.md)** -Objekt mit mehr als einer Auswahlabfrage im Source- \*\*\*\* Argument von OpenRecordset oder der **[SQL](querydef-sql-property-dao.md)** -Eigenschaft eines **[QueryDef](querydef-object-dao.md)** -Objekts der SELECT-Abfrage wie im folgenden Beispiel öffnen.</span><span class="sxs-lookup"><span data-stu-id="9de2b-110">In an ODBCDirect workspace, you can open a **[Recordset](recordset-object-dao.md)** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="9de2b-p101">Das zurückgegebene **Recordset** wird mit den Ergebnissen der ersten Abfrage geöffnet. Mit der **NextRecordset**-Methode können Sie die resultierenden Datensatzgruppen aus nachfolgenden Abfragen abrufen.</span><span class="sxs-lookup"><span data-stu-id="9de2b-p101">The returned **Recordset** will open with the results of the first query. To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="9de2b-p102">Sind mehrere Datensätze verfügbar (der **OpenRecordset**-Aufruf oder die **SQL**-Eigenschaft enthielt also eine weitere Auswahlabfrage), werden die von der nächsten Abfrage zurückgegebenen Datensätze in das **Recordset** geladen, und **NextRecordset** gibt **True** zurück, was die Verfügbarkeit der Datensätze angibt. Sind keine Datensätze mehr verfügbar (d. h. die Ergebnisse der letzten Auswahlabfrage wurden in das **Recordset**-Objekt geladen), dann gibt **NextRecordset** den Wert **False** zurück, und **Recordset** ist leer.</span><span class="sxs-lookup"><span data-stu-id="9de2b-p102">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available. When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="9de2b-115">Sie können die **[Cancel](connection-cancel-method-dao.md)** -Methode auch verwenden, um den Inhalt eines **Recordset-Objekts**zu leeren.</span><span class="sxs-lookup"><span data-stu-id="9de2b-115">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**.</span></span> <span data-ttu-id="9de2b-116">Mit **Cancel** werden auch die noch nicht geladenen Datensätze geleert.</span><span class="sxs-lookup"><span data-stu-id="9de2b-116">However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="9de2b-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9de2b-117">Example</span></span>

<span data-ttu-id="9de2b-p104">Dieses Beispiel zeigt mit der **NextRecordset**-Methode die Daten aus einer SELECT-Verbundabfrage an. Die **DefaultCursorDriver**-Eigenschaft muss beim Ausführen solcher Abfragen auf **dbUseODBCCursor** festgelegt sein. Die **NextRecordset**-Methode gibt auch dann **True** zurück, wenn einige oder alle der SELECT-Anweisungen keine Datensätze zurückgeben; **False** wird erst zurückgegeben, nachdem jede einzelne SQL-Klausel überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="9de2b-p104">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="9de2b-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span><span class="sxs-lookup"><span data-stu-id="9de2b-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

