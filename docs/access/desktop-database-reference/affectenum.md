---
title: AffectEnum (Access Desktop Database Reference)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297200"
---
# <a name="affectenum"></a><span data-ttu-id="6886c-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="6886c-102">AffectEnum</span></span>

<span data-ttu-id="6886c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6886c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6886c-104">Gibt an, welche Datensätze von einer Operation betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="6886c-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6886c-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="6886c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6886c-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6886c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6886c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6886c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6886c-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="6886c-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="6886c-109">3</span><span class="sxs-lookup"><span data-stu-id="6886c-109">3</span></span></p></td>
<td><p><span data-ttu-id="6886c-110">Wenn kein <a href="filter-property-ado.md">Filter</a> auf das <strong>Recordset</strong>angewendet wird, wirkt sich dies auf alle Datensätze aus.</span><span class="sxs-lookup"><span data-stu-id="6886c-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="6886c-111">Wenn die <strong>Filter</strong> -Eigenschaft auf eine Zeichenfolge (beispielsweise &quot;Author = ' Smith '&quot;) festgelegt ist, wirkt sich die Operation auf sichtbare Datensätze im aktuellen Kapitel aus.</span><span class="sxs-lookup"><span data-stu-id="6886c-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="6886c-112">Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wirkt sich die Operation auf alle Zeilen des <strong>Recordset-Objekts</strong>aus.</span><span class="sxs-lookup"><span data-stu-id="6886c-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="6886c-113"><strong>Hinweis</strong>: adAffectAll ist im Visual Basic-Objekt Browser ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="6886c-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6886c-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="6886c-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="6886c-115">4</span><span class="sxs-lookup"><span data-stu-id="6886c-115">4</span></span></p></td>
<td><p><span data-ttu-id="6886c-116">Wirkt sich auf alle Datensätze in allen nebengeordneten Kapiteln des <strong>Recordset-Objekts</strong>aus, einschließlich derer, die nicht über einen <strong>Filter</strong> angezeigt werden, der derzeit angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6886c-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6886c-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="6886c-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="6886c-118">1</span><span class="sxs-lookup"><span data-stu-id="6886c-118">1</span></span></p></td>
<td><p><span data-ttu-id="6886c-119">Wirkt sich lediglich auf den aktuellen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="6886c-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6886c-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="6886c-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="6886c-121">2</span><span class="sxs-lookup"><span data-stu-id="6886c-121">2</span></span></p></td>
<td><p><span data-ttu-id="6886c-122">Betrifft nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a>-Eigenschaft erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6886c-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="6886c-123">Sie müssen die <strong>Filter</strong> -Eigenschaft auf einen <strong>FilterGroupEnum</strong> -Wert oder ein Array von <strong>Textmarken</strong> festlegen, um diese Option zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6886c-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6886c-124">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="6886c-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="6886c-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6886c-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6886c-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="6886c-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6886c-127">AdoEnums. affect. ALL</span><span class="sxs-lookup"><span data-stu-id="6886c-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6886c-128">AdoEnums. affect. allCHAPTERs</span><span class="sxs-lookup"><span data-stu-id="6886c-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6886c-129">AdoEnums. affect. CURRENT</span><span class="sxs-lookup"><span data-stu-id="6886c-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6886c-130">AdoEnums. affect. GROUP</span><span class="sxs-lookup"><span data-stu-id="6886c-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

