---
<<<<<<< HEAD-Titel: Count-Eigenschaft Beispiel) (VB) TOCTitle: Count-Eigenschaft Beispiel) (VB) === Titel: Count-Eigenschaft (Beispiel) (VB) TOCTitle: Count-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 9fea66f7-a4ed-fe2e-c199-672b910fef47 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249734(v=office.15) Ms:contentKeyID: 48546695 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="count-property-example-vb"></a>Count Property Example (VB)
=======
# <a name="count-property-example-vb"></a>Count-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel veranschaulicht die [Count](count-property-ado.md) -Eigenschaft mit zwei Sammlungen in der ***Employee*** -Datenbank. Die Eigenschaft ruft die Anzahl der Objekte in der Auflistung ab und legt den oberen Grenzwert für Schleifen, die diese Auflistungen aufgezählt werden. Eine andere Möglichkeit, diese Auflistungen aufgezählt werden ohne Verwendung der **Count** -Eigenschaft wäre Anweisungen verwenden.

```vb 
 
'BeginCountVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLEmployees As String 
 Dim strCnxn As String 
 
 Dim intLoop As Integer 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employee table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "Employees" 
 'rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 rstEmployees.Open strSQLEmployees, Cnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines opening the recordset are identical as 
 'the default values for CursorType and LockType arguments match those specified 
 
 ' Print information about Fields collection 
 Debug.Print rstEmployees.Fields.Count & " Fields in Employee" 
 
 For intLoop = 0 To rstEmployees.Fields.Count - 1 
 Debug.Print " " & rstEmployees.Fields(intLoop).Name 
 Next intLoop 
 
 ' Print information about Properties collection 
 Debug.Print rstEmployees.Properties.Count & " Properties in Employee" 
 
 For intLoop = 0 To rstEmployees.Properties.Count - 1 
 Debug.Print " " & rstEmployees.Properties(intLoop).Name 
 Next intLoop 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndCountVB 
```
