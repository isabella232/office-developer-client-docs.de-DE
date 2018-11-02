---
title: Recordset2.GetRows-Methode (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d0489361a3c739527fb44db0c566986dc2a40a0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921397"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

Ruft mehrere Zeilen aus einem **[Recordset](recordset-object-dao.md)** -Objekt ab.

## <a name="syntax"></a>Syntax

*Ausdruck* . GetRows (***NumRows***)

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

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
<td><p>NumRows</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Die Anzahl der abzurufenden Zeilen.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Variant

## <a name="remarks"></a>Hinweise

Mit der **GetRows**-Methode kopieren Sie Datensätze aus einem **Recordset**. **GetRows** gibt ein zweidimensionales Array zurück. Der erste Index identifiziert das Feld und der zweite die Nummer der Zeile. Beispielsweise stellt intField das Feld dar, und intRecord identifiziert die Zeilennummer:

AvarRecords (IntField, IntRecord)

Um den ersten Feldwert in der zweiten zurückgegebenen Zeile zu erhalten, verwenden Sie folgenden Code:

Feld1 = avarRecords(0,1)

Um den zweiten Feldwert in der ersten Zeile zu erhalten, verwenden Sie folgenden Code:

Field2 = avarRecords(1,0)

Die avarRecords-Variable wird automatisch zu einem zweidimensionalen Array, wenn **GetRows** Daten zurückgibt.

Wenn Sie mehr Zeilen anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Zeilen zurück. Sie können mithilfe der Visual Basic für Applikationen-Funktion **UBound** feststellen, wie viele Zeilen durch **GetRows** abgerufen wurden, denn die Größe des Arrays entspricht der Anzahl zurückgegebener Zeilen. Wenn Sie die Ergebnisse in einer **Variant** aufgerufen VARIANZA zurückgegeben, konnte Sie beispielsweise den folgenden Code verwenden, um zu bestimmen, wie viele Zeilen tatsächlich zurückgegeben wurden:

NumReturned = UBound(varA,2) + 1

Sie müssen "+ 1" verwenden, da sich die erste zurückgegebene Zeile im Element 0 des Arrays befindet. Wie viele Zeilen abgerufen werden können, hängt von dem verfügbaren Speicher ab. Verwenden Sie GetRows nicht zum Abrufen einer ganzen Tabelle in ein Array, wenn sie groß ist.

Da **GetRows** alle Felder des **Recordsets** in das Array zurückgibt, einschließlich "Memo"- und "Long Binary"-Felder, sollten Sie eine Abfrage verwenden, die die zurückgegebenen Felder beschränkt.

Nach dem Aufruf von **GetRows** wird der aktuelle Datensatz in der nächsten ungelesenen Zeile positioniert. **GetRows** hat d. h., die gleiche Auswirkung auf den aktuellen Datensatz als Numrows **Verschieben**.

Wenn Sie versuchen, alle Zeilen mithilfe mehrerer **GetRows** -Aufrufe abzurufen, verwenden Sie die **[EOF](recordset2-eof-property-dao.md)** -Eigenschaft, um sicherzustellen, dass Sie sich am Ende des **Recordsets** befinden. **GetRows** gibt weniger als die angeforderte Anzahl zurück, wenn es sich am Ende des **Recordsets** befindet oder wenn es im angeforderten Bereich keine Zeile abrufen kann. Wenn Sie zum Beispiel versuchen, zehn Datensätze abzurufen, den fünften aber nicht abrufen können, gibt **GetRows** vier Datensätze zurück und nacht den fünften Datensatz zum aktuellen Datensatz. Es wird kein Laufzeitfehler generiert. Das kann auftreten, wenn ein anderer Benutzer einen Datensatz in einem **Recordset** vom "dynaset"-Typ löscht. Das Beispiel demonstriert das Vorgehen in einem solchen Fall.

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die **GetRows** -Methode, um eine angegebene Anzahl Zeilen aus einem **Recordset** abzurufen und ein Array mit den daraus resultierenden Daten zu füllen. Die **GetRows** -Methode gibt in zwei Fällen weniger als die gewünschte Anzahl von Zeilen zurück: wenn **EOF** erreicht wurde oder wenn **GetRows** versucht hat, einen Datensatz abzurufen, der von einem anderen Benutzer gelöscht wurde. Die Funktion gibt nur im zweiten Fall **False** zurück. Für das Ausführen dieser Prozedur ist die "GetRowsOK"-Funktion erforderlich.

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
