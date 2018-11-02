---
title: Field2.DataUpdatable-Eigenschaft (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aafa6e49168d6ab04ad357f867554ecaff581afd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930924"
---
# <a name="field2dataupdatable-property-dao"></a>Field2.DataUpdatable-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013


Gibt einen Wert zurück, der angibt, ob die Daten eines durch ein **Field2**-Objekt dargestellten Felds aktualisiert werden können.

## <a name="syntax"></a>Syntax

*Ausdruck* . DataUpdatable

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ermitteln Sie mit dieser Eigenschaft, ob Sie die Einstellung einer **[Value](field-value-property-dao.md)** -Eigenschaft eines **Field2**-Objekts ändern können. Diese Eigenschaft ist bei einem **Field2**-Objekt immer **False**, dessen **[Attributes](field-attributes-property-dao.md)** -Eigenschaft auf **dbAutoIncrField** festgelegt ist.

Sie können die **DataUpdatable**-Eigenschaft bei **Field2**-Objekten verwenden, die der **[Fields](fields-collection-dao.md)** -Auflistung der Objekte **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** oder **[Relation](relation-object-dao.md)** hinzugefügt werden, nicht jedoch der **Fields**-Auflistung der Objekte **[Index](index-object-dao.md)** oder **[TableDef](tabledef-object-dao.md)**.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die DataUpdatable-Eigenschaft veranschaulicht, indem ihr Wert geändert und ein neues Recordsets-Objekt erstellt wird. Zum Ausführen dieser Prozedur ist die SortOutput-Funktion erforderlich.

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```

