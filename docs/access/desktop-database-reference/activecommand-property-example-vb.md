---
title: ActiveCommand-Eigenschaft (Beispiel) (VB)
TOCTitle: ActiveCommand property example (VB)
ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15)
ms:contentKeyID: 48545999
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 46338c801bbdf1e4faaef5a3f6ff1c10d28ab544
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870002"
---
# <a name="activecommand-property-example-vb"></a>ActiveCommand-Eigenschaft (Beispiel) (VB)


**Betrifft**: Access 2013, Office 2013

Dieses Beispiel veranschaulicht die [ActiveCommand](activecommand-property-ado.md)-Eigenschaft.

Eine Unterroutine erhält ein [Recordset](recordset-object-ado.md)-Objekt, dessen **ActiveCommand** -Eigenschaft zum Anzeigen des Befehlstexts und des Parameters verwendet werden, mit denen das **Recordset** -Objekt erstellt wurde.

```vb 
 
'BeginActiveCommandVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim cmd As ADODB.Command 
 Dim rst As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 'record variables 
 Dim strPrompt As String 
 Dim strName As String 
 
 Set Cnxn = New ADODB.Connection 
 Set cmd = New ADODB.Command 
 
 strPrompt = "Enter an author's name (e.g., Ringer): " 
 strName = Trim(InputBox(strPrompt, "ActiveCommandX Example")) 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 'create SQL command string 
 cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?" 
 cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName) 
 
 Cnxn.Open strCnxn 
 cmd.ActiveConnection = Cnxn 
 
 'create the recordset by executing command string 
 Set rst = cmd.Execute(, , adCmdText) 
 'see the results 
 Call ActiveCommandXprint(rst) 
 
 ' clean up 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActiveCommandVB 
```

Die **ActiveCommandXprint** -Routine erhält nur ein **Recordset** -Objekt, sie muss jedoch den Befehlstext und den Parameter anzeigen, mit denen das **Recordset** -Objekt erstellt wurde. Dies ist möglich, weil die **ActiveCommand** -Eigenschaft des **Recordset** -Objekts das zugeordnete [Command](command-object-ado.md)-Objekt liefert.

Die [CommandText](commandtext-property-ado.md)-Eigenschaft des **Command**-Objekts liefert den parametrisierten Befehl, mit dem das **Recordset**-Objekt erstellt wurde. Die [Parameters](parameters-collection-ado.md)-Auflistung des **Command**-Objekts liefert den Wert, durch den der Parameterplatzhalter ("**?**") ersetzt wurde.

Schließlich werden die Fehlermeldung oder der Name und die ID des Autors angezeigt.

```vb 
 
'BeginActiveCommandPrintVB 
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset) 
 
 Dim strName As String 
 
 strName = rstp.ActiveCommand.Parameters.Item("LastName").Value 
 
 Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'" 
 Debug.Print "Parameter = '"; strName; "'" 
 
 If rstp.BOF = True Then 
 Debug.Print "Name = '"; strName; "', not found." 
 Else 
 Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _ 
 "', author ID = '"; rstp!au_id; "'" 
 End If 
 
 rstp.Close 
 Set rstp = Nothing 
End Sub 
'EndActiveCommandPrintVB 
```

