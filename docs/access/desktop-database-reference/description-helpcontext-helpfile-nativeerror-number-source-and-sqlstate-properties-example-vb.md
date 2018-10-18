---
<<<<<<< HEAD-Titel: Description, HelpContext, HelpFile Eigenschaften Beispiel) (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Anzahl, Source- und SQLState Eigenschaften Beispiel) (VB) === Titel: Beschreibung, HelpContext-und HelpFile-Eigenschaft (Beispiel) (VB) TOCTitle: Eigenschaften Description, HelpContext, HelpFile, NativeError, Anzahl, Source- und SQLState (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) Ms:contentKeyID: 48544304 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a>Description-, HelpContext-, HelpFile-, NativeError-, Number-, Source- und SQLState-Eigenschaft (Beispiel) (VB)
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a>Eigenschaften Description, HelpContext, HelpFile, NativeError, Anzahl, Source- und SQLState (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md) und [SQLState](sqlstate-property-ado.md) des resultierenden [Error](error-object-ado.md)-Objekts an.

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
