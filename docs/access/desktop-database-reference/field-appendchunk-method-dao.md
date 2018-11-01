---
title: Field.AppendChunk Method (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44aef9e335b606b88dfcc1446a3d167627b1db2b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870954"
---
# <a name="fieldappendchunk-method-dao"></a>Field.AppendChunk Method (DAO)

**Betrifft**: Access 2013, Office 2013

Fügt Daten aus einem Zeichenfolgenausdruck an ein Field-Objekt vom Typ Memo oder Long Binary in einem Recordset an.

## <a name="syntax"></a>Syntax

*Ausdruck* . AppendChunk (***Val***)

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

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
<td><p>Val</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein Ausdruck oder eine Variable vom Typ Variant (Untertyp String) mit den Daten, die an das <strong>Field</strong>-Objekt angefügt werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die Methoden AppendChunk und GetChunk verwenden, um auf Teilmengen der Daten in einem Memo- oder Long Binary-Feld zuzugreifen.

Mithilfe dieser Methoden können Sie auch Zeichenfolgenspeicher freigeben, wenn Sie mit Memo- und Long Binary-Feldern arbeiten. Für bestimmte Vorgänge (z. B. Kopieren) sind temporäre Zeichenfolgen erforderlich. Bei begrenztem Zeichenfolgenspeicher müssen Sie evtl. Abschnitte eines Felds statt das ganze Feld verwenden.

Wenn Sie **AppendChunk** verwenden, ohne dass ein aktueller Datensatz vorhanden ist, tritt ein Fehler auf.

> [!NOTE]
> Durch den ersten **AppendChunk**-Vorgang (nach einem **[Edit](recordset-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Aufruf) werden die Daten einfach in das Feld geschrieben, und vorhandene Daten werden überschrieben. Nachfolgende **AppendChunk**-Aufrufe innerhalb derselben **Edit**- oder **AddNew**-Sitzung werden anschließend zu den vorhandenen Daten hinzugefügt.

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
