---
title: QueryDef. RecordsAffected-Eigenschaft (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 29a864b5-305c-d33f-b2ca-fc9a08baaa5c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192040(v=office.15)
ms:contentKeyID: 48543886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053082
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ad3759be1bcb60052111a4e7d27419aff08d510a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300966"
---
# <a name="querydefrecordsaffected-property-dao"></a><span data-ttu-id="d0522-102">QueryDef. RecordsAffected-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="d0522-102">QueryDef.RecordsAffected property (DAO)</span></span>


<span data-ttu-id="d0522-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0522-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0522-104">Gibt die Anzahl der Datensätze zurück, die von der zuletzt aufgerufenen **[Execute](querydef-execute-method-dao.md)** -Methode betroffen waren.</span><span class="sxs-lookup"><span data-stu-id="d0522-104">Returns the number of records affected by the most recently invoked **[Execute](querydef-execute-method-dao.md)** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0522-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0522-105">Syntax</span></span>

<span data-ttu-id="d0522-106">*Ausdruck* . RecordsAffected</span><span class="sxs-lookup"><span data-stu-id="d0522-106">*expression* .RecordsAffected</span></span>

<span data-ttu-id="d0522-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0522-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0522-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0522-108">Remarks</span></span>

<span data-ttu-id="d0522-109">Wenn Sie die **Execute**-Methode verwenden, um eine Aktionsabfrage für ein **QueryDef**-Objekt auszuführen, enthält die **RecordsAffected**-Eigenschaft die Anzahl der gelöschten, aktualisierten oder eingefügten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="d0522-109">When you use the **Execute** method to run an action query from a **QueryDef** object, the **RecordsAffected** property will contain the number of records deleted, updated, or inserted.</span></span>

## <a name="example"></a><span data-ttu-id="d0522-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0522-110">Example</span></span>

<span data-ttu-id="d0522-p101">This example uses the **RecordsAffected** property with action queries executed from a **[Database](database-object-dao.md)** object and from a **QueryDef** object. The RecordsAffectedOutput function is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="d0522-p101">This example uses the **RecordsAffected** property with action queries executed from a **[Database](database-object-dao.md)** object and from a **QueryDef** object. The RecordsAffectedOutput function is required for this procedure to run.</span></span>

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
