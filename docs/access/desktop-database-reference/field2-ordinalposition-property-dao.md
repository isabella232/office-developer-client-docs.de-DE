---
title: Field2.Ordinalposition-Eigenschaft (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26d37bfda90f2ab4e2627b936d3cf37b5be811d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726330"
---
# <a name="field2ordinalposition-property-dao"></a>Field2.Ordinalposition-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013


Mit dieser Eigenschaft wird die relative Position eines **Field2**-Objekts in einer **[Fields](fields-collection-dao.md)** -Auflistung festgelegt oder zurückgegeben.

## <a name="syntax"></a>Syntax

*Ausdruck* . OrdinalPosition

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei einem Objekt, das noch nicht der **Fields**-Auflistung angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.

Der Standardwert ist 0.

Die Verfügbarkeit der **OrdinalPosition**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit der Fields-Auflistung</p></th>
<th><p>
Verfügbarkeit von OrdinalPosition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> -Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> -Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> -Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> -Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> -Objekt</p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
</tbody>
</table>


In der Regel hängt die Position eines Objekts, das Sie einer Auflistung anfügen, von der Reihenfolge der Anfügung ab. Das erste angefügte Objekt befindet sich an der ersten Position (0), das zweite an der zweiten Position (1) usw. Das letzte hinzugefügte Objekt befindet sich an Position Count – 1, wobei Count der Anzahl von Objekten in der Auflistung entspricht, wie durch die Einstellung der **[Count](containers-count-property-dao.md)**-Eigenschaft angegeben.

Sie können mithilfe der **OrdinalPosition**-Eigenschaft eine Position für neue **Field2**-Objekte angeben, die von der Reihenfolge abweicht, in der Sie diese Objekte der Auflistung anfügen. Dadurch können Sie eine Feldreihenfolge für Tabellen, Abfragen und Recordsets angeben, die Sie in einer Anwendung verwenden. Beispielsweise die Reihenfolge, in der Felder in einer SELECT-Anweisung zurückgegeben werden \* Abfrage wird durch die aktuellen Werte der **OrdinalPosition** -Eigenschaft bestimmt.

Sie können die Reihenfolge, in der Felder in Recordsets zurückgegeben werden, dauerhaft zurücksetzen, indem Sie die **OrdinalPosition**-Eigenschaft auf eine positive ganze Zahl festlegen.

Zwei oder mehr Field2-Objekte in derselben Auflistung können denselben OrdinalPosition-Eigenschaftswert besitzen. In diesem Fall werden sie alphabetisch angeordnet. Wenn Sie z. B. ein Feld namens Alter auf 4 und ein zweites Feld namens Gewicht auf 4 festlegen, wird das Gewicht nach dem Alter zurückgegeben.

Sie können einen Wert angeben, der größer als die Anzahl der Felder minus 1 ist. Das Feld wird in einer Reihenfolge relativ zum größten Wert zurückgegeben. Wenn Sie z. B. die **OrdinalPosition**-Eigenschaft eines Felds auf 20 festlegen (und nur 5 Felder vorhanden sind) und Sie die **OrdinalPosition**-Eigenschaft für zwei anderen Felder auf 10 und 30 gesetzt haben, wird das Feld mit dem Wert 20 zwischen den Feldern mit den Werten 10 und 30 zurückgegeben.


> [!NOTE]
> Auch wenn die **Fields** -Auflistung ein **[TableDef](tabledef-object-dao.md)** -Objekt nicht aktualisiert wurde, wird die Reihenfolge der Felder in einem **[Recordset-Objekt](recordset-object-dao.md)** aus der **TableDef** geöffnet die **OrdinalPosition** -Daten des **TableDef** -Objekts widerspiegeln. Ein **Recordset-Objekt** vom Typ Tabelle wird die gleichen **OrdinalPosition** Daten wie der zugrunde liegenden Tabelle, aber eine andere Art von **Recordset-Objekt** werden neue **OrdinalPosition** -Daten (beginnend mit 0), die die Reihenfolge der **Folgen haben OrdinalPosition** Daten des **TableDef**.



## <a name="example"></a>Beispiel

Dieses Beispiel ändert die Werte der OrdinalPosition-Eigenschaft des TableDef-Objekts in der Employees-Tabelle (Personal), um die Field2-Reihenfolge in einem resultierenden Recordset-Objekt zu steuern. Indem die OrdinalPosition-Eigenschaft aller Felder der Fields-Auflistung auf 1 festgelegt wird, ordnen resultierende Recordset-Objekte die Fields-Auflistung alphabetisch an. Beachten Sie, dass die OrdinalPosition-Werte im Recordset-Objekt nicht mit den Werten im TableDef-Objekt übereinstimmen, sondern lediglich das Endergebnis der TableDef-Änderungen wiedergeben.

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
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
