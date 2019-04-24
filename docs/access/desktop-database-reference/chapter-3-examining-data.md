---
title: 'Kapitel 3: Untersuchen von Daten'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcf837a02c40d11fecfa56b8aa34ac80a848411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296458"
---
# <a name="chapter-3-examining-data"></a>Kapitel 3: Untersuchen von Daten

**Gilt für**: Access 2013, Office 2013

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

<br/>

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
Name = Einzelpreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>7</p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30,0000</p></td>
</tr>
<tr class="even">
<td><p>14</p></td>
<td><p>Tofu</p></td>
<td><p>23,2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45,6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Manjimup Dried Apples</p></td>
<td><p>53,0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10,0000</p></td>
</tr>
</tbody>
</table>


Im nächsten Abschnitt wird erläutert, wie Sie die aktuelle Position des Cursors in diesem **Recordset**-Beispiel finden.

In diesem Kapitel werden die folgenden Themen behandelt:

- [Suchen des aktuellen Datensatzes (ADO)](locating-the-current-record.md)
- [Navigieren durch die Daten (ADO)](navigating-through-the-data.md)
- [Grundlegendes zur Recordset-Struktur (ADO)](understanding-recordset-structure.md)
