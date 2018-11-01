---
title: Recordsets Collection (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a32c52f60ed8c7bd68f32ed9986638bffcdec84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869001"
---
# <a name="recordsets-collection-dao"></a>Recordsets Collection (DAO)

**Betrifft**: Access 2013, Office 2013

Eine **Recordsets**-Auflistung enthält alle geöffneten **Recordset**-Objekte in einem **Connection**- oder **Database**-Objekt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie DAO-Objekte verwenden, bearbeiten Sie Daten nahezu vollständig unter Verwendung von **Recordset**-Objekten.

Der **Recordsets**-Auflistung wird automatisch ein neues **Recordset**-Objekt hinzugefügt, wenn Sie das **Recordset**-Objekt öffnen, und automatisch daraus entfernt, wenn Sie es schließen.

Sie können so viele **Recordset**-Objektvariablen erstellen wie nötig. Unterschiedliche **Recordset**-Objekte können ohne Konflikte auf dieselben Tabellen, Abfragen oder Felder zugreifen.

Wenn Sie auf ein **Recordset**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

- **Recordsets**(0)

- **Recordset-Objekte** ("Name")

- **Recordsets**\!\[Namen\]

> [!NOTE]
> [!HINWEIS] Sie können ein **Recordset**-Objekt derselben Datenquelle oder Datenbank mehrmals öffnen und dabei doppelte Namen in der **Recordsets**-Auflistung erstellen. Sie sollten Objektvariablen **Recordset**-Objekte zuweisen und mit Variablennamen auf sie verweisen.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht Recordset-Objekte und die Recordsets-Auflistung, indem es vier verschiedene Typen von Recordsets-Objekten öffnet und die Recordsets-Auflistung des aktuellen Database-Objekts und dann die Properties-Auflistung der einzelnen Recordset-Objekte aufführt.

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
