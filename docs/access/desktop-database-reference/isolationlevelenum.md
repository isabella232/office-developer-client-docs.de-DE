---
title: IsolationLevelEnum (Access PC-Datenbank-Referenz)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80e7d22a5152b24894bf746b939f705739d4220d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475990"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="47e10-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="47e10-102">IsolationLevelEnum</span></span>


<span data-ttu-id="47e10-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="47e10-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="47e10-104">Gibt die Transaktionsisolation für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="47e10-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47e10-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="47e10-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="47e10-106">Wert</span><span class="sxs-lookup"><span data-stu-id="47e10-106">Value</span></span></p></th>
<th><p><span data-ttu-id="47e10-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47e10-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47e10-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-109">-1</span><span class="sxs-lookup"><span data-stu-id="47e10-109">-1</span></span></p></td>
<td><p><span data-ttu-id="47e10-110">Gibt an, dass der Provider nicht die angegebene, sondern eine andere Isolationsstufe verwendet, diese Stufe jedoch nicht ermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47e10-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-112">16</span><span class="sxs-lookup"><span data-stu-id="47e10-112">16</span></span></p></td>
<td><p><span data-ttu-id="47e10-113">Gibt an, dass die ausstehenden Änderungen aus isolierteren Transaktionen nicht überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="47e10-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-115">256</span><span class="sxs-lookup"><span data-stu-id="47e10-115">256</span></span></p></td>
<td><p><span data-ttu-id="47e10-116">Gibt an, dass Sie nicht gespeicherte Änderungen einer Transaktion in anderen Transaktionen anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="47e10-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-118">256</span><span class="sxs-lookup"><span data-stu-id="47e10-118">256</span></span></p></td>
<td><p><span data-ttu-id="47e10-119">Entspricht <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="47e10-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-121">4096</span><span class="sxs-lookup"><span data-stu-id="47e10-121">4096</span></span></p></td>
<td><p><span data-ttu-id="47e10-122">Gibt an, dass Sie Änderungen einer Transaktion in anderen Transaktionen anzeigen können, nachdem sie gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="47e10-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-124">4096</span><span class="sxs-lookup"><span data-stu-id="47e10-124">4096</span></span></p></td>
<td><p><span data-ttu-id="47e10-125">Entspricht <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="47e10-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-127">65536</span><span class="sxs-lookup"><span data-stu-id="47e10-127">65536</span></span></p></td>
<td><p><span data-ttu-id="47e10-128">Gibt an, dass Sie von einer Transaktion keine Änderungen, die in anderen Transaktionen vorgenommen wurden, anzeigen können, aber dass durch erneutes Abfragen neue <strong>Recordset</strong>-Objekte abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="47e10-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-130">1048576</span><span class="sxs-lookup"><span data-stu-id="47e10-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="47e10-131">Gibt an, dass Transaktionen in Isolierung anderer Transaktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="47e10-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="47e10-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="47e10-133">1048576</span><span class="sxs-lookup"><span data-stu-id="47e10-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="47e10-134">Entspricht <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="47e10-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47e10-135">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="47e10-135">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="47e10-136">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="47e10-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47e10-137">Konstante</span><span class="sxs-lookup"><span data-stu-id="47e10-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47e10-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="47e10-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="47e10-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="47e10-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="47e10-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="47e10-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="47e10-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="47e10-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47e10-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="47e10-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47e10-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="47e10-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

