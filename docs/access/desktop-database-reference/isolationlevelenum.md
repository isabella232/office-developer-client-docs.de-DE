---
title: IsolationLevelEnum (Access PC-Datenbank-Referenz)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7e32cd3c8ae78199f90fcac8cccdf377bf332d38
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863941"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="e0bd9-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="e0bd9-102">IsolationLevelEnum</span></span>

<span data-ttu-id="e0bd9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0bd9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e0bd9-104">Gibt die Transaktionsisolation für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0bd9-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="e0bd9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e0bd9-106">Wert</span><span class="sxs-lookup"><span data-stu-id="e0bd9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e0bd9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0bd9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-109">-1</span><span class="sxs-lookup"><span data-stu-id="e0bd9-109">-1</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-110">Gibt an, dass der Provider nicht die angegebene, sondern eine andere Isolationsstufe verwendet, diese Stufe jedoch nicht ermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-112">16</span><span class="sxs-lookup"><span data-stu-id="e0bd9-112">16</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-113">Gibt an, dass die ausstehenden Änderungen aus isolierteren Transaktionen nicht überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-115">256</span><span class="sxs-lookup"><span data-stu-id="e0bd9-115">256</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-116">Gibt an, dass Sie nicht gespeicherte Änderungen einer Transaktion in anderen Transaktionen anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-118">256</span><span class="sxs-lookup"><span data-stu-id="e0bd9-118">256</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-119">Entspricht <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-121">4096</span><span class="sxs-lookup"><span data-stu-id="e0bd9-121">4096</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-122">Gibt an, dass Sie Änderungen einer Transaktion in anderen Transaktionen anzeigen können, nachdem sie gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-124">4096</span><span class="sxs-lookup"><span data-stu-id="e0bd9-124">4096</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-125">Entspricht <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-127">65536</span><span class="sxs-lookup"><span data-stu-id="e0bd9-127">65536</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-128">Gibt an, dass Sie von einer Transaktion keine Änderungen, die in anderen Transaktionen vorgenommen wurden, anzeigen können, aber dass durch erneutes Abfragen neue <strong>Recordset</strong>-Objekte abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-130">1048576</span><span class="sxs-lookup"><span data-stu-id="e0bd9-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-131">Gibt an, dass Transaktionen in Isolierung anderer Transaktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="e0bd9-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bd9-133">1048576</span><span class="sxs-lookup"><span data-stu-id="e0bd9-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="e0bd9-134">Entspricht <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0bd9-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e0bd9-135">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="e0bd9-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="e0bd9-136">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e0bd9-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0bd9-137">Konstante</span><span class="sxs-lookup"><span data-stu-id="e0bd9-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="e0bd9-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="e0bd9-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="e0bd9-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="e0bd9-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="e0bd9-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="e0bd9-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="e0bd9-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0bd9-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="e0bd9-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0bd9-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="e0bd9-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

