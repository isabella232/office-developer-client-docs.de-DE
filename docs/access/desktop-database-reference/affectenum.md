---
title: AffectEnum (Access PC-Datenbank-Referenz)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ffb2ab2abbd24a19ddc433b5fd315dd535fd2a0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473880"
---
# <a name="affectenum"></a><span data-ttu-id="eff35-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="eff35-102">AffectEnum</span></span>


<span data-ttu-id="eff35-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eff35-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eff35-104">Gibt an, welche Datensätze von einer Operation betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="eff35-104">Specifies which records are affected by an operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff35-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="eff35-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="eff35-106">Wert</span><span class="sxs-lookup"><span data-stu-id="eff35-106">Value</span></span></p></th>
<th><p><span data-ttu-id="eff35-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eff35-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff35-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="eff35-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="eff35-109">3</span><span class="sxs-lookup"><span data-stu-id="eff35-109">3</span></span></p></td>
<td><p><span data-ttu-id="eff35-110">Wenn Sie nicht, dass ein <a href="filter-property-ado.md">Filter</a> für das <strong>Recordset-Objekt</strong>angewendet wird, wirkt sich auf alle Datensätze.</span><span class="sxs-lookup"><span data-stu-id="eff35-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="eff35-111">Wenn die <strong>Filter</strong> -Eigenschaft auf ein zeichenfolgenkriterium festgelegt ist (wie &quot;Author = 'Smith'&quot;), und klicken Sie dann der Vorgang sichtbaren Datensätze im aktuellen Kapitel auswirkt.</span><span class="sxs-lookup"><span data-stu-id="eff35-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), then the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="eff35-112">Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wird der Vorgang alle Zeilen des <strong>Recordsets</strong>beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="eff35-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, then the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="eff35-113">AdAffectAll ist im Objektbrowser von Visual Basic ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="eff35-113">adAffectAll is hidden in the Visual Basic Object Browser.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff35-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="eff35-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="eff35-115">4</span><span class="sxs-lookup"><span data-stu-id="eff35-115">4</span></span></p></td>
<td><p><span data-ttu-id="eff35-116">Wirkt sich auf alle Datensätze in allen gleichgeordneten Kapiteln des <strong>Recordset-Objekts</strong>, einschließlich derjenigen, die über keinen der <strong>Filter</strong> , die momentan angewendet ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="eff35-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff35-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="eff35-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="eff35-118">1</span><span class="sxs-lookup"><span data-stu-id="eff35-118">1</span></span></p></td>
<td><p><span data-ttu-id="eff35-119">Wirkt sich lediglich auf den aktuellen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="eff35-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff35-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="eff35-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="eff35-121">2</span><span class="sxs-lookup"><span data-stu-id="eff35-121">2</span></span></p></td>
<td><p><span data-ttu-id="eff35-122">Wirkt sich auf nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a> -Eigenschaft zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="eff35-122">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting.</span></span> <span data-ttu-id="eff35-123">Sie müssen die <strong>Filter</strong> -Eigenschaft auf ein <strong>FilterGroupEnum</strong> -Wert oder ein Array von <strong>Lesezeichen</strong> verwenden Sie diese Option festlegen.</span><span class="sxs-lookup"><span data-stu-id="eff35-123">You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eff35-124">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="eff35-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="eff35-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="eff35-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff35-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="eff35-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff35-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="eff35-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff35-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="eff35-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff35-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="eff35-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff35-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="eff35-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

