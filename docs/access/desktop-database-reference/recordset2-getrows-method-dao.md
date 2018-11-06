---
title: Recordset2.GetRows-Methode (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 652bd4ce63164463d58f30a0259a7e4208f118ee
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998736"
---
# <a name="recordset2getrows-method-dao"></a><span data-ttu-id="05d1f-102">Recordset2.GetRows-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="05d1f-102">Recordset2.GetRows method (DAO)</span></span>

<span data-ttu-id="05d1f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05d1f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05d1f-104">Ruft mehrere Zeilen aus einem **[Recordset](recordset-object-dao.md)** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="05d1f-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d1f-105">Syntax</span></span>

<span data-ttu-id="05d1f-106">*Ausdruck* . GetRows (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="05d1f-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="05d1f-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="05d1f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="05d1f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05d1f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05d1f-109">Name</span><span class="sxs-lookup"><span data-stu-id="05d1f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="05d1f-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="05d1f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="05d1f-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="05d1f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="05d1f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05d1f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05d1f-113"><em>NumRows</em></span><span class="sxs-lookup"><span data-stu-id="05d1f-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="05d1f-114">Optional</span><span class="sxs-lookup"><span data-stu-id="05d1f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="05d1f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="05d1f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="05d1f-116">Die Anzahl der abzurufenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="05d1f-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="05d1f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05d1f-117">Return value</span></span>

<span data-ttu-id="05d1f-118">Variant</span><span class="sxs-lookup"><span data-stu-id="05d1f-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="05d1f-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05d1f-119">Remarks</span></span>

<span data-ttu-id="05d1f-120">Verwenden Sie die **GetRows** -Methode, um Datensätze aus einem **Recordset** zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="05d1f-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="05d1f-121">**GetRows** gibt ein zweidimensionales Array zurück.</span><span class="sxs-lookup"><span data-stu-id="05d1f-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="05d1f-122">Das erste Subskript identifiziert das Feld und das zweite identifiziert die Zeilenanzahl.</span><span class="sxs-lookup"><span data-stu-id="05d1f-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="05d1f-123">Beispielsweise `intField` das Feld dar und `intRecord` Nummer der Zeile:</span><span class="sxs-lookup"><span data-stu-id="05d1f-123">For example, `intField` represents the field, and `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="05d1f-124">Um den ersten Feldwert in der zweiten zurückgegebenen Zeile zu erhalten, verwenden Sie folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="05d1f-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="05d1f-125">Um den zweiten Feldwert in der ersten Zeile zu erhalten, verwenden Sie folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="05d1f-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="05d1f-126">Die avarRecords-Variable wird automatisch zu einem zweidimensionalen Array, wenn **GetRows** Daten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="05d1f-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="05d1f-127">Wenn Sie mehr Zeilen anfordern, als verfügbar sind, gibt **GetRows** nur die verfügbaren Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="05d1f-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="05d1f-128">Sie können mithilfe der Visual Basic für Applikationen-Funktion **UBound** feststellen, wie viele Zeilen durch **GetRows** abgerufen wurden, denn die Größe des Arrays entspricht der Anzahl zurückgegebener Zeilen.</span><span class="sxs-lookup"><span data-stu-id="05d1f-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="05d1f-129">Wenn Sie die Ergebnisse in einer **Variant** aufgerufen VARIANZA zurückgegeben, konnte Sie beispielsweise den folgenden Code verwenden, um zu bestimmen, wie viele Zeilen tatsächlich zurückgegeben wurden:</span><span class="sxs-lookup"><span data-stu-id="05d1f-129">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="05d1f-p103">Sie müssen "+ 1" verwenden, da sich die erste zurückgegebene Zeile im Element 0 des Arrays befindet. Wie viele Zeilen abgerufen werden können, hängt von dem verfügbaren Speicher ab. Verwenden Sie GetRows nicht zum Abrufen einer ganzen Tabelle in ein Array, wenn sie groß ist.</span><span class="sxs-lookup"><span data-stu-id="05d1f-p103">You need to use "+ 1" because the first row returned is in the 0 element of the array. The number of rows that you can retrieve is constrained by the amount of available memory. You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="05d1f-133">Da **GetRows** alle Felder des **Recordsets** in das Array zurückgibt, einschließlich "Memo"- und "Long Binary"-Felder, sollten Sie eine Abfrage verwenden, die die zurückgegebenen Felder beschränkt.</span><span class="sxs-lookup"><span data-stu-id="05d1f-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="05d1f-134">Nach dem Aufruf von **GetRows** wird der aktuelle Datensatz in der nächsten ungelesenen Zeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="05d1f-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="05d1f-135">**GetRows** hat d. h., die gleiche Auswirkung auf den aktuellen Datensatz als Numrows **Verschieben**.</span><span class="sxs-lookup"><span data-stu-id="05d1f-135">That is, **GetRows** has the same effect on the current record as **Move**numrows.</span></span>

<span data-ttu-id="05d1f-p105">Wenn Sie versuchen, alle Zeilen mithilfe mehrerer **GetRows** -Aufrufe abzurufen, verwenden Sie die **[EOF](recordset2-eof-property-dao.md)** -Eigenschaft, um sicherzustellen, dass Sie sich am Ende des **Recordsets** befinden. **GetRows** gibt weniger als die angeforderte Anzahl zurück, wenn es sich am Ende des **Recordsets** befindet oder wenn es im angeforderten Bereich keine Zeile abrufen kann. Wenn Sie zum Beispiel versuchen, zehn Datensätze abzurufen, den fünften aber nicht abrufen können, gibt **GetRows** vier Datensätze zurück und nacht den fünften Datensatz zum aktuellen Datensatz. Es wird kein Laufzeitfehler generiert. Das kann auftreten, wenn ein anderer Benutzer einen Datensatz in einem **Recordset** vom "dynaset"-Typ löscht. Das Beispiel demonstriert das Vorgehen in einem solchen Fall.</span><span class="sxs-lookup"><span data-stu-id="05d1f-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset2-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="05d1f-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="05d1f-142">Example</span></span>

<span data-ttu-id="05d1f-p106">Dieses Beispiel verwendet die **GetRows** -Methode, um eine angegebene Anzahl Zeilen aus einem **Recordset** abzurufen und ein Array mit den daraus resultierenden Daten zu füllen. Die **GetRows** -Methode gibt in zwei Fällen weniger als die gewünschte Anzahl von Zeilen zurück: wenn **EOF** erreicht wurde oder wenn **GetRows** versucht hat, einen Datensatz abzurufen, der von einem anderen Benutzer gelöscht wurde. Die Funktion gibt nur im zweiten Fall **False** zurück. Für das Ausführen dieser Prozedur ist die "GetRowsOK"-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="05d1f-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

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
