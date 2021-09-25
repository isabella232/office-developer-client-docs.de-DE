---
title: Recordsets-Auflistung (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f11c3f5711d7f566dacad8071574ebe230d91b16
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562307"
---
# <a name="recordsets-collection-dao"></a>Recordsets-Auflistung (DAO)

**Gilt für**: Access 2013, Office 2013

Eine **Recordsets**-Auflistung enthält alle geöffneten **Recordset**-Objekte in einem **Connection**- oder **Database**-Objekt.

## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie DAO-Objekte verwenden, bearbeiten Sie Daten nahezu vollständig unter Verwendung von **Recordset**-Objekten.

Der **Recordsets**-Auflistung wird automatisch ein neues **Recordset**-Objekt hinzugefügt, wenn Sie das **Recordset**-Objekt öffnen, und automatisch daraus entfernt, wenn Sie es schließen.

Sie können so viele **Recordset**-Objektvariablen erstellen wie nötig. Unterschiedliche **Recordset**-Objekte können ohne Konflikte auf dieselben Tabellen, Abfragen oder Felder zugreifen.

Um auf ein **Recordset**-Objekt in einer Auflistung durch die Ordnungszahl oder die Einstellung der **Name**-Eigenschaft zu verweisen, verwenden Sie eine der folgenden Syntaxformen:

- **Recordsets**(0)

- **Recordsets**("Name")

- **Recordsets**\!\[name\]

> [!NOTE]
> Sie können ein **Recordset**-Objekt aus der gleichen Datenquelle oder Datenbank mehrmals öffnen und doppelte Namen in der **Recordsets**-Auflistung erstellen. Sie sollten **Recordset**-Objekten Objektvariablen zuweisen und mit dem Variablennamen auf sie verweisen.

## <a name="example"></a>Beispiel

This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
