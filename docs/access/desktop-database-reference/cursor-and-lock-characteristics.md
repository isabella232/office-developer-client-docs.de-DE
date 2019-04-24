---
title: Cursor- und Sperrenmerkmale
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295289"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="6d2e5-102">Cursor- und Sperrenmerkmale</span><span class="sxs-lookup"><span data-stu-id="6d2e5-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="6d2e5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d2e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d2e5-104">Die Merkmale eines Cursors hängen zwar von der Funktionalität des Anbieters ab, aber die folgenden Vor- und Nachteile gelten im Allgemeinen für die verschiedenen Typen von Cursorn und Sperren.</span><span class="sxs-lookup"><span data-stu-id="6d2e5-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d2e5-105">Cursor- oder Sperrtyp</span><span class="sxs-lookup"><span data-stu-id="6d2e5-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="6d2e5-106">Vorteile</span><span class="sxs-lookup"><span data-stu-id="6d2e5-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="6d2e5-107">Nachteile</span><span class="sxs-lookup"><span data-stu-id="6d2e5-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d2e5-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-109">Niedrige Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2e5-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-110">Bildlauf rückwärts ist nicht möglich</span><span class="sxs-lookup"><span data-stu-id="6d2e5-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-111">Keine Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="6d2e5-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d2e5-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-113">Bildlauffähigem</span><span class="sxs-lookup"><span data-stu-id="6d2e5-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-114">Keine Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="6d2e5-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d2e5-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-116">Gewisse Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="6d2e5-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-117">Bildlauffähigem</span><span class="sxs-lookup"><span data-stu-id="6d2e5-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-118">Höhere Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2e5-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-119">In getrenntem Szenario nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="6d2e5-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d2e5-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-121">Hohe Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="6d2e5-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-122">Bildlauffähigem</span><span class="sxs-lookup"><span data-stu-id="6d2e5-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-123">Höchste Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2e5-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-124">In getrenntem Szenario nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="6d2e5-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d2e5-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-126">Niedrige Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2e5-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-127">Extrem skalierbar</span><span class="sxs-lookup"><span data-stu-id="6d2e5-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-128">Daten sind über Cursor nicht aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="6d2e5-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d2e5-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-130">Batchaktualisierungen</span><span class="sxs-lookup"><span data-stu-id="6d2e5-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-131">Ermöglicht getrennte Szenarien</span><span class="sxs-lookup"><span data-stu-id="6d2e5-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="6d2e5-132">Andere Benutzer haben Zugriff auf Daten</span><span class="sxs-lookup"><span data-stu-id="6d2e5-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-133">Daten können von mehreren Benutzern gleichzeitig geändert werden</span><span class="sxs-lookup"><span data-stu-id="6d2e5-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d2e5-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-135">Daten können von anderen Benutzern nicht geändert werden, wenn sie gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="6d2e5-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-136">Andere Benutzer haben keinen Zugriff auf Daten, wenn sie gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="6d2e5-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d2e5-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="6d2e5-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-138">Andere Benutzer haben Zugriff auf Daten</span><span class="sxs-lookup"><span data-stu-id="6d2e5-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="6d2e5-139">Daten können von mehreren Benutzern gleichzeitig geändert werden</span><span class="sxs-lookup"><span data-stu-id="6d2e5-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

