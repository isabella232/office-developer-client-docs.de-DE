---
title: Field.GetChunk-Methode (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 4219445f4e0369479023cffad59899b0aba95232
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602640"
---
# <a name="fieldgetchunk-method-dao"></a>Field.GetChunk-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt den gesamten Inhalt oder einen Teil des Inhalts eines **Memo-** oder **Long Binary** **[Field](field-object-dao.md)** -Objekts in der **[Fields -Auflistung](fields-collection-dao.md)** eines **[Recordset](recordset-object-dao.md)** -Objekts zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . GetChunk(***Offset** _, _*_Bytes_**)

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

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
<td><p><em>Offset</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Die Anzahl von zu überspringenden Bytes, bevor das Kopieren gestartet wird.</p></td>
</tr>
<tr class="even">
<td><p><em>Bytes</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Die Anzahl von Bytes, die zurückgegeben werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Variant

## <a name="remarks"></a>Bemerkungen

The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.

Wenn der Offset 0 ist, beginnt **GetChunk** mit dem Kopieren aus dem ersten Byte des Felds.

Wenn Numbyte größer als die Anzahl der Bytes im Feld ist, gibt **GetChunk** die tatsächliche Anzahl der verbleibenden Bytes im Feld zurück.

> [!NOTE]
> [!HINWEIS] Verwenden Sie ein **Memo**-Feld für Text, und schreiben Sie binäre Daten nur in Felder des Typs **Long Binary**. Andernfalls erzielen Sie unerwünschte Ergebnisse.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
