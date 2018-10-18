---
<span data-ttu-id="45815-101"><<<<<<< HEAD-Titel: Status--Eigenschaft (Beispiel) (Field) (VB) TOCTitle: Status--Eigenschaft (Beispiel) (Field) (VB) === Titel: Status--Eigenschaft (Beispiel) (Field) (VB) TOCTitle: Status--Eigenschaft (Beispiel) (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="45815-101"><<<<<<< HEAD title: Status Property Example (Field) (VB) TOCTitle: Status Property Example (Field) (VB) ======= title: Status property example (Field) (VB) TOCTitle: Status property example (Field) (VB)</span></span>
>>>>>>> <span data-ttu-id="45815-102">Master Ms:assetid: 1dc2807f-f469-de97-1280-4b1984b271b4 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248969(v=office.15) Ms:contentKeyID: 48543601 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="45815-102">master ms:assetid: 1dc2807f-f469-de97-1280-4b1984b271b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248969(v=office.15) ms:contentKeyID: 48543601 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="45815-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="45815-103"><<<<<<< HEAD</span></span>
# <a name="status-property-example-field-vb"></a><span data-ttu-id="45815-104">Status-Eigenschaft (Beispiel) (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="45815-104">Status Property Example (Field) (VB)</span></span>
=======
# <a name="status-property-example-field-vb"></a><span data-ttu-id="45815-105">Status--Eigenschaft (Beispiel) (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="45815-105">Status property example (Field) (VB)</span></span>
>>>>>>> <span data-ttu-id="45815-106">master</span><span class="sxs-lookup"><span data-stu-id="45815-106">master</span></span>


<span data-ttu-id="45815-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="45815-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45815-p101">Im folgenden Beispiel wird unter Verwendung des [Internet Publishing-Anbieters](microsoft-ole-db-provider-for-internet-publishing.md) ein Dokument in einem Ordner mit Schreib-/Lesezugriff geöffnet. Die [Status](status-property-ado-field.md)-Eigenschaft eines [Field](field-object-ado.md)-Objekts des [Record](record-object-ado.md)-Objekts wird auf **adFieldPendingInsert** festgelegt und dann auf **adFieldOk** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="45815-p101">The following example opens a document from a read/write folder using the [Internet Publishing Provider](microsoft-ole-db-provider-for-internet-publishing.md). The [Status](status-property-ado-field.md) property of a [Field](field-object-ado.md) object of the [Record](record-object-ado.md) will first be set to **adFieldPendingInsert**, then be updated to **adFieldOk**.</span></span>

```vb
    'BeginStatusFieldVB
        
     ' to integrate this code replace the values in the source string
    
    Sub Main()
        
       Dim File As ADODB.Record
       Dim strFile As String
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
       
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       ' Open a read/write document
       File.Source = strFile
       File.ActiveConnection = Cnxn
       File.Mode = adModeReadWrite
       File.Open
    
       Debug.Print "Append a couple of fields"
       
       File.Fields.Append "chektest:fld1", adWChar, 42, adFldUpdatable, "fld1"
       File.Fields.Append "chektest:fld2", adWChar, 42, adFldUpdatable, "fld2"
       
       Debug.Print "status for the fields"
       Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert
       Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update
       
       Debug.Print "Update succeeds"
       Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert + adFieldUnavailable
       Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert + adFieldUnavailable
        
        ' resume default error-handling
       On Error GoTo 0
         
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
          
    End Sub
    'EndStatusFieldVB
```

<br/>

<span data-ttu-id="45815-p102">Im folgenden Beispiel wird ein bekanntes **Field** -Objekt aus einem in einem Dokument geöffneten **Record** -Objekt gelöscht. Die **Status** -Eigenschaft wird zuerst auf **adFieldOK** und dann auf **adFieldPendingUnknown** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45815-p102">The following example deletes a known **Field** from a **Record** opened from a document. The **Status** property will first be set to **adFieldOK**, then **adFieldPendingUnknown**.</span></span>

```vb
    'BeginStatusField2VB
    
    ' to integrate this code replace the values in the source string
    
    Sub Main()
    
       Dim File As ADODB.Record
       Dim fld As ADODB.Field
       Dim strFile As String
       
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       
        ' create connection as a URL
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       ' Open a read/write document
       File.Open strFile, Cnxn, adModeReadWrite
       Debug.Print File.Fields("chektest:fld1").Status ' should be adFldOK
       
       ' Delete a field which already exists in the collection
       File.Fields.Delete "chektest:fld1"
       Set fld = File.Fields("chektest:fld1")
       Debug.Print File.Fields("chektest:fld1").Status   ' Pending delete
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update
       
       Debug.Print "Deleted"
       Debug.Print fld.Status   ' Pending unknown
    
        ' resume default error-handling
       On Error GoTo 0
         
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
    
    End Sub
    'EndStatusField2VB
```

<br/>

<span data-ttu-id="45815-p103">Der folgende Code löscht ein **Field** -Objekt aus einem **Record** -Objekt, das in einem schreibgeschützten Dokument geöffnet ist. Die **Status** -Eigenschaft wird auf **adFieldPendingDelete** festgelegt. Mit [Update](update-method-ado.md) schlägt der Löschvorgang fehl, und die **Status** -Eigenschaft lautet **adFieldPendingDelete** plus **adFieldPermissionDenied**. [CancelUpdate](cancelupdate-method-ado.md) löscht die ausstehende **Status** -Einstellung.</span><span class="sxs-lookup"><span data-stu-id="45815-p103">The following code deletes a **Field** from a **Record** opened on a read-only document. **Status** will be set to **adFieldPendingDelete**. At [Update](update-method-ado.md), the delete will fail and **Status** will be **adFieldPendingDelete** plus **adFieldPermissionDenied**. [CancelUpdate](cancelupdate-method-ado.md) clears the pending **Status** setting.</span></span>

```vb
    Sub Main()
       Dim File As ADODB.Record
       Dim fld As ADODB.Field
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       Dim strFile As String
       
        ' create connection as a URL
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
    
       ' Open a read/write document
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       File.Open strFile, Cnxn, adModeReadWrite, adCreateCollection Or adOpenIfExists
    
       Debug.Print "Try to delete something without permission"
       File.Fields.Delete ("RESOURCE_PARSENAME")
       Set fld = File.Fields("RESOURCE_PARSENAME")
       
       Debug.Print "Pending delete"
       Debug.Print fld.Status   ' Pending delete
       Debug.Print "Delete should fail on Update"
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update   ' Should fail
       
       Debug.Print fld.Status   ' Pending delete plus error
       File.Fields.CancelUpdate
       Debug.Print fld.Status   ' Okay
        
        ' resume default error-handling
       On Error GoTo 0
            
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
       
    End Sub
    'EndStatusField3VB
```
