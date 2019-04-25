---
title: Connection.Database-Eigenschaft (DAO)
TOCTitle: Database Property
ms:assetid: cf871353-0ea4-f995-6e0e-812af443daf9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834675(v=office.15)
ms:contentKeyID: 48547809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053581
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 7033c612642aa3ae6ce6c6175560438c893cde6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295919"
---
# <a name="connectiondatabase-property-dao"></a><span data-ttu-id="4a7e7-102">Connection.Database-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a7e7-102">Connection.Database Property (DAO)</span></span>


<span data-ttu-id="4a7e7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a7e7-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="syntax"></a><span data-ttu-id="4a7e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a7e7-104">Syntax</span></span>

<span data-ttu-id="4a7e7-105">*Ausdruck* .Database</span><span class="sxs-lookup"><span data-stu-id="4a7e7-105">expression  . Database</span></span>

<span data-ttu-id="4a7e7-106">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a7e7-106">*expression*  A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a7e7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a7e7-107">Remarks</span></span>

<span data-ttu-id="4a7e7-p101">Verwenden Sie bei einem **[Connection](connection-object-dao.md)** -Objekt zum Abrufen eines **Database** -Objekts zur entsprechenden **Verbindung** die **Database** -Eigenschaft. In DAO sind das **Connection** -Objekt und das entsprechende **Database** -Objekt schlicht und ergreifend zwei verschiedene Objektvariablenverweise auf dasselbe Objekt. Die **Database** -Eigenschaft eines **Connection** -Objekts und die **[Connection](database-connection-property-dao.md)** -Eigenschaft eines **Database** -Objekts erleichtern die Umstellung von Verbindungen mit einer ODBC-Datenquelle über das Microsoft Access-Datenbankmodul auf ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="4a7e7-p101">On a **[Connection](connection-object-dao.md)** object, use the **Database** property to obtain a reference to a **Database** object that corresponds to the **Connection**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **Database** property of a **Connection** object and the **[Connection](database-connection-property-dao.md)** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

## <a name="example"></a><span data-ttu-id="4a7e7-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a7e7-111">Example</span></span>

<span data-ttu-id="4a7e7-112">In diesem Beispiel wird gezeigt, wie die **Database**-Eigenschaft dazu verwendet werden kann, Code so umzuwandeln, dass anstelle von ODBC-Daten über das Microsoft Access-Datenbankmodul anschließend ODBCDirect-Verbindungsobjekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a7e7-112">This example uses the **Database** property to show how code that used to access ODBC data through the Microsoft Access database engine can be converted to use ODBCDirect Connection objects.</span></span>

<span data-ttu-id="4a7e7-113">Die OldDatabaseCode-Prozedur verwendet für den Zugriff auf eine ODBC-Datenbank eine Datenquelle, die mit dem Microsoft Access-Datenbankmodul verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4a7e7-113">The OldDatabaseCode procedure uses a Microsoft Access database engine-connected data source to access an ODBC database.</span></span>

```vb
    Sub OldDatabaseCode() 
     
     Dim wrkMain As Workspace 
     Dim dbsPubs As Database 
     Dim prpLoop As Property 
     
     ' Create a Workspace object. 
     Set wrkMain = CreateWorkspace("", "admin", "", dbUseJet) 
     
     ' Open a Database object based on information in 
     ' the connect string. 
     
     'Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set dbsPubs = wrkMain.OpenDatabase("Publishers", _ 
     dbDriverNoPrompt, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Enumerate the Properties collection of the Database 
     ' object. 
     With dbsPubs 
     Debug.Print "Database properties for " & _ 
     .Name & ":" 
     
     On Error Resume Next 
     For Each prpLoop In .Properties 
     If prpLoop.Name = "Connection" Then 
     ' Property actually returns a Connection object. 
     Debug.Print " Connection[.Name] = " & _ 
     .Connection.Name 
     Else 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop 
     End If 
     Next prpLoop 
     On Error GoTo 0 
     
     End With 
     
     dbsPubs.Close 
     wrkMain.Close 
     
    End Sub 
```

<span data-ttu-id="4a7e7-p102">Das Beispiel für NewDatabaseCode öffnet ein **Connection** -Objekt in einem ODBCDirect-Arbeitsbereich. Dann wird die **Database** -Eigenschaft des **Connection** -Objekts einer Objektvariable zugewiesen, die denselben Namen erhält wie die Datenquelle im der alten Prozedur. Der folgende Code muss nicht modifiziert werden, solange keine spezifischen Funktionen des Microsoft Access-Arbeitsbereiches verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a7e7-p102">The NewDatabaseCode example opens a **Connection** object in an ODBCDirect workspace. It then assigns the **Database** property of the **Connection** object to an object variable with the same name as the data source in the old procedure. None of the subsequent code has to be changed as long as it doesn't use any features specific to Microsoft Access workspaces.</span></span>

```vb 
Sub NewDatabaseCode() 
 
 Dim wrkMain As Workspace 
 Dim conPubs As Connection 
 Dim dbsPubs As Database 
 Dim prpLoop As Property 
 
 ' Create ODBCDirect Workspace object instead of Microsoft 
 ' Access Workspace object. 
 Set wrkMain = CreateWorkspace("", "admin", "", dbUseODBC) 
 
 ' Open Connection object based on information in 
 ' the connect string. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 ' Assign the Database property to the same object 
 ' variable as in the old code. 
 Set dbsPubs = conPubs.Database 
 
 ' Enumerate the Properties collection of the Database 
 ' object. From this point on, the code is the same as the 
 ' old example. 
 With dbsPubs 
 Debug.Print "Database properties for " & _ 
 .Name & ":" 
 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 .Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 End With 
 
 dbsPubs.Close 
 wrkMain.Close 
 
End Sub 
 
```

