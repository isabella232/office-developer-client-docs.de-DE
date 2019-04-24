---
title: CursorTypeEnum (Access Desktop Database Reference)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295163"
---
# <a name="cursortypeenum"></a><span data-ttu-id="aa690-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="aa690-102">CursorTypeEnum</span></span>

<span data-ttu-id="aa690-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa690-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa690-104">Gibt den in einem [Recordset](recordset-object-ado.md)-Objekt verwendeten Cursortyp an.</span><span class="sxs-lookup"><span data-stu-id="aa690-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa690-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="aa690-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="aa690-106">Wert</span><span class="sxs-lookup"><span data-stu-id="aa690-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aa690-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa690-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa690-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="aa690-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="aa690-109">2</span><span class="sxs-lookup"><span data-stu-id="aa690-109">2</span></span></p></td>
<td><p><span data-ttu-id="aa690-p101">Verwendet einen dynamischen Cursor. Hinzufügungen, Änderungen und Löschungen von anderen Benutzern sind sichtbar, und alle Arten der Navigation durch das Recordset sind zulässig, mit Ausnahme von Textmarken, falls diese vom Anbieter nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="aa690-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa690-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="aa690-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="aa690-113">0</span><span class="sxs-lookup"><span data-stu-id="aa690-113">0</span></span></p></td>
<td><p><span data-ttu-id="aa690-p102">Standardwert. Verwendet einen Vorwärtscursor. Mit einem statischen Cursor identisch, außer dass Sie in den Datensätzen nur einen Bildlauf vorwärts ausführen können. Wenn Sie nur einen Durchlauf durch ein Recordset ausführen müssen, wird die Leistung dadurch verbessert.</span><span class="sxs-lookup"><span data-stu-id="aa690-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa690-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="aa690-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="aa690-119">1</span><span class="sxs-lookup"><span data-stu-id="aa690-119">1</span></span></p></td>
<td><p><span data-ttu-id="aa690-p103">Verwendet einen Keysetcursor. Wie bei einem dynamischen Cursor, außer, dass Sie keine Datensätze anzeigen können, die von anderen Benutzern hinzugefügt werden, obwohl die von anderen Benutzern gelöschten Datensätze von Ihrem Recordset aus nicht zugänglich sind. Die Datenänderungen durch andere Benutzer sind weiterhin sichtbar.</span><span class="sxs-lookup"><span data-stu-id="aa690-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa690-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="aa690-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="aa690-124">3</span><span class="sxs-lookup"><span data-stu-id="aa690-124">3</span></span></p></td>
<td><p><span data-ttu-id="aa690-p104">Verwendet einen statischen Cursor. Eine statische Kopie einer Datensatzgruppe, die Sie zum Suchen von Daten oder Erstellen von Berichten verwenden können. Hinzufügungen, Änderungen oder Löschvorgänge durch andere Benutzer sind nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="aa690-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa690-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="aa690-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="aa690-129">-1</span><span class="sxs-lookup"><span data-stu-id="aa690-129">-1</span></span></p></td>
<td><p><span data-ttu-id="aa690-130">Gibt keinen Cursortyp an.</span><span class="sxs-lookup"><span data-stu-id="aa690-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="aa690-131">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="aa690-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="aa690-132">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="aa690-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa690-133">Konstante</span><span class="sxs-lookup"><span data-stu-id="aa690-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa690-134">AdoEnums. CursorType. DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="aa690-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa690-135">AdoEnums. CursorType. FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="aa690-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa690-136">AdoEnums. CursorType. KEYSet</span><span class="sxs-lookup"><span data-stu-id="aa690-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa690-137">AdoEnums. CursorType. STATIC</span><span class="sxs-lookup"><span data-stu-id="aa690-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa690-138">AdoEnums. CursorType. unSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="aa690-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

