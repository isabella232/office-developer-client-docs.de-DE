---
title: Recordset2.GetRows-Methode (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 42f5153ae2804b81fd98c32587bba787020e306d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596918"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Ruft mehrere Zeilen aus einem **[Recordset](recordset-object-dao.md)**-Objekt ab.

## <a name="syntax"></a>Syntax

*expression* .GetRows(***NumRows***)

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

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
<td><p><em>NumRows</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Die Anzahl der abzurufenden Zeilen.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Variant

## <a name="remarks"></a>Bemerkungen

Mit der **GetRows**-Methode kopieren Sie Datensätze aus einem **Recordset**. **GetRows** gibt ein zweidimensionales Array zurück. Der erste Index identifiziert das Feld und der zweite die Nummer der Zeile. Beispielsweise stellt `intField` das Feld dar, und `intRecord` identifiziert die Zeilennummer:

`avarRecords(intField, intRecord)`

Verwenden Sie einen ähnlichen Code wie im folgenden Beispiel, damit der erste Feldwert in der zweiten Zeile zurückgegeben wird:

`field1 = avarRecords(0,1)`

Verwenden Sie einen ähnlichen Code wie im folgenden Beispiel, um den zweiten Feldwert in der ersten Zeile anzuzeigen:

`field2 = avarRecords(1,0)`

Die Variable AvarRecords wird automatisch zu einem zweidimensionalen Array, wenn **GetRows** Daten zurückgibt.

Wenn Sie mehr Zeilen anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Zeilen zurück. Sie können mithilfe der Visual Basic für Applikationen-Funktion **UBound** feststellen, wie viele Zeilen durch **GetRows** abgerufen wurden, denn die Größe des Arrays entspricht der Anzahl zurückgegebener Zeilen. Wurden die Ergebnisse beispielsweise in einen **Variant**-Wert namens varA zurückgegeben, können Sie mit dem folgenden Code ermitteln, wie viele Zeilen zurückgegeben wurden:

`numReturned = UBound(varA,2) + 1`

Sie müssen "+ 1" verwenden, das sich die erste zurückgegebene Zeile im 0-Element des Arrays befindet. Die Anzahl der Zeilen, die Sie abrufen können, ist durch den verfügbaren Arbeitsspeicher beschränkt. Sie sollten **GetRows** nicht verwenden, um eine ganze Tabelle in ein Array abzurufen, wenn sie groß ist.

Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.

Nach dem Aufrufen von **GetRows** wird der aktuelle Datensatz an der nächsten ungelesenen Zeile positioniert. Das heißt, **GetRows** hat die gleiche Auswirkung auf den aktuellen Datensatz wie **Move** numrows.

If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset2-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.

## <a name="example"></a>Beispiel

This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.

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
