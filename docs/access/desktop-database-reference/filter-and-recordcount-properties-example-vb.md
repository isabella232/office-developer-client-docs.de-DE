---
title: Filter- und RecordCount-Eigenschaft (Beispiel) (VB)
TOCTitle: Filter and RecordCount properties example (VB)
ms:assetid: 3da4623e-03e7-27ac-7351-3b22415be0b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249167(v=office.15)
ms:contentKeyID: 48544354
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1d2262a3153d7168caa2e27a6eb0f0688e55ec10
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626589"
---
# <a name="filter-and-recordcount-properties-example-vb"></a>Filter- und RecordCount-Eigenschaft (Beispiel) (VB)


**Gilt für**: Access 2013, Office 2013

In diesem Beispiel wird ein **Recordset-Objekt** in der Tabelle Publishers in der **_Pubs_-Datenbank_*geöffnet. Anschließend wird die [Filter-Eigenschaft](filter-property-ado.md) verwendet, um die Anzahl sichtbarer Datensätze auf die Herausgeber in einem bestimmten Land/einer bestimmten Region zu beschränken. Die* _RecordCount-Eigenschaft** wird verwendet, um den Unterschied zwischen den gefilterten und ungefilterten Recordsets anzuzeigen.

```vb 
 
'BeginFilterVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim SQLPublishers As String 
 
 ' criteria variables 
 Dim intPublisherCount As Integer 
 Dim strCountry As String 
 Dim strMessage As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with data from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 SQLPublishers = "publishers" 
 rstPublishers.Open SQLPublishers, strCnxn, adOpenStatic, , adCmdTable 
 
 intPublisherCount = rstPublishers.RecordCount 
 
 ' get user input 
 strCountry = Trim(InputBox("Enter a country to filter on (e.g. USA):")) 
 
 If strCountry <> "" Then 
 ' open a filtered Recordset object 
 rstPublishers.Filter = "Country ='" & strCountry & "'" 
 
 If rstPublishers.RecordCount = 0 Then 
 MsgBox "No publishers from that country." 
 Else 
 ' print number of records for the original recordset 
 ' and the filtered recordset 
 strMessage = "Orders in original recordset: " & _ 
 vbCr & intPublisherCount & vbCr & _ 
 "Orders in filtered recordset (Country = '" & _ 
 strCountry & "'): " & vbCr & _ 
 rstPublishers.RecordCount 
 MsgBox strMessage 
 End If 
 End If 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndFilterVB 
```


> [!NOTE]
> [!HINWEIS] Wenn Sie wissen, welche Daten Sie auswählen möchten, ist es in der Regel effizienter, ein **Recordset** -Objekt mit einer SQL-Anweisung zu öffnen. Das folgende Beispiel zeigt, wie Sie nur ein **Recordset** -Objekt erstellen und die Daten eines bestimmten Landes/einer bestimmten Region erhalten.



```vb 
 
'BeginFilter2VB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim rstPublishers As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLPublishers As String 
 Dim strCnxn As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset with criteria from Publishers table 
 Set rstPublishers = New ADODB.Recordset 
 strSQLPublishers = "SELECT * FROM publishers WHERE Country = 'USA'" 
 rstPublishers.Open strSQLPublishers, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' print recordset 
 rstPublishers.MoveFirst 
 Do While Not rstPublishers.EOF 
 Debug.Print rstPublishers!pub_name & ", " & rstPublishers!country 
 rstPublishers.MoveNext 
 Loop 
 
 ' clean up 
 rstPublishers.Close 
 Cnxn.Close 
 Set rstPublishers = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstPublishers Is Nothing Then 
 If rstPublishers.State = adStateOpen Then rstPublishers.Close 
 End If 
 Set rstPublishers = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndFilter2VB 
```

