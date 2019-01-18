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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704616"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="c5457-102">Cursor- und Sperrenmerkmale</span><span class="sxs-lookup"><span data-stu-id="c5457-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="c5457-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5457-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5457-104">Die Merkmale eines Cursors hängen zwar von der Funktionalität des Anbieters ab, aber die folgenden Vor- und Nachteile gelten im Allgemeinen für die verschiedenen Typen von Cursorn und Sperren.</span><span class="sxs-lookup"><span data-stu-id="c5457-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5457-105">Cursor- oder Sperrtyp</span><span class="sxs-lookup"><span data-stu-id="c5457-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="c5457-106">Vorteile</span><span class="sxs-lookup"><span data-stu-id="c5457-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="c5457-107">Nachteile</span><span class="sxs-lookup"><span data-stu-id="c5457-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5457-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-109">Niedrige Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="c5457-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-110">Bildlauf rückwärts ist nicht möglich</span><span class="sxs-lookup"><span data-stu-id="c5457-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="c5457-111">Keine Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="c5457-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5457-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-113">Bildlauffähig</span><span class="sxs-lookup"><span data-stu-id="c5457-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-114">Keine Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="c5457-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5457-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-116">Gewisse Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="c5457-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="c5457-117">Bildlauffähig</span><span class="sxs-lookup"><span data-stu-id="c5457-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-118">Höhere Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="c5457-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="c5457-119">In getrenntem Szenario nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c5457-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5457-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-121">Hohe Datenparallelität</span><span class="sxs-lookup"><span data-stu-id="c5457-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="c5457-122">Bildlauffähig</span><span class="sxs-lookup"><span data-stu-id="c5457-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-123">Höchste Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="c5457-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="c5457-124">In getrenntem Szenario nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c5457-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5457-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-126">Niedrige Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="c5457-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="c5457-127">Extrem skalierbar</span><span class="sxs-lookup"><span data-stu-id="c5457-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-128">Daten sind über Cursor nicht aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="c5457-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5457-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-130">Batchaktualisierungen</span><span class="sxs-lookup"><span data-stu-id="c5457-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="c5457-131">Ermöglicht getrennte Szenarien</span><span class="sxs-lookup"><span data-stu-id="c5457-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="c5457-132">Andere Benutzer haben Zugriff auf Daten</span><span class="sxs-lookup"><span data-stu-id="c5457-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-133">Daten können von mehreren Benutzern gleichzeitig geändert werden</span><span class="sxs-lookup"><span data-stu-id="c5457-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5457-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-135">Daten können von anderen Benutzern nicht geändert werden, wenn sie gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="c5457-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-136">Andere Benutzer haben keinen Zugriff auf Daten, wenn sie gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="c5457-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5457-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="c5457-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-138">Andere Benutzer haben Zugriff auf Daten</span><span class="sxs-lookup"><span data-stu-id="c5457-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="c5457-139">Daten können von mehreren Benutzern gleichzeitig geändert werden</span><span class="sxs-lookup"><span data-stu-id="c5457-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

