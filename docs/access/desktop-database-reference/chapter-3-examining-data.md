---
title: 'Kapitel 3: Untersuchen von Daten'
TOCTitle: 'Chapter 3: Examining Data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5542b465cc6fc31949f2ceb5ed8bda408b1e653
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875931"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="022e1-102">Kapitel 3: Untersuchen von Daten</span><span class="sxs-lookup"><span data-stu-id="022e1-102">Chapter 3: Examining Data</span></span>


<span data-ttu-id="022e1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="022e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="022e1-p101">In Kapitel 2 wird erläutert, wie Sie Daten aus einer Datenquelle als **Recordset** -Objekt abrufen können. Dieses Kapitel beschreibt das **Recordset** -Objekt detaillierter und erklärt, wie Sie das **Recordset** -Objekt und seine Daten in einer Schleife durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="022e1-p101">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object. This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="022e1-p102">**Recordset** -Objekte haben Methoden und Eigenschaften, die es erleichtern, sie zu durchlaufen und ihre Inhalte zu überprüfen. Abhängig von der vom Anbieter unterstützten Funktionalität sind einige **Recordset** -Methoden oder -Eigenschaften möglicherweise nicht verfügbar. Im folgenden Codebeispiel mit einem von der Northwind-Beispieldatenbank auf Microsoft SQL Server 2000 zurückgegebenen **Recordset** -Objekt wird die Verwendung des **Recordset** -Objekts genauer beschrieben:</span><span class="sxs-lookup"><span data-stu-id="022e1-p102">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents. Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available. To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

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

<span data-ttu-id="022e1-p103">Diese SQL-Abfrage gibt ein **Recordset** -Objekt mit fünf Zeilen (Datensätzen) und drei Spalten (Feldern) zurück. Die Werte für die einzelnen Zeilen sind in der folgenden Tabelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="022e1-p103">This SQL query returns a **Recordset** with five rows (records) and three columns (fields). The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="022e1-111">FELD 0</span><span class="sxs-lookup"><span data-stu-id="022e1-111">FIELD 0</span></span><br />
<span data-ttu-id="022e1-112">Name = ProductID</span><span class="sxs-lookup"><span data-stu-id="022e1-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="022e1-113">FELD 1</span><span class="sxs-lookup"><span data-stu-id="022e1-113">FIELD 1</span></span><br />
<span data-ttu-id="022e1-114">Name = ProductName</span><span class="sxs-lookup"><span data-stu-id="022e1-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="022e1-115">FELD 2</span><span class="sxs-lookup"><span data-stu-id="022e1-115">FIELD 2</span></span><br />
<span data-ttu-id="022e1-116">Name = UnitPrice</span><span class="sxs-lookup"><span data-stu-id="022e1-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="022e1-117">7</span><span class="sxs-lookup"><span data-stu-id="022e1-117">7</span></span></p></td>
<td><p><span data-ttu-id="022e1-118">Uncle Bob's Organic Dried Pears</span><span class="sxs-lookup"><span data-stu-id="022e1-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="022e1-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="022e1-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022e1-120">14</span><span class="sxs-lookup"><span data-stu-id="022e1-120">14</span></span></p></td>
<td><p><span data-ttu-id="022e1-121">Tofu</span><span class="sxs-lookup"><span data-stu-id="022e1-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="022e1-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="022e1-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022e1-123">28</span><span class="sxs-lookup"><span data-stu-id="022e1-123">28</span></span></p></td>
<td><p><span data-ttu-id="022e1-124">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="022e1-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="022e1-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="022e1-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022e1-126">51</span><span class="sxs-lookup"><span data-stu-id="022e1-126">51</span></span></p></td>
<td><p><span data-ttu-id="022e1-127">Manjimup Dried Apples</span><span class="sxs-lookup"><span data-stu-id="022e1-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="022e1-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="022e1-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022e1-129">74</span><span class="sxs-lookup"><span data-stu-id="022e1-129">74</span></span></p></td>
<td><p><span data-ttu-id="022e1-130">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="022e1-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="022e1-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="022e1-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="022e1-132">Im nächste Abschnitt wird erläutert, wie die aktuelle Position des Cursors in diesem Beispiel **Recordset**gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="022e1-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="022e1-133">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="022e1-133">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="022e1-134">Locating the Current Record (ADO)</span><span class="sxs-lookup"><span data-stu-id="022e1-134">Locating the Current Record (ADO)</span></span>](locating-the-current-record.md)

  - [<span data-ttu-id="022e1-135">Navigating Through the Data (ADO)</span><span class="sxs-lookup"><span data-stu-id="022e1-135">Navigating Through the Data (ADO)</span></span>](navigating-through-the-data.md)

  - [<span data-ttu-id="022e1-136">Understanding Recordset Structure (ADO)</span><span class="sxs-lookup"><span data-stu-id="022e1-136">Understanding Recordset Structure (ADO)</span></span>](understanding-recordset-structure.md)