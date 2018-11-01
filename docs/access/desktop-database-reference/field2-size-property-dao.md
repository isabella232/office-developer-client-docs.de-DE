---
title: Field2.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3783ed413d57eb3bb9a41fa1880485aa5d3ad281
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882448"
---
# <a name="field2size-property-dao"></a>Field2.Size Property (DAO)


**Betrifft**: Access 2013, Office 2013


Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die maximale Größe eines **Field2**-Objekts in Bytes angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Größe

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.

Bei Feldern (außer Memofeldern), die Zeichendaten enthalten, gibt die **Size**-Eigenschaft die maximale Anzahl von Zeichen an, die ein Feld enthalten kann. Bei numerischen Feldern gibt die **Size**-Eigenschaft an, wie viel Speicherplatz in Bytes erforderlich ist.

Die Verwendung der **Size**-Eigenschaft hängt vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit zu Objekt</p></th>
<th><p>Verwendung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef-Objekt</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Beziehung</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
</tbody>
</table>


Wenn Sie ein Field2-Objekt mit einem anderen Datentyp als Text erstellen, bestimmt die Einstellung der Type-Eigenschaft automatisch die Einstellung der Size-Eigenschaft, und Sie müssen die Eigenschaft nicht festlegen. Bei einem  Field2-Objekt mit dem Datentyp Text können Sie die Size-Eigenschaft jedoch auf eine ganze Zahl bis zu einer maximalen Textgröße festlegen (255 bei Microsoft Access-Datenbanken). Wenn Sie die Größe nicht festlegen, besitzt das Feld die in der Datenbank zulässige Größe.

Bei Field2-Objekten vom Datentyp Long Binary und Memo ist die Size-Eigenschaft immer auf 0 festgelegt. Bestimmen Sie mit der FieldSize-Eigenschaft des Field2-Objekts den Umfang der Daten in einem bestimmten Datensatz. Die maximale Größe eines Felds vom Typ Long Binary oder Memo wird nur durch die Systemressourcen oder die maximal in der Datenbank zulässige Größe beschränkt.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht die Size-Eigenschaft, indem es die Namen und Größen des Field2-Objekts in der Employees-Tabelle (Personal) aufzählt.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
