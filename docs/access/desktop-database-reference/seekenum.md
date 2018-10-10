---
title: SeekEnum (Access PC-Datenbank-Referenz)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a151f7a4549a234c20f76bc1ac93d5eff6cf250
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472648"
---
# <a name="seekenum"></a><span data-ttu-id="54b73-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="54b73-102">SeekEnum</span></span>


<span data-ttu-id="54b73-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="54b73-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="54b73-104">Gibt die Art der auszuführenden [Suche](seek-method-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="54b73-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54b73-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="54b73-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="54b73-106">Wert</span><span class="sxs-lookup"><span data-stu-id="54b73-106">Value</span></span></p></th>
<th><p><span data-ttu-id="54b73-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54b73-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54b73-108">Nordwind.mdb</span><span class="sxs-lookup"><span data-stu-id="54b73-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="54b73-109">1</span><span class="sxs-lookup"><span data-stu-id="54b73-109">1</span></span></p></td>
<td><p><span data-ttu-id="54b73-110">Sucht den ersten Schlüssel, der <em>KeyValues</em> entspricht.</span><span class="sxs-lookup"><span data-stu-id="54b73-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b73-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="54b73-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="54b73-112">2</span><span class="sxs-lookup"><span data-stu-id="54b73-112">2</span></span></p></td>
<td><p><span data-ttu-id="54b73-113">Sucht den letzten Schlüssel, der <em>KeyValues</em> entspricht.</span><span class="sxs-lookup"><span data-stu-id="54b73-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54b73-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="54b73-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="54b73-115">4</span><span class="sxs-lookup"><span data-stu-id="54b73-115">4</span></span></p></td>
<td><p><span data-ttu-id="54b73-116">Sucht entweder einen Schlüssel, der <em>KeyValues</em> entspricht, oder direkt nach der Stelle, an der diese Übereinstimmung aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="54b73-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b73-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="54b73-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="54b73-118">8</span><span class="sxs-lookup"><span data-stu-id="54b73-118">8</span></span></p></td>
<td><p><span data-ttu-id="54b73-119">Sucht einen Schlüssel direkt nach der Stelle, an der eine Übereinstimmung mit <em>KeyValues</em> aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="54b73-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54b73-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="54b73-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="54b73-121">16</span><span class="sxs-lookup"><span data-stu-id="54b73-121">16</span></span></p></td>
<td><p><span data-ttu-id="54b73-122">Sucht einen Schlüssel, der entweder <em>KeyValues</em> entspricht, oder direkt vor der Stelle, an der diese Übereinstimmung aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="54b73-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b73-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="54b73-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="54b73-124">32</span><span class="sxs-lookup"><span data-stu-id="54b73-124">32</span></span></p></td>
<td><p><span data-ttu-id="54b73-125">Sucht einen Schlüssel direkt vor der Stelle, an der eine Übereinstimmung mit <em>KeyValues</em> aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="54b73-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54b73-126">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="54b73-126">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="54b73-127">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="54b73-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54b73-128">Konstante</span><span class="sxs-lookup"><span data-stu-id="54b73-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54b73-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="54b73-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b73-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="54b73-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54b73-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="54b73-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b73-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="54b73-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54b73-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="54b73-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b73-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="54b73-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

