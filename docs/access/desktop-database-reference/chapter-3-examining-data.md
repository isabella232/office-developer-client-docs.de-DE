---
title: 'Kapitel 3: Untersuchen von Daten'
TOCTitle: 'Chapter 3: Examining Data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af923408c07ac0437bde0aa52707b70c1a002ffc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25859895"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="e8ef4-102">Kapitel 3: Untersuchen von Daten</span><span class="sxs-lookup"><span data-stu-id="e8ef4-102">Chapter 3: Examining Data</span></span>


<span data-ttu-id="e8ef4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8ef4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8ef4-p101">In Kapitel 2 wird erläutert, wie Sie Daten aus einer Datenquelle als **Recordset** -Objekt abrufen können. Dieses Kapitel beschreibt das **Recordset** -Objekt detaillierter und erklärt, wie Sie das **Recordset** -Objekt und seine Daten in einer Schleife durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e8ef4-p101">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object. This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="e8ef4-p102">**Recordset** -Objekte haben Methoden und Eigenschaften, die es erleichtern, sie zu durchlaufen und ihre Inhalte zu überprüfen. Abhängig von der vom Anbieter unterstützten Funktionalität sind einige **Recordset** -Methoden oder -Eigenschaften möglicherweise nicht verfügbar. Im folgenden Codebeispiel mit einem von der Northwind-Beispieldatenbank auf Microsoft SQL Server 2000 zurückgegebenen **Recordset** -Objekt wird die Verwendung des **Recordset** -Objekts genauer beschrieben:</span><span class="sxs-lookup"><span data-stu-id="e8ef4-p102">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents. Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available. To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

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

<span data-ttu-id="e8ef4-p103">Diese SQL-Abfrage gibt ein **Recordset** -Objekt mit fünf Zeilen (Datensätzen) und drei Spalten (Feldern) zurück. Die Werte für die einzelnen Zeilen sind in der folgenden Tabelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e8ef4-p103">This SQL query returns a **Recordset** with five rows (records) and three columns (fields). The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8ef4-111">FELD 0</span><span class="sxs-lookup"><span data-stu-id="e8ef4-111">FIELD 0</span></span><br />
<span data-ttu-id="e8ef4-112">Name = ProductID</span><span class="sxs-lookup"><span data-stu-id="e8ef4-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="e8ef4-113">FELD 1</span><span class="sxs-lookup"><span data-stu-id="e8ef4-113">FIELD 1</span></span><br />
<span data-ttu-id="e8ef4-114">Name = ProductName</span><span class="sxs-lookup"><span data-stu-id="e8ef4-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="e8ef4-115">FELD 2</span><span class="sxs-lookup"><span data-stu-id="e8ef4-115">FIELD 2</span></span><br />
<span data-ttu-id="e8ef4-116">Name = UnitPrice</span><span class="sxs-lookup"><span data-stu-id="e8ef4-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8ef4-117">7</span><span class="sxs-lookup"><span data-stu-id="e8ef4-117">7</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-118">Uncle Bob's Organic Dried Pears</span><span class="sxs-lookup"><span data-stu-id="e8ef4-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="e8ef4-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ef4-120">14</span><span class="sxs-lookup"><span data-stu-id="e8ef4-120">14</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-121">Tofu</span><span class="sxs-lookup"><span data-stu-id="e8ef4-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="e8ef4-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ef4-123">28</span><span class="sxs-lookup"><span data-stu-id="e8ef4-123">28</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-124">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="e8ef4-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="e8ef4-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ef4-126">51</span><span class="sxs-lookup"><span data-stu-id="e8ef4-126">51</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-127">Manjimup Dried Apples</span><span class="sxs-lookup"><span data-stu-id="e8ef4-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="e8ef4-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ef4-129">74</span><span class="sxs-lookup"><span data-stu-id="e8ef4-129">74</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-130">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="e8ef4-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="e8ef4-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="e8ef4-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8ef4-132">Im nächste Abschnitt wird erläutert, wie die aktuelle Position des Cursors in diesem Beispiel **Recordset**gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8ef4-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="e8ef4-133">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="e8ef4-133">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="e8ef4-134">Locating the Current Record (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8ef4-134">Locating the Current Record (ADO)</span></span>](locating-the-current-record.md)

  - [<span data-ttu-id="e8ef4-135">Navigating Through the Data (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8ef4-135">Navigating Through the Data (ADO)</span></span>](navigating-through-the-data.md)

  - [<span data-ttu-id="e8ef4-136">Understanding Recordset Structure (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8ef4-136">Understanding Recordset Structure (ADO)</span></span>](understanding-recordset-structure.md)