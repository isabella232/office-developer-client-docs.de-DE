---
title: AffectEnum (Access PC-Datenbank-Referenz)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720583"
---
# <a name="affectenum"></a><span data-ttu-id="1a756-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="1a756-102">AffectEnum</span></span>

<span data-ttu-id="1a756-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a756-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a756-104">Gibt an, welche Datensätze von einer Operation betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="1a756-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a756-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a756-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1a756-106">Wert</span><span class="sxs-lookup"><span data-stu-id="1a756-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1a756-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a756-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a756-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="1a756-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="1a756-109">3</span><span class="sxs-lookup"><span data-stu-id="1a756-109">3</span></span></p></td>
<td><p><span data-ttu-id="1a756-110">Wenn Sie nicht, dass ein <a href="filter-property-ado.md">Filter</a> für das <strong>Recordset-Objekt</strong>angewendet wird, wirkt sich auf alle Datensätze.</span><span class="sxs-lookup"><span data-stu-id="1a756-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="1a756-111">Wenn die <strong>Filter</strong> -Eigenschaft auf ein zeichenfolgenkriterium festgelegt ist (wie &quot;Author = 'Smith'&quot;), der Vorgang wirkt sich auf die sichtbaren Datensätze im aktuellen Kapitel.</span><span class="sxs-lookup"><span data-stu-id="1a756-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="1a756-112">Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wirkt sich die Operation alle Zeilen des <strong>Recordset-Objekts</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a756-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="1a756-113"><strong>Hinweis</strong>: AdAffectAll ist im Objektbrowser von Visual Basic ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="1a756-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a756-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="1a756-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="1a756-115">4</span><span class="sxs-lookup"><span data-stu-id="1a756-115">4</span></span></p></td>
<td><p><span data-ttu-id="1a756-116">Wirkt sich auf alle Datensätze in allen gleichgeordneten Kapiteln des <strong>Recordset-Objekts</strong>, einschließlich derjenigen, die über keinen der <strong>Filter</strong> , die momentan angewendet ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="1a756-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a756-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="1a756-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="1a756-118">1</span><span class="sxs-lookup"><span data-stu-id="1a756-118">1</span></span></p></td>
<td><p><span data-ttu-id="1a756-119">Wirkt sich lediglich auf den aktuellen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="1a756-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a756-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="1a756-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="1a756-121">2</span><span class="sxs-lookup"><span data-stu-id="1a756-121">2</span></span></p></td>
<td><p><span data-ttu-id="1a756-122">Wirkt sich auf nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a> -Eigenschaft zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1a756-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="1a756-123">Sie müssen die <strong>Filter</strong> -Eigenschaft auf ein <strong>FilterGroupEnum</strong> -Wert oder ein Array von <strong>Lesezeichen</strong> verwenden Sie diese Option festlegen.</span><span class="sxs-lookup"><span data-stu-id="1a756-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1a756-124">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="1a756-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="1a756-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1a756-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a756-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a756-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a756-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="1a756-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a756-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="1a756-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a756-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="1a756-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a756-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="1a756-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

