---
title: SeekEnum (Access PC-Datenbank-Referenz)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698610"
---
# <a name="seekenum"></a><span data-ttu-id="c4121-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="c4121-102">SeekEnum</span></span>

<span data-ttu-id="c4121-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4121-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4121-104">Gibt die Art der auszuführenden [Suche](seek-method-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="c4121-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4121-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="c4121-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c4121-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c4121-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c4121-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4121-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4121-108">Nordwind.mdb</span><span class="sxs-lookup"><span data-stu-id="c4121-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="c4121-109">1</span><span class="sxs-lookup"><span data-stu-id="c4121-109">1</span></span></p></td>
<td><p><span data-ttu-id="c4121-110">Sucht den ersten Schlüssel, der <em>KeyValues</em> entspricht.</span><span class="sxs-lookup"><span data-stu-id="c4121-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4121-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="c4121-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="c4121-112">2</span><span class="sxs-lookup"><span data-stu-id="c4121-112">2</span></span></p></td>
<td><p><span data-ttu-id="c4121-113">Sucht den letzten Schlüssel, der <em>KeyValues</em> entspricht.</span><span class="sxs-lookup"><span data-stu-id="c4121-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4121-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="c4121-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="c4121-115">4</span><span class="sxs-lookup"><span data-stu-id="c4121-115">4</span></span></p></td>
<td><p><span data-ttu-id="c4121-116">Sucht entweder einen Schlüssel, der <em>KeyValues</em> entspricht, oder direkt nach der Stelle, an der diese Übereinstimmung aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="c4121-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4121-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="c4121-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="c4121-118">8</span><span class="sxs-lookup"><span data-stu-id="c4121-118">8</span></span></p></td>
<td><p><span data-ttu-id="c4121-119">Sucht einen Schlüssel direkt nach der Stelle, an der eine Übereinstimmung mit <em>KeyValues</em> aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="c4121-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4121-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="c4121-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="c4121-121">16</span><span class="sxs-lookup"><span data-stu-id="c4121-121">16</span></span></p></td>
<td><p><span data-ttu-id="c4121-122">Sucht einen Schlüssel, der entweder <em>KeyValues</em> entspricht, oder direkt vor der Stelle, an der diese Übereinstimmung aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="c4121-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4121-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="c4121-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="c4121-124">32</span><span class="sxs-lookup"><span data-stu-id="c4121-124">32</span></span></p></td>
<td><p><span data-ttu-id="c4121-125">Sucht einen Schlüssel direkt vor der Stelle, an der eine Übereinstimmung mit <em>KeyValues</em> aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="c4121-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c4121-126">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="c4121-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="c4121-127">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c4121-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4121-128">Konstante</span><span class="sxs-lookup"><span data-stu-id="c4121-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4121-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="c4121-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4121-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="c4121-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4121-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="c4121-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4121-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="c4121-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4121-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="c4121-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4121-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="c4121-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

