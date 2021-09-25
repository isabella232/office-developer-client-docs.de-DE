---
title: Parameter-Objekt (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 78a1b7a497e31e031d15fbccb4181279ddfab67c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568761"
---
# <a name="parameter-object-dao"></a>Parameter-Objekt (DAO)


**Gilt für**: Access 2013, Office 2013

Ein **Parameter**-Objekt stellt einen Wert für eine Abfrage dar. Der Parameter wird einem **QueryDef**-Objekt zugeordnet, das aus einer Parameterabfrage erstellt wird.

## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe von **Parameter**-Objekten können Sie die Argumente eines häufig ausgeführten **QueryDef**-Objekts ändern, ohne dass Sie die Abfrage erneut kompilieren müssen.

Mit den Eigenschaften eines **Parameter**-Objekts können Sie eine Parameterabfrage festlegen, die vor dem Ausführen der Abfrage geändert werden kann. Sie können die folgenden Aktionen ausführen:

  - Geben Sie mit der **Name**-Eigenschaft den Namen eines Parameters zurück.

  - Verwenden Sie die **Value**-Eigenschaft, um die in der Abfrage verwendeten Parameterwerte festzulegen oder zurückzugeben.

  - Geben Sie mit der **Type**-Eigenschaft den Datentyp des **Parameter**-Objekts zurück.

  - Verwenden Sie die **Direction**-Eigenschaft, um festzulegen oder zurückzugeben, ob es sich bei dem Parameter um einen Eingabeparameter und/oder einen Ausgabeparameter handelt.

## <a name="example"></a>Beispiel

This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.

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
