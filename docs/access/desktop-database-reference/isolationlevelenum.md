---
title: IsolationLevelEnum (Access PC-Datenbank-Referenz)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cb8873a7ddfc62429847b561736df4bfa91d429d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872845"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="cac7a-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="cac7a-102">IsolationLevelEnum</span></span>

<span data-ttu-id="cac7a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cac7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cac7a-104">Gibt die Transaktionsisolation für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cac7a-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cac7a-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="cac7a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cac7a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="cac7a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cac7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cac7a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-109">-1</span><span class="sxs-lookup"><span data-stu-id="cac7a-109">-1</span></span></p></td>
<td><p><span data-ttu-id="cac7a-110">Gibt an, dass der Provider nicht die angegebene, sondern eine andere Isolationsstufe verwendet, diese Stufe jedoch nicht ermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cac7a-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-112">16</span><span class="sxs-lookup"><span data-stu-id="cac7a-112">16</span></span></p></td>
<td><p><span data-ttu-id="cac7a-113">Gibt an, dass die ausstehenden Änderungen aus isolierteren Transaktionen nicht überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="cac7a-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-115">256</span><span class="sxs-lookup"><span data-stu-id="cac7a-115">256</span></span></p></td>
<td><p><span data-ttu-id="cac7a-116">Gibt an, dass Sie nicht gespeicherte Änderungen einer Transaktion in anderen Transaktionen anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="cac7a-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-118">256</span><span class="sxs-lookup"><span data-stu-id="cac7a-118">256</span></span></p></td>
<td><p><span data-ttu-id="cac7a-119">Entspricht <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac7a-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-121">4096</span><span class="sxs-lookup"><span data-stu-id="cac7a-121">4096</span></span></p></td>
<td><p><span data-ttu-id="cac7a-122">Gibt an, dass Sie Änderungen einer Transaktion in anderen Transaktionen anzeigen können, nachdem sie gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="cac7a-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-124">4096</span><span class="sxs-lookup"><span data-stu-id="cac7a-124">4096</span></span></p></td>
<td><p><span data-ttu-id="cac7a-125">Entspricht <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac7a-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-127">65536</span><span class="sxs-lookup"><span data-stu-id="cac7a-127">65536</span></span></p></td>
<td><p><span data-ttu-id="cac7a-128">Gibt an, dass Sie von einer Transaktion keine Änderungen, die in anderen Transaktionen vorgenommen wurden, anzeigen können, aber dass durch erneutes Abfragen neue <strong>Recordset</strong>-Objekte abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="cac7a-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-130">1048576</span><span class="sxs-lookup"><span data-stu-id="cac7a-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="cac7a-131">Gibt an, dass Transaktionen in Isolierung anderer Transaktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cac7a-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="cac7a-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="cac7a-133">1048576</span><span class="sxs-lookup"><span data-stu-id="cac7a-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="cac7a-134">Entspricht <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac7a-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cac7a-135">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="cac7a-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="cac7a-136">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cac7a-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cac7a-137">Konstante</span><span class="sxs-lookup"><span data-stu-id="cac7a-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="cac7a-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="cac7a-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="cac7a-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="cac7a-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="cac7a-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="cac7a-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="cac7a-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cac7a-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="cac7a-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cac7a-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="cac7a-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

