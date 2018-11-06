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
ms.openlocfilehash: a651e017b77e01a3fc6e810f58c00c94ece123ad
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997770"
---
# <a name="querydefreturnsrecords-property-dao"></a><span data-ttu-id="9abda-102">QueryDef.ReturnsRecords-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="9abda-102">QueryDef.ReturnsRecords property (DAO)</span></span>

<span data-ttu-id="9abda-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9abda-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9abda-104">Gibt einen Wert zurück, der angibt, ob eine SQL Pass-Through-Abfrage an eine externe Datenbank Datensätze zurückgibt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="9abda-104">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9abda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9abda-105">Syntax</span></span>

<span data-ttu-id="9abda-106">*Ausdruck* . ReturnsRecords</span><span class="sxs-lookup"><span data-stu-id="9abda-106">*expression* .ReturnsRecords</span></span>

<span data-ttu-id="9abda-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9abda-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9abda-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9abda-108">Remarks</span></span>

<span data-ttu-id="9abda-p101">Nicht alle SQL Pass-Through-Abfragen an externe Datenbanken geben Datensätze zurück. Eine SQL UPDATE-Anweisung aktualisiert z. B. Datensätze, ohne Datensätze zurückzugeben, während eine SQL SELECT-Anweisung Datensätze zurückgibt. Wenn die Abfrage Datensätze zurückgibt, legen Sie für die **ReturnsRecords**-Eigenschaft **True** fest. Wenn die Abfrage keine Datensätze zurückgibt, legen Sie für die **ReturnsRecords**-Eigenschaft **False** fest.</span><span class="sxs-lookup"><span data-stu-id="9abda-p101">Not all SQL pass-through queries to external databases return records. For example, an SQL UPDATE statement updates records without returning records, while an SQL SELECT statement does return records. If the query returns records, set the **ReturnsRecords** property to **True**; if the query doesn't return records, set the **ReturnsRecords** property to **False**.</span></span>

> [!NOTE]
> <span data-ttu-id="9abda-112">[!HINWEIS] Vor dem Festlegen der [ReturnsRecords](querydef-connect-property-dao.md)-Eigenschaft müssen Sie die \*\*\*\*Connect\*\*\*\* -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="9abda-112">You must set the **[Connect](querydef-connect-property-dao.md)** property before you set the **ReturnsRecords** property.</span></span>

## <a name="example"></a><span data-ttu-id="9abda-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9abda-113">Example</span></span>

<span data-ttu-id="9abda-p102">In diesem Beispiel werden die Eigenschaften **Connect** und **ReturnsRecords** verwendet, um die 5 stärksten Buchtitel aus einer Microsoft SQL Server-Datenbank basierend auf den Verkaufszahlen eines Jahres auszuwählen. Bei einer genauen Übereinstimmung der Verkaufszahlen wird in diesem Beispiel die Größe der Liste erweitert, die die Ergebnisse der Abfrage anzeigt, und eine entsprechende Meldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9abda-p102">This example uses the **Connect** and **ReturnsRecords** properties to select the top five book titles from a Microsoft SQL Server database based on year-to-date sales amounts. In the event of an exact match in sales amounts, the example increases the size of the list displaying the results of the query and prints a message explaining why this occurred.</span></span>

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

<span data-ttu-id="9abda-116">In diesem Beispiel wird mit der Eigenschaft **ReturnsRecords** und der benutzerdefinierten Eigenschaft **LogMessages** eine Pass-Through-Abfrage erstellt, die Daten und alle vom Remoteserver erstellten Meldungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9abda-116">This example uses the **ReturnsRecords** property and the custom **LogMessages** property to create a pass-through query that will return data and any messages generated by the remote server.</span></span>

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

