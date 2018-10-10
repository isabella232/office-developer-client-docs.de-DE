---
title: 'Kapitel 3: Untersuchen von Daten'
TOCTitle: 'Chapter 3: Examining Data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 481fbc3bc39f184aeefe6738ac8d2a80fcd1d93f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474285"
---
# <a name="chapter-3-examining-data"></a>Kapitel 3: Untersuchen von Daten


**Betrifft**: Access 2013 | Office 2013

In Kapitel 2 wird erläutert, wie Sie Daten aus einer Datenquelle als **Recordset** -Objekt abrufen können. Dieses Kapitel beschreibt das **Recordset** -Objekt detaillierter und erklärt, wie Sie das **Recordset** -Objekt und seine Daten in einer Schleife durchlaufen.

**Recordset** -Objekte haben Methoden und Eigenschaften, die es erleichtern, sie zu durchlaufen und ihre Inhalte zu überprüfen. Abhängig von der vom Anbieter unterstützten Funktionalität sind einige **Recordset** -Methoden oder -Eigenschaften möglicherweise nicht verfügbar. Im folgenden Codebeispiel mit einem von der Northwind-Beispieldatenbank auf Microsoft SQL Server 2000 zurückgegebenen **Recordset** -Objekt wird die Verwendung des **Recordset** -Objekts genauer beschrieben:

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

Diese SQL-Abfrage gibt ein **Recordset** -Objekt mit fünf Zeilen (Datensätzen) und drei Spalten (Feldern) zurück. Die Werte für die einzelnen Zeilen sind in der folgenden Tabelle aufgelistet.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>FELD 0<br />
Name = ProductID</p></th>
<th><p>FELD 1<br />
Name = ProductName</p></th>
<th><p>FELD 2<br />
Name = UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="even">
<td><p>14</p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Manjimup Dried Apples</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10.0000</p></td>
</tr>
</tbody>
</table>


Der Abschnitt beschreibt, wie Sie die aktuelle Position des Cursors in diesem **Recordset** -Beispielobjekt finden.
