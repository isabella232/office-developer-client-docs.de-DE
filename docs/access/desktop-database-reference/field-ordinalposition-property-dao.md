---
title: Field.OrdinalPosition Property (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1218dd1cc6b1b309c5513a9b0f67a66d06d9c499
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863637"
---
# <a name="fieldordinalposition-property-dao"></a>Field.OrdinalPosition Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt die relative Position eines **[Field](field-object-dao.md)** -Objekts innerhalb einer **[Fields](fields-collection-dao.md)** -Auflistung fest oder gibt die relative Position zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . OrdinalPosition

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

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

Die **OrdinalPosition** -Eigenschaft können Sie eine Position für den neuen **Field** -Objekten angeben, die von der Reihenfolge abweicht, in dem Sie diese Objekte an eine Auflistung anzufügen. Dadurch können Sie eine Feldreihenfolge für Tabellen, Abfragen und Recordsets angeben, die Sie in einer Anwendung verwenden. Beispielsweise die Reihenfolge, in der Felder in einer SELECT-Anweisung zurückgegeben werden \* Abfrage wird durch die aktuellen Werte der **OrdinalPosition** -Eigenschaft bestimmt.

Sie können die Reihenfolge, in der Felder in Datensatzgruppen zurückgegeben werden, dauerhaft festlegen, indem Sie die **OrdinalPosition**-Eigenschaft auf eine positive Ganzzahl setzen.

Zwei oder mehr Field-Objekte in derselben Auflistung können denselben OrdinalPosition-Eigenschaftswert haben. In diesem Fall werden sie alphabetisch angeordnet. Wenn Sie z. B. ein Feld mit dem Namen Alter auf den Wert 4 festlegen und für ein zweites Feld mit dem Namen Gewicht den Wert 4 angeben, wird Gewicht nach Alter zurückgegeben.

Sie können einen Wert angeben, der größer als die Anzahl der Felder minus 1 ist. Das Feld wird in einer Reihenfolge relativ zum größten Wert zurückgegeben. Wenn Sie z. B. die **OrdinalPosition**-Eigenschaft eines Felds auf 20 festlegen (und nur 5 Felder vorhanden sind) und Sie die **OrdinalPosition**-Eigenschaft für zwei anderen Felder auf 10 und 30 gesetzt haben, wird das Feld mit dem Wert 20 zwischen den Feldern mit den Werten 10 und 30 zurückgegeben.

> [!NOTE]
> Selbst wenn die Fields-Auflistung eines TableDef-Objekts nicht aktualisiert wurde, gibt die Reihenfolge der Felder in einem Recordset-Objekt, das vom TableDef-Objekt aus geöffnet wird, die OrdinalPosition-Daten des TableDef-Objekts wieder. Ein Recordset-Objekt vom Typ Tabelle besitzt dieselben OrdinalPosition-Daten wie die zugrunde liegende Tabelle, jeder andere Recordset-Objekttyp weist jedoch neue OrdinalPosition-Daten auf (beginnend bei 0), die der durch die OrdinalPosition-Daten des TableDef-Objekts bestimmten Reihenfolge entsprechen.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die OrdinalPosition-Eigenschaftswerte im TableDef-Objekt von Employees geändert, um die Reihenfolge des Field-Objekts in einem sich ergebenden Recordset-Objekt zu steuern. OrdinalPosition wird für alle Fields-Objekte auf den Wert 1 festgelegt, sodass die Reihenfolge der Fields-Objekte von den sich ergebenden Recordset-Objekten alphabetisch sortiert wird. Beachten Sie, dass die OrdinalPosition-Werte im Recordset-Objekt nicht mit den Werten im TableDef-Objekt übereinstimmen, sondern einfach das Ergebnis des TableDef-Objekts widerspiegeln.

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
