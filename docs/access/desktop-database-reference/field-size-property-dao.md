---
title: Field.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c55c7cedb3ad249e30180af872aead372554e9a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473848"
---
# <a name="fieldsize-property-dao"></a>Field.Size Property (DAO)


**Betrifft**: Access 2013 | Office 2013


Legt einen Wert fest, der die maximale Größe eines **[Field](field-object-dao.md)** -Objekts in Byte angibt, oder gibt den betreffenden Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . Größe

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.

Bei Feldern (außer Memofeldern), die Zeichendaten enthalten, gibt die **Size**-Eigenschaft die maximale Anzahl von Zeichen an, die ein Feld enthalten kann. Bei numerischen Feldern gibt die **Size**-Eigenschaft an, wie viel Speicherplatz in Bytes erforderlich ist.

Die Verwendung der **Size**-Eigenschaft hängt von dem Objekt ab, das die **Fields**-Auflistung enthält, an die das **Field**-Objekt angehängt ist, wie in der folgenden Tabelle dargestellt.

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


Wenn Sie ein Field-Objekt mit einem anderen Datentyp als Text erstellen, legt der Wert der Type-Eigenschaft automatisch die Einstellung des Size-Eigenschaft fest, sodass Sie diese Eigenschaft nicht festlegen müssen. Bei einem Field-Objekt vom Text-Datentyp können Sie jedoch Size auf eine Ganzzahl bis zur maximalen Textgröße festlegen (255 für Microsoft Access-Datenbanken). Wenn Sie die Größe nicht festlegen, hat das Feld die maximale von der Datenbank zugelassene Größe.

Bei Field-Objekten der Datentypen Long Binary und Memo hat Size immer den Wert 0. Verwenden Sie die FieldSize-Eigenschaft des Field-Objekts, um die Größe der Daten in einem bestimmten Datensatz festzustellen. Die maximale Größe eines Felds vom Datentyp Long Binary oder Memo ist nur durch die Systemressourcen bzw. die maximale von der Datenbank erlaubte Größe begrenzt.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die Size-Eigenschaft veranschaulicht, indem die Namen und Größen der Field-Objekte in der Tabelle Employees durchlaufen werden.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
