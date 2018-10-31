---
title: AffectEnum (Access PC-Datenbank-Referenz)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9e1bd4d86e6e269c9363daca0ffa7b8df6303326
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863668"
---
# <a name="affectenum"></a><span data-ttu-id="34d4d-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="34d4d-102">AffectEnum</span></span>

<span data-ttu-id="34d4d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34d4d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34d4d-104">Gibt an, welche Datensätze von einer Operation betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="34d4d-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34d4d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="34d4d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="34d4d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="34d4d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="34d4d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34d4d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34d4d-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="34d4d-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="34d4d-109">3</span><span class="sxs-lookup"><span data-stu-id="34d4d-109">3</span></span></p></td>
<td><p><span data-ttu-id="34d4d-110">Wenn Sie nicht, dass ein <a href="filter-property-ado.md">Filter</a> für das <strong>Recordset-Objekt</strong>angewendet wird, wirkt sich auf alle Datensätze.</span><span class="sxs-lookup"><span data-stu-id="34d4d-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="34d4d-111">Wenn die <strong>Filter</strong> -Eigenschaft auf ein zeichenfolgenkriterium festgelegt ist (wie &quot;Author = 'Smith'&quot;), der Vorgang wirkt sich auf die sichtbaren Datensätze im aktuellen Kapitel.</span><span class="sxs-lookup"><span data-stu-id="34d4d-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="34d4d-112">Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wirkt sich die Operation alle Zeilen des <strong>Recordset-Objekts</strong>.</span><span class="sxs-lookup"><span data-stu-id="34d4d-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>
<p><span data-ttu-id="34d4d-113"><strong>Hinweis</strong>: AdAffectAll ist im Objektbrowser von Visual Basic ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="34d4d-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d4d-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="34d4d-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="34d4d-115">4</span><span class="sxs-lookup"><span data-stu-id="34d4d-115">4</span></span></p></td>
<td><p><span data-ttu-id="34d4d-116">Wirkt sich auf alle Datensätze in allen gleichgeordneten Kapiteln des <strong>Recordset-Objekts</strong>, einschließlich derjenigen, die über keinen der <strong>Filter</strong> , die momentan angewendet ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="34d4d-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34d4d-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="34d4d-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="34d4d-118">1</span><span class="sxs-lookup"><span data-stu-id="34d4d-118">1</span></span></p></td>
<td><p><span data-ttu-id="34d4d-119">Wirkt sich lediglich auf den aktuellen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="34d4d-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d4d-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="34d4d-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="34d4d-121">2</span><span class="sxs-lookup"><span data-stu-id="34d4d-121">2</span></span></p></td>
<td><p><span data-ttu-id="34d4d-122">Wirkt sich auf nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a> -Eigenschaft zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="34d4d-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="34d4d-123">Sie müssen die <strong>Filter</strong> -Eigenschaft auf ein <strong>FilterGroupEnum</strong> -Wert oder ein Array von <strong>Lesezeichen</strong> verwenden Sie diese Option festlegen.</span><span class="sxs-lookup"><span data-stu-id="34d4d-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="34d4d-124">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="34d4d-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="34d4d-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="34d4d-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34d4d-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="34d4d-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34d4d-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="34d4d-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d4d-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="34d4d-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34d4d-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="34d4d-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34d4d-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="34d4d-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

