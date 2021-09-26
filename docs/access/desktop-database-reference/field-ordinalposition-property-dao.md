---
title: Field.OrdinalPosition-Eigenschaft (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1a709b8c9f138be50b71911854a05af69e6bbf50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622347"
---
# <a name="fieldordinalposition-property-dao"></a>Field.OrdinalPosition-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt die relative Position eines **[Field](field-object-dao.md)** -Objekts innerhalb einer **[Fields](fields-collection-dao.md)** -Auflistung fest oder gibt die relative Position zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . OrdinalPosition

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei einem Objekt, das noch nicht der **Fields**-Auflistung angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.

The default is 0.

Die Verfügbarkeit der **OrdinalPosition**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit der Fields-Auflistung</p></th>
<th><p>OrdinalPosition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong>-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong>-Objekt</p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong>-Objekt</p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong>-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong>-Objekt</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>


In der Regel hängt die Position eines Objekts, das Sie einer Auflistung anfügen, von der Reihenfolge der Anfügung ab. Das erste angefügte Objekt befindet sich an der ersten Position (0), das zweite an der zweiten Position (1) usw. The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.

Mit der **OrdinalPosition**-Eigenschaft können Sie eine Ordnungsposition für neue **Field**-Objekte festlegen, die sich von der Reihenfolge unterscheidet, in der Sie diese Objekte an eine Auflistung anhängen. Dadurch können Sie eine Feldreihenfolge für Tabellen, Abfragen und Recordsets angeben, die Sie in einer Anwendung verwenden. Beispielsweise wird die Reihenfolge, in der Felder in einer SELECT-Abfrage zurückgegeben werden, \* durch die aktuellen Werte der **OrdinalPosition-Eigenschaft** bestimmt.

Sie können die Reihenfolge, in der Felder in Datensatzgruppen zurückgegeben werden, dauerhaft festlegen, indem Sie die **OrdinalPosition**-Eigenschaft auf eine positive Ganzzahl setzen.

Two or more **Field** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.

Sie können einen Wert angeben, der größer als die Anzahl der Felder minus 1 ist. Das Feld wird in einer Reihenfolge relativ zum größten Wert zurückgegeben. Wenn Sie z. B. die **OrdinalPosition**-Eigenschaft eines Felds auf 20 festlegen (und nur 5 Felder vorhanden sind) und Sie die **OrdinalPosition**-Eigenschaft für zwei anderen Felder auf 10 und 30 gesetzt haben, wird das Feld mit dem Wert 20 zwischen den Feldern mit den Werten 10 und 30 zurückgegeben.

> [!NOTE]
> Even if the **Fields** collection of a [TableDef](tabledef-object-dao.md) has not been refreshed, the field order in a [Recordset](recordset-object-dao.md) opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object. A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.

## <a name="example"></a>Beispiel

This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
