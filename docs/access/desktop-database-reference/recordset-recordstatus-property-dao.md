---
title: Recordset.RecordStatus-Eigenschaft (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 6fbd6909-6191-d7be-9a3a-1e9908dacc2b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195591(v=office.15)
ms:contentKeyID: 48545543
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1102617
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60a9e840e611988f33a66f67aff11ac5da3fe5ad
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919325"
---
# <a name="recordsetrecordstatus-property-dao"></a><span data-ttu-id="9d62e-102">Recordset.RecordStatus-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d62e-102">Recordset.RecordStatus property (DAO)</span></span>


<span data-ttu-id="9d62e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d62e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9d62e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d62e-104">Syntax</span></span>

<span data-ttu-id="9d62e-105">*Ausdruck* . RecordStatus</span><span class="sxs-lookup"><span data-stu-id="9d62e-105">*expression* .RecordStatus</span></span>

<span data-ttu-id="9d62e-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d62e-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d62e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d62e-107">Remarks</span></span>

<span data-ttu-id="9d62e-108">Der Wert der **RecordStatus**-Eigenschaft gibt an, ob und wie der aktuelle Datensatz an der nächsten optimistischen Batchaktualisierung beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="9d62e-108">The value of the **RecordStatus** property indicates whether and how the current record will be involved in the next optimistic batch update.</span></span>

<span data-ttu-id="9d62e-p101">Wenn ein Benutzer einen Datensatz ändert, wird die **RecordStatus**-Eigenschaft für diesen Datensatz automatisch in **dbRecordModified** geändert. Wenn ein Datensatz hinzugefügt oder gelöscht wird, enthält **RecordStatus** ebenfalls die entsprechende Konstante. Wenn Sie dann eine **[Update](recordset-update-method-dao.md)** -Methode im Batchmodus verwenden, sendet DAO für jeden Datensatz, basierend auf der **RecordStatus**-Eigenschaft des Datensatzes, einen geeigneten Vorgang an den Remoteserver.</span><span class="sxs-lookup"><span data-stu-id="9d62e-p101">When a user changes a record, the **RecordStatus** for that record automatically changes to **dbRecordModified**. Similarly, if a record is added or deleted, **RecordStatus** reflects the appropriate constant. When you then use a batch-mode **[Update](recordset-update-method-dao.md)** method, DAO will submit an appropriate operation to the remote server for each record, based on the record's **RecordStatus** property.</span></span>

## <a name="example"></a><span data-ttu-id="9d62e-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9d62e-112">Example</span></span>

<span data-ttu-id="9d62e-p102">In diesem Beispiel werden die Eigenschaften RecordStatus und DefaultCursorDriver verwendet, um zu zeigen, wie Änderungen eines lokalen Recordset-Objekts während einer Batchaktualisierung verfolgt werden. Zum Ausführen dieser Prozedur ist die RecordStatusOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d62e-p102">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating. The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

