---
title: Parameter-Objekt (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5df04b1ee06a2224db9e21f67e9c68a3ee5740bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288084"
---
# <a name="parameter-object-dao"></a><span data-ttu-id="69a3d-102">Parameter-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="69a3d-102">Parameter object (DAO)</span></span>


<span data-ttu-id="69a3d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69a3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69a3d-104">Ein **Parameter**-Objekt stellt einen Wert für eine Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="69a3d-104">A **Parameter** object represents a value supplied to a query.</span></span> <span data-ttu-id="69a3d-105">Der Parameter wird einem **QueryDef**-Objekt zugeordnet, das aus einer Parameterabfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="69a3d-105">The parameter is associated with a **QueryDef** object created from a parameter query.</span></span>

## <a name="remarks"></a><span data-ttu-id="69a3d-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69a3d-106">Remarks</span></span>

<span data-ttu-id="69a3d-107">Mithilfe von **Parameter**-Objekten können Sie die Argumente eines häufig ausgeführten **QueryDef**-Objekts ändern, ohne dass Sie die Abfrage erneut kompilieren müssen.</span><span class="sxs-lookup"><span data-stu-id="69a3d-107">**Parameter** objects allow you to change the arguments in a frequently run **QueryDef** object without having to recompile the query.</span></span>

<span data-ttu-id="69a3d-p102">Mit den Eigenschaften eines **Parameter**-Objekts können Sie eine Parameterabfrage festlegen, die vor dem Ausführen der Abfrage geändert werden kann. Sie können die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="69a3d-p102">Using the properties of a **Parameter** object, you can set a query parameter that can be changed before the query is run. You can:</span></span>

  - <span data-ttu-id="69a3d-110">Geben Sie mit der **Name**-Eigenschaft den Namen eines Parameters zurück.</span><span class="sxs-lookup"><span data-stu-id="69a3d-110">Use the **Name** property to return the name of a parameter.</span></span>

  - <span data-ttu-id="69a3d-111">Verwenden Sie die **Value**-Eigenschaft, um die in der Abfrage verwendeten Parameterwerte festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="69a3d-111">Use the **Value** property to set or return the parameter values to be used in the query.</span></span>

  - <span data-ttu-id="69a3d-112">Geben Sie mit der **Type**-Eigenschaft den Datentyp des **Parameter**-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="69a3d-112">Use the **Type** property to return the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="69a3d-113">Verwenden Sie die **Direction**-Eigenschaft, um festzulegen oder zurückzugeben, ob es sich bei dem Parameter um einen Eingabeparameter und/oder einen Ausgabeparameter handelt.</span><span class="sxs-lookup"><span data-stu-id="69a3d-113">Use the **Direction** property to set or return whether the parameter is an input parameter, an output parameter, or both.</span></span>

## <a name="example"></a><span data-ttu-id="69a3d-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="69a3d-114">Example</span></span>

<span data-ttu-id="69a3d-p103">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="69a3d-p103">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.</span></span>

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
