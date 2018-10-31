---
title: ObjectStateEnum (Access PC-Datenbank-Referenz)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: e15faf0b31965a0a8a71440f424729b13b117b05
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861454"
---
# <a name="objectstateenum"></a><span data-ttu-id="cf32f-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="cf32f-102">ObjectStateEnum</span></span>

<span data-ttu-id="cf32f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf32f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cf32f-104">Gibt an, ob ein Objekt geöffnet oder geschlossen ist, eine Verbindung mit einer Datenquelle herstellt, einen Befehl ausführt oder Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="cf32f-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf32f-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="cf32f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cf32f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="cf32f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cf32f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf32f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf32f-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="cf32f-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="cf32f-109">0</span><span class="sxs-lookup"><span data-stu-id="cf32f-109">0</span></span></p></td>
<td><p><span data-ttu-id="cf32f-110">Gibt an, dass das Objekt geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cf32f-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf32f-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="cf32f-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="cf32f-112">1</span><span class="sxs-lookup"><span data-stu-id="cf32f-112">1</span></span></p></td>
<td><p><span data-ttu-id="cf32f-113">Gibt an, dass das Objekt geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="cf32f-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf32f-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="cf32f-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="cf32f-115">2</span><span class="sxs-lookup"><span data-stu-id="cf32f-115">2</span></span></p></td>
<td><p><span data-ttu-id="cf32f-116">Gibt an, dass das Objekt eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="cf32f-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf32f-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="cf32f-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="cf32f-118">4</span><span class="sxs-lookup"><span data-stu-id="cf32f-118">4</span></span></p></td>
<td><p><span data-ttu-id="cf32f-119">Gibt an, dass das Objekt einen Befehl ausführt.</span><span class="sxs-lookup"><span data-stu-id="cf32f-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf32f-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="cf32f-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="cf32f-121">8</span><span class="sxs-lookup"><span data-stu-id="cf32f-121">8</span></span></p></td>
<td><p><span data-ttu-id="cf32f-122">Gibt an, dass die Zeilen des Objekts abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cf32f-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cf32f-123">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="cf32f-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="cf32f-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cf32f-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf32f-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="cf32f-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf32f-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="cf32f-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf32f-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="cf32f-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf32f-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="cf32f-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf32f-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="cf32f-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf32f-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="cf32f-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

