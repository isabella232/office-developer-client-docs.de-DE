---
title: Database.RecordsAffected-Eigenschaft (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 1c591231-21dd-f0b1-4ba6-87784c5890d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845732(v=office.15)
ms:contentKeyID: 48543567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f5f7123aabb813e3e447756005cce1bd2d7a4c69
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569167"
---
# <a name="databaserecordsaffected-property-dao"></a>Database.RecordsAffected-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt die Anzahl der Datensätze zurück, die von der zuletzt aufgerufenen **[Execute](connection-execute-method-dao.md)** -Methode betroffen waren.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordsAffected

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="example"></a>Beispiel

This example uses the **RecordsAffected** property with action queries executed from a **Database** object and from a **QueryDef** object. The RecordsAffectedOutput function is required for this procedure to run.

```vb
    Sub RecordsAffectedX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim strSQLChange As String 
     Dim strSQLRestore As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "Number of records in Employees table: " & _ 
     .TableDefs!Employees.RecordCount 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and execute an action query. 
     strSQLChange = "UPDATE Employees " & _ 
     "SET Country = 'United States' " & _ 
     "WHERE Country = 'USA'" 
     .Execute strSQLChange 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from Database: " & .RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and run another action query. 
     strSQLRestore = "UPDATE Employees " & _ 
     "SET Country = 'USA' " & _ 
     "WHERE Country = 'United States'" 
     Set qdfTemp = .CreateQueryDef("", strSQLRestore) 
     qdfTemp.Execute 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from QueryDef: " & qdfTemp.RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     .Close 
     
     End With 
     
    End Sub 
     
    Function RecordsAffectedOutput(dbsNorthwind As Database) 
     
     Dim rstEmployees As Recordset 
     
     ' Open a Recordset object from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Enumerate Recordset. 
     .MoveFirst 
     Do While Not .EOF 
     Debug.Print " " & !LastName & ", " & !Country 
     .MoveNext 
     Loop 
     .Close 
     End With 
     
    End Function
```
