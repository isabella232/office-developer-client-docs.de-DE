---
title: ResyncEnum (Access Desktop Database Reference)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff09d69a9cf36246b3367202531a011c4e1aba12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306545"
---
# <a name="resyncenum"></a><span data-ttu-id="c9656-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="c9656-102">ResyncEnum</span></span>

<span data-ttu-id="c9656-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9656-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9656-104">Gibt an, ob die zugrunde liegenden Werte durch einen Aufruf von [Resync](resync-method-ado.md) überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c9656-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9656-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="c9656-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c9656-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c9656-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c9656-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9656-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9656-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="c9656-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="c9656-109">2</span><span class="sxs-lookup"><span data-stu-id="c9656-109">2</span></span></p></td>
<td><p><span data-ttu-id="c9656-p101">Standardwert. Überschreibt Daten, und die ausstehenden Aktualisierungen werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c9656-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9656-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="c9656-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="c9656-113">1</span><span class="sxs-lookup"><span data-stu-id="c9656-113">1</span></span></p></td>
<td><p><span data-ttu-id="c9656-114">Überschreibt keine Daten, und die ausstehenden Aktualisierungen werden nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c9656-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c9656-115">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="c9656-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="c9656-116">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c9656-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9656-117">Konstante</span><span class="sxs-lookup"><span data-stu-id="c9656-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9656-118">AdoEnums. Resync. allVALUEs</span><span class="sxs-lookup"><span data-stu-id="c9656-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9656-119">AdoEnums. Resync. UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="c9656-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

