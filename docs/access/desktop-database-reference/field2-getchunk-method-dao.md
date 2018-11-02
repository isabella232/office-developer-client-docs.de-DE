---
title: Field2.GetChunk-Methode (DAO)
TOCTitle: GetChunk Method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09660c472a6fd799c111214dafe3266cdec9eced
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926647"
---
# <a name="field2getchunk-method-dao"></a>Field2.GetChunk-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt den gesamten oder einen Teil des Inhalts eines Objekts **vom Typ Memo** oder **Long Field2** in der **[Fields](fields-collection-dao.md)** -Auflistung eines **[Recordset](recordset-object-dao.md)** -Objekts.

## <a name="syntax"></a>Syntax

*Ausdruck* . GetChunk (***Offset***, ***Byte***)

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Offset</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Die Anzahl von zu überspringenden Bytes, bevor das Kopieren gestartet wird.</p></td>
</tr>
<tr class="even">
<td><p>Bytes</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Die Anzahl von Bytes, die zurückgegeben werden sollen.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Variant

## <a name="remarks"></a>Bemerkungen

Die durch GetChunk zurückgegebenen Bytes werden Variable zugewiesen. Mithilfe von GetChunk geben Sie jeweils einen Teil des gesamten Datenwerts zurück. Sie können die AppendChunk-Methode verwenden, um die Teile wieder zusammenzufügen.

Wenn offset gleich 0 ist, beginnt GetChunk ab dem ersten Byte des Felds mit dem Kopieren.

Wenn Numbytes größer als die Anzahl von Bytes im Feld ist, gibt **GetChunk** die tatsächliche Anzahl von verbliebenen Bytes im Feld zurück.


> [!NOTE]
> <P>[!HINWEIS] Verwenden Sie ein <STRONG>Memo</STRONG>-Feld für Text, und schreiben Sie binäre Daten nur in Felder des Typs <STRONG>Long Binary</STRONG>. Andernfalls erzielen Sie unerwünschte Ergebnisse.</P>



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
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
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
