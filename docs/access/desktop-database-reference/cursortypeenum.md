---
title: CursorTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710790"
---
# <a name="cursortypeenum"></a><span data-ttu-id="c41d3-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="c41d3-102">CursorTypeEnum</span></span>

<span data-ttu-id="c41d3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c41d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c41d3-104">Gibt den in einem [Recordset](recordset-object-ado.md)-Objekt verwendeten Cursortyp an.</span><span class="sxs-lookup"><span data-stu-id="c41d3-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c41d3-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="c41d3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c41d3-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c41d3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c41d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c41d3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c41d3-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="c41d3-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="c41d3-109">2</span><span class="sxs-lookup"><span data-stu-id="c41d3-109">2</span></span></p></td>
<td><p><span data-ttu-id="c41d3-110">Verwendet einen dynamischen Cursor.</span><span class="sxs-lookup"><span data-stu-id="c41d3-110">Uses a dynamic cursor.</span></span> <span data-ttu-id="c41d3-111">Hinzufügen, ändern und Löschen von anderen Benutzern angezeigt werden, und alle Arten von Bewegung durch das <strong>Recordset-Objekt</strong> sind zulässig, mit Ausnahme von Lesezeichen, wenn der Anbieter sie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c41d3-111">Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c41d3-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="c41d3-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="c41d3-113">0</span><span class="sxs-lookup"><span data-stu-id="c41d3-113">0</span></span></p></td>
<td><p><span data-ttu-id="c41d3-114">Standard.</span><span class="sxs-lookup"><span data-stu-id="c41d3-114">Default.</span></span> <span data-ttu-id="c41d3-115">Ein Vorwärtscursor verwendet.</span><span class="sxs-lookup"><span data-stu-id="c41d3-115">Uses a forward-only cursor.</span></span> <span data-ttu-id="c41d3-116">Identisch mit einer statischen Cursor, außer dass Sie nur vorwärts durch die Datensätze blättern können.</span><span class="sxs-lookup"><span data-stu-id="c41d3-116">Identical to a static cursor, except that you can only scroll forward through records.</span></span> <span data-ttu-id="c41d3-117">Dies verbessert die Leistung, wenn Sie nur eine Pass-through-ein <strong>Recordset</strong>treffen müssen.</span><span class="sxs-lookup"><span data-stu-id="c41d3-117">This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c41d3-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="c41d3-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="c41d3-119">1</span><span class="sxs-lookup"><span data-stu-id="c41d3-119">1</span></span></p></td>
<td><p><span data-ttu-id="c41d3-120">Verwendet einen Keysetcursor.</span><span class="sxs-lookup"><span data-stu-id="c41d3-120">Uses a keyset cursor.</span></span> <span data-ttu-id="c41d3-121">Wie Sie einen dynamischen Cursor mit der Ausnahme, dass Sie keine Datensätze, die andere Benutzer anzeigen hinzufügen, obwohl Datensätze, die andere Benutzer löschen aus dem <strong>Recordset-Objekt</strong>zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c41d3-121">Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>.</span></span> <span data-ttu-id="c41d3-122">Datenänderungen durch andere Benutzer werden weiterhin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c41d3-122">Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c41d3-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="c41d3-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="c41d3-124">3</span><span class="sxs-lookup"><span data-stu-id="c41d3-124">3</span></span></p></td>
<td><p><span data-ttu-id="c41d3-p104">Verwendet einen statischen Cursor. Eine statische Kopie einer Datensatzgruppe, die Sie zum Suchen von Daten oder Erstellen von Berichten verwenden können. Hinzufügungen, Änderungen oder Löschvorgänge durch andere Benutzer sind nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="c41d3-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c41d3-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="c41d3-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="c41d3-129">-1</span><span class="sxs-lookup"><span data-stu-id="c41d3-129">-1</span></span></p></td>
<td><p><span data-ttu-id="c41d3-130">Gibt keinen Cursortyp an.</span><span class="sxs-lookup"><span data-stu-id="c41d3-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c41d3-131">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="c41d3-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="c41d3-132">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c41d3-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c41d3-133">Konstante</span><span class="sxs-lookup"><span data-stu-id="c41d3-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c41d3-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="c41d3-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c41d3-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="c41d3-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c41d3-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="c41d3-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c41d3-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="c41d3-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c41d3-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="c41d3-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

