---
<span data-ttu-id="07e6a-101"><<<<<<< HEAD-Titel: Description, HelpContext, HelpFile Eigenschaften Beispiel) (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Anzahl, Source- und SQLState Eigenschaften Beispiel) (VB) === Titel: Beschreibung, HelpContext-und HelpFile-Eigenschaft (Beispiel) (VB) TOCTitle: Eigenschaften Description, HelpContext, HelpFile, NativeError, Anzahl, Source- und SQLState (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="07e6a-101"><<<<<<< HEAD title: Description, HelpContext, HelpFile Properties Example (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB) ======= title: Description, HelpContext, HelpFile properties example (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="07e6a-102">Master Ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) Ms:contentKeyID: 48544304 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="07e6a-102">master ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) ms:contentKeyID: 48544304 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="07e6a-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="07e6a-103"><<<<<<< HEAD</span></span>
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="07e6a-104">Description-, HelpContext-, HelpFile-, NativeError-, Number-, Source- und SQLState-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="07e6a-104">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB)</span></span>
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="07e6a-105">Eigenschaften Description, HelpContext, HelpFile, NativeError, Anzahl, Source- und SQLState (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="07e6a-105">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="07e6a-106">master</span><span class="sxs-lookup"><span data-stu-id="07e6a-106">master</span></span>


<span data-ttu-id="07e6a-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07e6a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07e6a-108">Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md) und [SQLState](sqlstate-property-ado.md) des resultierenden [Error](error-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="07e6a-108">This example triggers an error, traps it, and displays the [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md), and [SQLState](sqlstate-property-ado.md) properties of the resulting [Error](error-object-ado.md) object.</span></span>

```vb
    'BeginDescriptionVB
    Public Sub Main()
    
        Dim Cnxn As ADODB.Connection
        Dim Err As ADODB.Error
        Dim strError As String
        
        On Error GoTo ErrorHandler
        
        ' Intentionally trigger an error
        Set Cnxn = New ADODB.Connection
        Cnxn.Open "nothing"
        
        Set Cnxn = Nothing
        Exit Sub
    
    ErrorHandler:
    
        ' Enumerate Errors collection and display
        ' properties of each Error object
        For Each Err In Cnxn.Errors
            strError = "Error #" & Err.Number & vbCr & _
                "   " & Err.Description & vbCr & _
                "   (Source: " & Err.Source & ")" & vbCr & _
                "   (SQL State: " & Err.SQLState & ")" & vbCr & _
                "   (NativeError: " & Err.NativeError & ")" & vbCr
            If Err.HelpFile = "" Then
                strError = strError & "   No Help file available"
            Else
                strError = strError & _
                   "   (HelpFile: " & Err.HelpFile & ")" & vbCr & _
                   "   (HelpContext: " & Err.HelpContext & ")" & _
                   vbCr & vbCr
            End If
             
            Debug.Print strError
        Next
    
        Resume Next
    End Sub
    'EndDescriptionVB
```
