---
title: QueryDef.ReturnsRecords-Eigenschaft (DAO)
TOCTitle: ReturnsRecords Property
ms:assetid: 3d1e538b-4d60-588f-4a20-89f1e2b434e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192701(v=office.15)
ms:contentKeyID: 48544334
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053005
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: bf0655deb2f145dd46483bfd8dc8d55fbec12584
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621997"
---
# <a name="querydefreturnsrecords-property-dao"></a>QueryDef.ReturnsRecords-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob eine SQL Pass-Through-Abfrage an eine externe Datenbank Datensätze zurückgibt (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . GibtRecords zurück

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Nicht alle SQL Pass-Through-Abfragen an externe Datenbanken geben Datensätze zurück. Eine SQL UPDATE-Anweisung aktualisiert z. B. Datensätze, ohne Datensätze zurückzugeben, während eine SQL SELECT-Anweisung Datensätze zurückgibt. Wenn die Abfrage Datensätze zurückgibt, legen Sie für die **ReturnsRecords**-Eigenschaft **True** fest. Wenn die Abfrage keine Datensätze zurückgibt, legen Sie für die **ReturnsRecords**-Eigenschaft **False** fest.

> [!NOTE]
> Sie müssen die **[Verbinden-Eigenschaft](querydef-connect-property-dao.md)** festlegen, bevor Sie die **ReturnsRecords-Eigenschaft** festlegen.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Eigenschaften **Connect** und **ReturnsRecords** verwendet, um die 5 stärksten Buchtitel aus einer Microsoft SQL Server-Datenbank basierend auf den Verkaufszahlen eines Jahres auszuwählen. Bei einer genauen Übereinstimmung der Verkaufszahlen wird in diesem Beispiel die Größe der Liste erweitert, die die Ergebnisse der Abfrage anzeigt, und eine entsprechende Meldung angezeigt.

```vb 
Sub ClientServerX1() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTopFive As Recordset 
 Dim strMessage As String 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("AllTitles") 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles " & _ 
 "ORDER BY ytd_sales DESC" 
 qdfPassThrough.ReturnsRecords = True 
 
 ' Create a temporary QueryDef object to retrieve 
 ' data from the pass-through query. 
 Set qdfLocal = dbsCurrent.CreateQueryDef("") 
 qdfLocal.SQL = "SELECT TOP 5 title FROM AllTitles" 
 
 Set rstTopFive = qdfLocal.OpenRecordset() 
 
 ' Display results of queries. 
 With rstTopFive 
 strMessage = _ 
 "Our top 5 best-selling books are:" & vbCr 
 
 Do While Not .EOF 
 strMessage = strMessage & " " & !Title & _ 
 vbCr 
 .MoveNext 
 Loop 
 
 If .RecordCount > 5 Then 
 strMessage = strMessage & _ 
 "(There was a tie, resulting in " & _ 
 vbCr & .RecordCount & _ 
 " books in the list.)" 
 End If 
 
 MsgBox strMessage 
 .Close 
 End With 
 
 ' Delete new pass-through query because this is a 
 ' demonstration. 
 dbsCurrent.QueryDefs.Delete "AllTitles" 
 dbsCurrent.Close 
 
```

<br/>

In diesem Beispiel wird mit der Eigenschaft **ReturnsRecords** und der benutzerdefinierten Eigenschaft **LogMessages** eine Pass-Through-Abfrage erstellt, die Daten und alle vom Remoteserver erstellten Meldungen zurückgibt.

```vb 
Sub LogMessagesX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsCurrent As Database 
 Dim qdfTemp As QueryDef 
 Dim prpNew As Property 
 Dim rstTemp As Recordset 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 Set dbsCurrent = wrkAcc.OpenDatabase("DB1.mdb") 
 
 ' Create a QueryDef that will log any messages from the 
 ' server in temporary tables. 
 Set qdfTemp = dbsCurrent.CreateQueryDef("NewQueryDef") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfTemp.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfTemp.SQL = "SELECT * FROM stores" 
 qdfTemp.ReturnsRecords = True 
 Set prpNew = qdfTemp.CreateProperty("LogMessages", _ 
 dbBoolean, True) 
 qdfTemp.Properties.Append prpNew 
 
 ' Execute query and display results. 
 Set rstTemp = qdfTemp.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfTemp.Name 
 dbsCurrent.Close 
 wrkAcc.Close 
 
End Sub 
 
```

