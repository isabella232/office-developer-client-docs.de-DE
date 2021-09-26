---
title: Database.CreateTableDef-Methode (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 64cb20daaf235ebdd736771d571881cec17950f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562748"
---
# <a name="databasecreatetabledef-method-dao"></a>Database.CreateTableDef-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[TableDef](tabledef-object-dao.md)**-Objekt (nur für Microsoft Access-Arbeitsbereiche). .

## <a name="syntax"></a>Syntax

*Ausdruck* .CreateTableDef(***Name** _, _*_Attribute_*_, _*_SourceTableName_*_, _*_Connect_**)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>), der das neue <strong>TableDef</strong>-Objekt eindeutig benennt. Unter der <strong><a href="tabledef-name-property-dao.md">Name</a></strong>-Eigenschaft finden Sie Einzelheiten zu gültigen <strong>TableDef</strong>-Namen.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante oder Kombination aus Konstanten, mit der mindestens ein Merkmal des neuen <strong>TableDef</strong>-Objekts angegeben wird. Weitere Informationen finden Sie im Thema zur <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong>-Eigenschaft.</p></td>
</tr>
<tr class="odd">
<td><p><em>SourceTableName</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>), der den Namen einer Tabelle in einer externen Datenbank enthält, bei der es sich um die ursprüngliche Quelle der Daten handelt. Die Quellenzeichenfolge wird zur Eigenschafteneinstellung <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> des neuen <strong>TableDef</strong>-Objekts.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>) mit Informationen über die Quelle einer geöffneten Datenbank, einer Datenbank, die in einer Pass-Through-Abfrage verwendet wird, oder einer verknüpften Tabelle. Weitere Informationen zu gültigen Verbindungszeichenfolgen finden Sie unter der Eigenschaft <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

TableDef

## <a name="remarks"></a>Hinweise

Wenn Sie einen oder mehrere der optionalen Teile für die **CreateTableDef**-Methode weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschaften ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.

Wenn „name“ sich auf ein Objekt bezieht, das bereits ein Mitglied einer Auflistung ist, oder wenn Sie im angefügten Objekt **TableDef** oder **[Field](field-object-dao.md)** eine ungültige Eigenschaft angeben, tritt bei Verwendung der Methode **[Append](tabledefs-append-method-dao.md)** ein Laufzeitfehler auf. Sie können ein **TableDef**-Objekt außerdem erst dann an die **TableDefs**-Sammlung anfügen, nachdem Sie mindestens ein **Field**-Objekt für das **TableDef**-Objekt definiert haben.

Um ein **TableDef**-Objekt aus der **[TableDefs](tabledefs-collection-dao.md)**-Auflistung zu entfernen, verwenden Sie die **[Delete](tabledefs-delete-method-dao.md)**-Methode für die Auflistung.

## <a name="example"></a>Beispiel

Dieses Beispiel erstellt ein neues **TableDef**-Objekt in der Northwind-Datenbank.

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel werden die **CreateTableDef**- und die **FillCache**-Methode sowie die **CacheSize**-, die **CacheStart**- und die **SourceTableName**-Eigenschaft verwendet, um die Datensätze in einer verknüpften Tabelle zwei Mal aufzuzählen. Anschließend werden die Einträge zweimal mit einem Cache für 50 Datensätze aufgezählt. Anschließend werden die Leistungsstatistiken für die Ausführung mit und ohne Zwischenspeicherung über die verknüpfte Tabelle angezeigt.

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
