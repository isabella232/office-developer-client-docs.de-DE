---
title: ResyncEnum (Access PC-Datenbank-Referenz)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3607c0796edb58a6d4227fee09a658220deabfe7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475889"
---
# <a name="resyncenum"></a><span data-ttu-id="323f5-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="323f5-102">ResyncEnum</span></span>


<span data-ttu-id="323f5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="323f5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="323f5-104">Gibt an, ob die zugrunde liegenden Werte durch einen Aufruf von [Resync](resync-method-ado.md) überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="323f5-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="323f5-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="323f5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="323f5-106">Wert</span><span class="sxs-lookup"><span data-stu-id="323f5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="323f5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="323f5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="323f5-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="323f5-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="323f5-109">2</span><span class="sxs-lookup"><span data-stu-id="323f5-109">2</span></span></p></td>
<td><p><span data-ttu-id="323f5-p101">Standardwert. Überschreibt Daten, und die ausstehenden Aktualisierungen werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="323f5-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="323f5-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="323f5-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="323f5-113">1</span><span class="sxs-lookup"><span data-stu-id="323f5-113">1</span></span></p></td>
<td><p><span data-ttu-id="323f5-114">Überschreibt keine Daten, und die ausstehenden Aktualisierungen werden nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="323f5-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="323f5-115">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="323f5-115">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="323f5-116">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="323f5-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="323f5-117">Konstante</span><span class="sxs-lookup"><span data-stu-id="323f5-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="323f5-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="323f5-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="323f5-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="323f5-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

