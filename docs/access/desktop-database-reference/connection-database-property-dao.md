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
ms.localizationpriority: high
ms.openlocfilehash: eaca7976e417d61ef8d70f0d60aa2438f89072ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586040"
---
# <a name="connectiondatabase-property-dao"></a>Connection.Database-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013



## <a name="syntax"></a>Syntax

*Ausdruck* .Database

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie bei einem **[Connection](connection-object-dao.md)** -Objekt zum Abrufen eines **Database** -Objekts zur entsprechenden **Verbindung** die **Database** -Eigenschaft. In DAO sind das **Connection** -Objekt und das entsprechende **Database** -Objekt schlicht und ergreifend zwei verschiedene Objektvariablenverweise auf dasselbe Objekt. Die **Database** -Eigenschaft eines **Connection** -Objekts und die **[Connection](database-connection-property-dao.md)** -Eigenschaft eines **Database** -Objekts erleichtern die Umstellung von Verbindungen mit einer ODBC-Datenquelle über das Microsoft Access-Datenbankmodul auf ODBCDirect.

## <a name="example"></a>Beispiel

In diesem Beispiel wird gezeigt, wie die **Database**-Eigenschaft dazu verwendet werden kann, Code so umzuwandeln, dass anstelle von ODBC-Daten über das Microsoft Access-Datenbankmodul anschließend ODBCDirect-Verbindungsobjekte verwendet werden.

Die OldDatabaseCode-Prozedur verwendet für den Zugriff auf eine ODBC-Datenbank eine Datenquelle, die mit dem Microsoft Access-Datenbankmodul verbunden ist.

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

Das Beispiel für NewDatabaseCode öffnet ein **Connection** -Objekt in einem ODBCDirect-Arbeitsbereich. Dann wird die **Database** -Eigenschaft des **Connection** -Objekts einer Objektvariable zugewiesen, die denselben Namen erhält wie die Datenquelle im der alten Prozedur. Der folgende Code muss nicht modifiziert werden, solange keine spezifischen Funktionen des Microsoft Access-Arbeitsbereiches verwendet werden.

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

