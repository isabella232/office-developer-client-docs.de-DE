---
title: Field2.Required-Eigenschaft (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709047"
---
# <a name="field2required-property-dao"></a>Field2.Required-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013


Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein **Field2**-Objekt einen Nicht-Nullwert erfordert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Erforderlich

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei einem **Field2**-Objekt, das der **Fields**-Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.

Die Verfügbarkeit der **Required**-Eigenschaft hängt vom Objekt ab, in dem die **[Fields](fields-collection-dao.md)** -Auflistung enthalten ist (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit der Fields-Auflistung</p></th>
<th><p>Required-Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong>-Objekt</p></td>
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


Die Eigenschaft **Required** und **AllowZeroLength**, **ValidateOnSet**oder **ValidationRule** -Eigenschaft können Sie um die Gültigkeit der Einstellung der **Value** -Eigenschaft für das **Field2** -Objekt zu bestimmen. Wenn die **Required**-Eigenschaft den Wert **False**hat, kann das Feld **null**-Werte enthalten und ebenso Werte, die die von den Eigenschaften **AllowZeroLength** und **ValidationRule** festgelegten Bedingungen erfüllen.


> [!NOTE]
> [!HINWEIS] Wenn Sie diese Eigenschaft für ein **Index**-Objekt oder ein **Field2**-Objekt festlegen können, legen Sie sie für das **Field2**-Objekt fest. Die Gültigkeit der Eigenschafteneinstellung für ein **Field2**-Objekt wird vor der eines **Index**-Objekts überprüft.



## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die Required-Eigenschaft, um anzugeben, welche Felder in drei verschiedenen Tabellen Daten enthalten müssen, damit ein neuer Datensatz hinzugefügt wird.  Die RequiredOutput-Prozedur ist zum Ausführen dieser Prozedur erforderlich.

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

