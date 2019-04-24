---
title: CompareEnum (Access Desktop Database Reference)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd120f726a51c884d063bb03f6d6864ea2d48344
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296066"
---
# <a name="compareenum"></a><span data-ttu-id="31c90-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="31c90-102">CompareEnum</span></span>

<span data-ttu-id="31c90-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31c90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31c90-104">Gibt die relative Position von zwei Datensätzen an, die durch ihre Textmarken dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="31c90-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31c90-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="31c90-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="31c90-106">Wert</span><span class="sxs-lookup"><span data-stu-id="31c90-106">Value</span></span></p></th>
<th><p><span data-ttu-id="31c90-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31c90-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31c90-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="31c90-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="31c90-109">1</span><span class="sxs-lookup"><span data-stu-id="31c90-109">1</span></span></p></td>
<td><p><span data-ttu-id="31c90-110">Gibt an, dass die Textmarken gleich sind.</span><span class="sxs-lookup"><span data-stu-id="31c90-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c90-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="31c90-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="31c90-112">2</span><span class="sxs-lookup"><span data-stu-id="31c90-112">2</span></span></p></td>
<td><p><span data-ttu-id="31c90-113">Gibt an, dass sich die erste Textmarke hinter der zweiten befindet.</span><span class="sxs-lookup"><span data-stu-id="31c90-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c90-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="31c90-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="31c90-115">0</span><span class="sxs-lookup"><span data-stu-id="31c90-115">0</span></span></p></td>
<td><p><span data-ttu-id="31c90-116">Gibt an, dass sich die erste Textmarke vor der zweiten befindet.</span><span class="sxs-lookup"><span data-stu-id="31c90-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c90-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="31c90-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="31c90-118">4</span><span class="sxs-lookup"><span data-stu-id="31c90-118">4</span></span></p></td>
<td><p><span data-ttu-id="31c90-119">Gibt an, dass die Textmarken nicht verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="31c90-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c90-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="31c90-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="31c90-121">3</span><span class="sxs-lookup"><span data-stu-id="31c90-121">3</span></span></p></td>
<td><p><span data-ttu-id="31c90-122">Gibt an, dass die Textmarken nicht gleich und nicht sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="31c90-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="31c90-123">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="31c90-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="31c90-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="31c90-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31c90-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="31c90-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31c90-126">AdoEnums. Compare. EQUAL</span><span class="sxs-lookup"><span data-stu-id="31c90-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c90-127">AdoEnums. Compare. GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="31c90-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c90-128">AdoEnums. Compare. LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="31c90-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31c90-129">AdoEnums. Compare. NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="31c90-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31c90-130">AdoEnums. Compare. NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="31c90-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

