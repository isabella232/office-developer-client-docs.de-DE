---
title: CompareEnum (Access PC-Datenbank-Referenz)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 4749064e938912c459f455e54702460339994c37
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874573"
---
# <a name="compareenum"></a><span data-ttu-id="3d014-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="3d014-102">CompareEnum</span></span>

<span data-ttu-id="3d014-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d014-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d014-104">Gibt die relative Position von zwei Datensätzen an, die durch ihre Textmarken dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3d014-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d014-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="3d014-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3d014-106">Wert</span><span class="sxs-lookup"><span data-stu-id="3d014-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3d014-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d014-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d014-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="3d014-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="3d014-109">1</span><span class="sxs-lookup"><span data-stu-id="3d014-109">1</span></span></p></td>
<td><p><span data-ttu-id="3d014-110">Gibt an, dass die Textmarken gleich sind.</span><span class="sxs-lookup"><span data-stu-id="3d014-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d014-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="3d014-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="3d014-112">2</span><span class="sxs-lookup"><span data-stu-id="3d014-112">2</span></span></p></td>
<td><p><span data-ttu-id="3d014-113">Gibt an, dass sich die erste Textmarke hinter der zweiten befindet.</span><span class="sxs-lookup"><span data-stu-id="3d014-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d014-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="3d014-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="3d014-115">0</span><span class="sxs-lookup"><span data-stu-id="3d014-115">0</span></span></p></td>
<td><p><span data-ttu-id="3d014-116">Gibt an, dass sich die erste Textmarke vor der zweiten befindet.</span><span class="sxs-lookup"><span data-stu-id="3d014-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d014-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="3d014-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="3d014-118">4</span><span class="sxs-lookup"><span data-stu-id="3d014-118">4</span></span></p></td>
<td><p><span data-ttu-id="3d014-119">Gibt an, dass die Textmarken nicht verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="3d014-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d014-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="3d014-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="3d014-121">3</span><span class="sxs-lookup"><span data-stu-id="3d014-121">3</span></span></p></td>
<td><p><span data-ttu-id="3d014-122">Gibt an, dass die Textmarken nicht gleich und nicht sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="3d014-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3d014-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="3d014-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="3d014-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3d014-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d014-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="3d014-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d014-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="3d014-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d014-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="3d014-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d014-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="3d014-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d014-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="3d014-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d014-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="3d014-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

