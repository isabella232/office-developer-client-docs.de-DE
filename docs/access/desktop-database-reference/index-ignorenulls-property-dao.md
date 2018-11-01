---
title: Index.IgnoreNulls Property (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e7fd7b98b246f4fda24426d9376cc5edc2553b8e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870310"
---
# <a name="indexignorenulls-property-dao"></a>Index.IgnoreNulls Property (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der angibt, ob Datensätze, deren Indexfelder Nullwerte enthalten, über Indexeinträge verfügen (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . IgnoreNulls

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein neues **[Index](index-object-dao.md)** objekt, das noch nicht an eine Auflistung angehängt wurde, hat Lese-/Schreibzugriff auf diese Eigenschaft. Ein vorhandenes **Index**objekt in einer **[Indexes](indexes-collection-dao.md)** -Auflistung hat nur Lesezugriff auf die Eigenschaft.

Sie können einen Index für ein Feld definieren, um die Suche nach Datensätzen zu beschleunigen. Wenn Sie in einem indizierten Feld **null**-Einträge zulassen und erwarten, dass viele Einträge den Wert **null** haben, können Sie die **IgnoreNulls**-Eigenschaft für das **Index**-Objekt auf den Wert **True** festlegen, um den vom Index verwendeten Speicherplatz zu reduzieren.

Die Einstellungen der **IgnoreNulls**-Eigenschaft und der **[Required](field-required-property-dao.md)** -Eigenschaft legen gemeinsam fest, ob ein Datensatz mit einem **null**-Indexwert einen Indexeintrag hat.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>IgnoreNulls-Wert</p></th>
<th><p>Required-Wert</p></th>
<th><p>Dann</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>False</p></td>
<td><p>Im Indexfeld ist ein Nullwert erlaubt. Es wird kein Indexeintrag hinzugefügt.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>False</p></td>
<td><p>Im Indexfeld ist ein Nullwert erlaubt. Es wird ein Indexeintrag hinzugefügt.</p></td>
</tr>
<tr class="odd">
<td><p>True oder False</p></td>
<td><p>True</p></td>
<td><p>Im Indexfeld ist kein Nullwert erlaubt. Es wird kein Indexeintrag hinzugefügt.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Beispiel

In diesem Beispiel wird die **IgnoreNulls**-Eigenschaft eines neuen **Index**-Objekts basierend auf der Benutzereingabe auf **True** oder **False** gesetzt. Anschließend werden die Auswirkungen auf ein **Recordset**-Objekt mit einem Datensatz gezeigt, dessen Schlüsselfeld einen **Null**-Wert enthält.

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
