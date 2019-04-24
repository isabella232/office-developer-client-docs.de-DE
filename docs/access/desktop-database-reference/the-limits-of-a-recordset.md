---
title: Grenzen eines Recordset-Objekts
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d0da48080b64e43cc39b9567275e1a8755a8881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314112"
---
# <a name="limits-of-a-recordset"></a><span data-ttu-id="3a5fa-102">Die Einschränkungen eines Recordsets</span><span class="sxs-lookup"><span data-stu-id="3a5fa-102">Limits of a Recordset</span></span>


<span data-ttu-id="3a5fa-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a5fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a5fa-p101">Bestimmen Sie mithilfe der Eigenschaften **BOF** und **EOF**, ob ein **Recordset**-Objekt Datensätze enthält oder ob Sie beim Navigieren in den Datensätzen die Grenzen eines **Recordset**-Objekts überschritten haben. Stellen Sie sich **BOF** und **EOF** als "Phantomdatensätze" vor, die am Anfang und am Ende des **Recordset**-Objekts positioniert sind. Basierend auf dem **Recordset**-Beispielobjekt unter [Untersuchen von Daten](chapter-3-examining-data.md) würde dies nun wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="3a5fa-p101">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record. Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**. Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a5fa-107">ProductID</span><span class="sxs-lookup"><span data-stu-id="3a5fa-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="3a5fa-108">ProductName</span><span class="sxs-lookup"><span data-stu-id="3a5fa-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="3a5fa-109">UnitPrice</span><span class="sxs-lookup"><span data-stu-id="3a5fa-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a5fa-110">BOF</span><span class="sxs-lookup"><span data-stu-id="3a5fa-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a5fa-111">7</span><span class="sxs-lookup"><span data-stu-id="3a5fa-111">7</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-112">Uncle Bob's Organic Dried Pears</span><span class="sxs-lookup"><span data-stu-id="3a5fa-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-113">30,0000</span><span class="sxs-lookup"><span data-stu-id="3a5fa-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a5fa-114">14</span><span class="sxs-lookup"><span data-stu-id="3a5fa-114">14</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-115">Tofu</span><span class="sxs-lookup"><span data-stu-id="3a5fa-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-116">23,2500</span><span class="sxs-lookup"><span data-stu-id="3a5fa-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a5fa-117">28</span><span class="sxs-lookup"><span data-stu-id="3a5fa-117">28</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-118">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="3a5fa-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-119">45,6000</span><span class="sxs-lookup"><span data-stu-id="3a5fa-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a5fa-120">51</span><span class="sxs-lookup"><span data-stu-id="3a5fa-120">51</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-121">Manjimup Dried Apples</span><span class="sxs-lookup"><span data-stu-id="3a5fa-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-122">53,0000</span><span class="sxs-lookup"><span data-stu-id="3a5fa-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a5fa-123">74</span><span class="sxs-lookup"><span data-stu-id="3a5fa-123">74</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-124">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="3a5fa-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="3a5fa-125">10,0000</span><span class="sxs-lookup"><span data-stu-id="3a5fa-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a5fa-126">EOF</span><span class="sxs-lookup"><span data-stu-id="3a5fa-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a5fa-127">Die **BOF**-Eigenschaft gibt **True** (-1) zurück, falls sich die aktuelle Datensatzposition vor dem ersten Datensatz befindet, und **False** (0), falls sich die aktuelle Datensatzposition im oder nach dem ersten Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="3a5fa-128">Die **EOF**-Eigenschaft gibt **True** zurück, falls sich die aktuelle Datensatzposition nach dem letzten Datensatz befindet, und **False**, falls sich die aktuelle Datensatzposition im oder vor dem letzten Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="3a5fa-129">Wenn die **BOF** - oder die **EOF** -Eigenschaft **True** ist, gibt es wie im folgenden Code veranschaulicht keinen aktuellen Datensatz:</span><span class="sxs-lookup"><span data-stu-id="3a5fa-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="3a5fa-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="3a5fa-131">-1 wird für dynamische Cursor (**CursorType** = **adOpenDynamic**) zurückgegeben, und 0 wird für andere Cursor zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="3a5fa-132">Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz, und die Eigenschaften **BOF** und **EOF** sind **False**.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="3a5fa-p103">Wenn Sie den letzten verbleibenden Datensatz im **Recordset** -Objekt löschen, befindet sich der Cursor in einem unbestimmten Status. Die Eigenschaften **BOF** und **EOF** bleiben je nach Anbieter **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="3a5fa-p103">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state. The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

