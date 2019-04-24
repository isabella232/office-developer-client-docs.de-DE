---
title: Field2. Attributes-Eigenschaft (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292888"
---
# <a name="field2attributes-property-dao"></a>Field2. Attributes-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der ein oder mehrere Merkmale eines **Field2**-Objekts angibt. **Long**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Attribute

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Dieser Wert gibt die Merkmale des Felds an, das durch das **Field2**-Objekt dargestellt wird. Er kann aus einer Kombinationen der folgenden Konstanten bestehen.

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
<td><p><strong>Dbautoincrfield festgelegt</strong></p></td>
<td><p>Der Feldwert für neue Datensätze wird automatisch auf einen eindeutigen Long Integer-Wert erhöht, der nicht geändert werden kann (wird in einem Microsoft Access-Arbeitsbereich nur bei Microsoft Access-Datenbanktabellen unterstützt).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbAbsteigend</strong></p></td>
<td><p>Das Feld wird absteigend sortiert (Z-bis A-oder 100-0). Diese Option gilt nur für ein <strong>Field2</strong> -Objekt in <strong></strong> einer Fields-Auflistung eines <strong>Index</strong> -Objekts. Wenn Sie diese Konstante weglassen, wird das Feld aufsteigend sortiert (A-Z oder 0 bis 100). Dies ist der Standardwert für <strong>Index</strong> -und <strong>TableDef</strong> -Felder (nur Microsoft Access-Arbeitsbereiche)..</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedfield</strong></p></td>
<td><p>Die Feldgröße ist fest (Standard bei numerischen Feldern).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkfield</strong></p></td>
<td><p>Das Feld enthält Hyperlinkinformation (nur Memofelder).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemfield</strong></p></td>
<td><p>Das Feld speichert Replikationsinformationen für Replikate. Dieser Feldtyp kann nicht gelöscht werden (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbAktualisierfield</strong></p></td>
<td><p>Der Feldwert kann geändert werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariablefield</strong></p></td>
<td><p>Die Feldgröße ist variabel (nur Textfelder).</p></td>
</tr>
</tbody>
</table>


Bei Objekten, die noch keiner Auflistung angefügt sind, besteht für diese Eigenschaft Lese-/Schreibzugriff. Bei einem angefügten **Field2**-Objekt hängt die Verfügbarkeit der **Attributes**-Eigenschaft vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist.

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
<td><p>Mit Lese-/Schreibzugriff bis das <strong>TableDef</strong>-Objekt, dem das <strong>Index</strong>-Objekt angefügt wird, einem <strong>Database</strong>-Objekt angefügt wird; dann ist die Eigenschaft schreibgeschützt.</p></td>
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

Dieses Beispiel zeigt die **Attributes**-Eigenschaft für die Objekte **Field2**, **Relation** und **TableDef** in der Nordwind-Datenbank an.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
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

