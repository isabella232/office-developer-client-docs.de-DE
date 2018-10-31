---
title: CompareEnum (Access PC-Datenbank-Referenz)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8c35b04dc1b5aa0a97236ff7ece260018cbe29c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860308"
---
# <a name="compareenum"></a><span data-ttu-id="ff939-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="ff939-102">CompareEnum</span></span>

<span data-ttu-id="ff939-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff939-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ff939-104">Gibt die relative Position von zwei Datensätzen an, die durch ihre Textmarken dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff939-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff939-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="ff939-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ff939-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ff939-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ff939-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff939-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff939-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="ff939-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="ff939-109">1</span><span class="sxs-lookup"><span data-stu-id="ff939-109">1</span></span></p></td>
<td><p><span data-ttu-id="ff939-110">Gibt an, dass die Textmarken gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ff939-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff939-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="ff939-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="ff939-112">2</span><span class="sxs-lookup"><span data-stu-id="ff939-112">2</span></span></p></td>
<td><p><span data-ttu-id="ff939-113">Gibt an, dass sich die erste Textmarke hinter der zweiten befindet.</span><span class="sxs-lookup"><span data-stu-id="ff939-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff939-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="ff939-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="ff939-115">0</span><span class="sxs-lookup"><span data-stu-id="ff939-115">0</span></span></p></td>
<td><p><span data-ttu-id="ff939-116">Gibt an, dass sich die erste Textmarke vor der zweiten befindet.</span><span class="sxs-lookup"><span data-stu-id="ff939-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff939-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="ff939-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="ff939-118">4</span><span class="sxs-lookup"><span data-stu-id="ff939-118">4</span></span></p></td>
<td><p><span data-ttu-id="ff939-119">Gibt an, dass die Textmarken nicht verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="ff939-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff939-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="ff939-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="ff939-121">3</span><span class="sxs-lookup"><span data-stu-id="ff939-121">3</span></span></p></td>
<td><p><span data-ttu-id="ff939-122">Gibt an, dass die Textmarken nicht gleich und nicht sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="ff939-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ff939-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="ff939-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="ff939-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ff939-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff939-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="ff939-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff939-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="ff939-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff939-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="ff939-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff939-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="ff939-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff939-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="ff939-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff939-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="ff939-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

