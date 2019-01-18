---
title: ResyncEnum (Access PC-Datenbank-Referenz)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff09d69a9cf36246b3367202531a011c4e1aba12
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703769"
---
# <a name="resyncenum"></a><span data-ttu-id="51d3f-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="51d3f-102">ResyncEnum</span></span>

<span data-ttu-id="51d3f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51d3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51d3f-104">Gibt an, ob die zugrunde liegenden Werte durch einen Aufruf von [Resync](resync-method-ado.md) überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="51d3f-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51d3f-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="51d3f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="51d3f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="51d3f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="51d3f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51d3f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51d3f-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="51d3f-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="51d3f-109">2</span><span class="sxs-lookup"><span data-stu-id="51d3f-109">2</span></span></p></td>
<td><p><span data-ttu-id="51d3f-p101">Standardwert. Überschreibt Daten, und die ausstehenden Aktualisierungen werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51d3f-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51d3f-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="51d3f-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="51d3f-113">1</span><span class="sxs-lookup"><span data-stu-id="51d3f-113">1</span></span></p></td>
<td><p><span data-ttu-id="51d3f-114">Überschreibt keine Daten, und die ausstehenden Aktualisierungen werden nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51d3f-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="51d3f-115">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="51d3f-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="51d3f-116">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="51d3f-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51d3f-117">Konstante</span><span class="sxs-lookup"><span data-stu-id="51d3f-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51d3f-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="51d3f-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51d3f-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="51d3f-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

