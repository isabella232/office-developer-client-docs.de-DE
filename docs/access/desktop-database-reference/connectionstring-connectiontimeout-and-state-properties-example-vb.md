---
<<<<<<< HEAD-Titel: ConnectionString-, ConnectionTimeout- und State Eigenschaften Beispiel) (VB) TOCTitle: ConnectionString-, ConnectionTimeout- und State Eigenschaften Beispiel) (VB) === Titel: ConnectionString-, ConnectionTimeout-, und State-Eigenschaft (Beispiel) (VB) TOCTitle: ConnectionString-, ConnectionTimeout- und State-Eigenschaften (Beispiel) (VB)
>>>>>>> Master Ms:assetid: abdd0262-8647-d545-60e0-13f99337df06 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249796(v=office.15) Ms:contentKeyID: 48546984 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vb"></a>ConnectionString-, ConnectionTimeout- und State-Eigenschaft (Beispiel) (VB)
=======
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vb"></a>ConnectionString-, ConnectionTimeout- und State-Eigenschaften (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel veranschaulicht verschiedene Verwendungsmöglichkeiten der ConnectionString-Eigenschaft, um ein Connection-Objekt zu öffnen. Außerdem wird mithilfe der ConnectionTimeout-Eigenschaft ein Verbindungstimeout festgelegt, und mithilfe der State-Eigenschaft wird der Status der Verbindungen überprüft. Zum Ausführen dieser Prozedur ist die GetState-Funktion erforderlich.

```vb 
 
'BeginConnectionStringVB 
 
 'To integrate this code replace 
 'the database, DSN or Data Source values 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim Cnxn3 As ADODB.Connection 
 Dim Cnxn4 As ADODB.Connection 
 
 ' Open a connection without using a Data Source Name (DSN) 
 Set Cnxn1 = New ADODB.Connection 
 Cnxn1.ConnectionString = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn1.Open 
 MsgBox "Cnxn1 state: " & GetState(Cnxn1.State) 
 
 ' Open a connection using a DSN and ODBC tags 
 ' It is assumed that you have create DSN 'Pubs' with a user name as 
 ' 'MyUserId' and password as 'MyPassword'. 
 Set Cnxn2 = New ADODB.Connection 
 Cnxn2.ConnectionString = "Data Source='Pubs';" & _ 
 "User ID='MyUserId';Password='MyPassword';" 
 Cnxn2.ConnectionTimeout = 30 
 Cnxn2.Open 
 MsgBox "Cnxn2 state: " & GetState(Cnxn2.State) 
 
 ' Open a connection using a DSN and OLE DB tags 
 ' It is assumed that you have create DSN 'Pubs1' with windows authentication. 
 Set Cnxn3 = New ADODB.Connection 
 Cnxn3.ConnectionString = "Data Source='Pubs1';" 
 Cnxn3.Open 
 MsgBox "Cnxn2 state: " & GetState(Cnxn3.State) 
 
 ' Open a connection using a DSN and individual 
 ' arguments instead of a connection string 
 ' It is assumed that you have create DSN 'Pubs' with a user name as 
 ' 'MyUserId' and password as 'MyPassword'. 
 Set Cnxn4 = New ADODB.Connection 
 Cnxn4.Open "Pubs", "MyUserId", "MyPassword" 
 MsgBox "Cnxn4 state: " & GetState(Cnxn4.State) 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Cnxn3.Close 
 Cnxn4.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Set Cnxn3 = Nothing 
 Set Cnxn4 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Not Cnxn3 Is Nothing Then 
 If Cnxn3.State = adStateOpen Then Cnxn3.Close 
 End If 
 Set Cnxn3 = Nothing 
 
 If Not Cnxn4 Is Nothing Then 
 If Cnxn4.State = adStateOpen Then Cnxn4.Close 
 End If 
 Set Cnxn4 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
 
Public Function GetState(intState As Integer) As String 
 
 Select Case intState 
 Case adStateClosed 
 GetState = "adStateClosed" 
 Case adStateOpen 
 GetState = "adStateOpen" 
 End Select 
 
End Function 
'EndConnectionStringVB 
```

