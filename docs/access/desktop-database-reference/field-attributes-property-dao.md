---
title: Field.Attributes-Eigenschaft (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 010c7a2aea777a93d1ced2d33d8743320dd05ada
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293154"
---
# <a name="fieldattributes-property-dao"></a>Field.Attributes-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der ein oder mehrere Merkmale eines **[Field](field-object-dao.md)** -Objekts angibt. **Long** mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*expression* .Attributes

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Wert gibt die Merkmale des Felds an, das vom **Field**-Objekt dargestellt wird und eine Kombination der folgenden Konstanten sein kann.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>Der Feldwert für neue Datensätze wird automatisch auf einen eindeutigen Long Integer-Wert erhöht, der nicht geändert werden kann (wird in einem Microsoft Access-Arbeitsbereich nur bei Microsoft Access-Datenbanktabellen unterstützt).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>Das Feld wird in absteigender Reihenfolge (Z bis A oder 100 bis 0) sortiert. Diese Option gilt nur für ein <strong>Field</strong>-Objekt in einer <strong>Fields</strong>-Auflistung eines <strong>Index</strong>-Objekts. Wenn Sie diese Konstante nicht angeben, wird das Feld in aufsteigender Reihenfolge (A bis Z oder 0 bis 100) sortiert. Dies ist der Standardwert für <strong>Index</strong>- und <strong>TableDef</strong>-Felder (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>Die Feldgröße ist fest (Standard bei numerischen Feldern).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>Das Feld enthält Hyperlinkinformationen (nur Memofelder).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>Das Feld speichert Replikationsinformationen für Replikate. Dieser Typ von Feld kann nicht gelöscht werden (nur Microsoft Access-Arbeitsbereich).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>Der Wert des Felds kann geändert werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>Die Feldgröße ist variabel (nur Textfelder).</p></td>
</tr>
</tbody>
</table>


Bei Objekten, die noch keiner Auflistung angefügt sind, besteht für diese Eigenschaft Lese-/Schreibzugriff. Bei einem angefügten **Field**-Objekt hängt die Verfügbarkeit der **Attributes**-Eigenschaft vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit des Field-Objekts</p></th>
<th><p>Verfügbarkeit von Attributes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong>-Objekt</p></td>
<td><p>Lese-/Schreibzugriff, bis das <strong>TableDef</strong>-Objekt, an das das <strong>Index</strong>-Objekt angefügt ist, an ein <strong>Database</strong>-Objekt angefügt wird; die Eigenschaft ist dann schreibgeschützt.</p></td>
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


Wenn Sie mehrere Attribute festlegen, können Sie sie kombinieren, indem Sie die entsprechenden Konstanten addieren. Ungültige Werte werden ohne Auftreten eines Fehlers ignoriert.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Attributes**-Eigenschaft für **Field**-, **Relation**- und **TableDef**-Objekte in der Northwind-Datenbank angezeigt.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

