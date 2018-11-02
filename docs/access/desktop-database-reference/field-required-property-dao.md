---
title: Field.Required-Eigenschaft (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25ba678f759fefa460dd505cded6e05b3e96fdf5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928354"
---
# <a name="fieldrequired-property-dao"></a>Field.Required-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob ein **[Field](field-object-dao.md)** -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.

## <a name="syntax"></a>Syntax

*Ausdruck* . Erforderlich

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein **Field**-Objekt, das noch nicht an die **Fields**-Auflistung angehängt wurde, hat Lese-/Schreibzugriff für diese Eigenschaft.

Die Verfügbarkeit der **Required**-Eigenschaft hängt von dem Objekt ab, das die [Fields](fields-collection-dao.md)-Auflistung enthält, wie in der folgenden Tabelle dargestellt.

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


Mit der **Required**-Eigenschaft können Sie in Kombination mit der **[AllowZeroLength](field-allowzerolength-property-dao.md)** -, **[ValidateOnSet](field-validateonset-property-dao.md)** - oder **[ValidationRule](field-validationrule-property-dao.md)** -Eigenschaft die Gültigkeit des Werts der **[Value](field-value-property-dao.md)** -Eigenschaft für dieses **Field**-Objekt überprüfen. Wenn die **Required**-Eigenschaft den Wert **False**hat, kann das Feld **null**-Werte enthalten und ebenso Werte, die die von den Eigenschaften **AllowZeroLength** und **ValidationRule** festgelegten Bedingungen erfüllen.


> [!NOTE]
> <P>[!HINWEIS] Wenn Sie diese Eigenschaft sowohl für ein <STRONG>Index</STRONG>- als auch für ein <STRONG>Field</STRONG>-Objekt festlegen können, sollten Sie es für das <STRONG>Field</STRONG>-Objekt angeben. Die Gültigkeit des Werts dieser Eigenschaft wird zuerst für das <STRONG>Field</STRONG>-Objekt und erst danach für das <STRONG>Index</STRONG>-Objekt überprüft.</P>



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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

