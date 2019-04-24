---
title: CursorOptionEnum (Access Desktop Database Reference)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295198"
---
# <a name="cursoroptionenum"></a><span data-ttu-id="11e19-102">CursorOptionEnum</span><span class="sxs-lookup"><span data-stu-id="11e19-102">CursorOptionEnum</span></span>

<span data-ttu-id="11e19-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11e19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11e19-104">Gibt an, welche Funktionalität die [Supports](supports-method-ado.md)-Methode testen soll.</span><span class="sxs-lookup"><span data-stu-id="11e19-104">Specifies what functionality the [Supports](supports-method-ado.md) method should test for.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11e19-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="11e19-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="11e19-106">Wert</span><span class="sxs-lookup"><span data-stu-id="11e19-106">Value</span></span></p></th>
<th><p><span data-ttu-id="11e19-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11e19-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11e19-108"><strong>AddNew</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-108"><strong>adAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-109">0x1000400</span><span class="sxs-lookup"><span data-stu-id="11e19-109">0x1000400</span></span></p></td>
<td><p><span data-ttu-id="11e19-110">Unterstützt die <a href="addnew-method-ado.md">AddNew</a>-Methode, um neue Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="11e19-110">Supports the <a href="addnew-method-ado.md">AddNew</a> method to add new records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-111"><strong>adApproxPosition</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-111"><strong>adApproxPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-112">0x4000</span><span class="sxs-lookup"><span data-stu-id="11e19-112">0x4000</span></span></p></td>
<td><p><span data-ttu-id="11e19-113">Unterstützt die Eigenschaften <a href="absoluteposition-property-ado.md">AbsolutePosition</a> und <a href="absolutepage-property-ado.md">AbsolutePage</a>.</span><span class="sxs-lookup"><span data-stu-id="11e19-113">Supports the <a href="absoluteposition-property-ado.md">AbsolutePosition</a> and <a href="absolutepage-property-ado.md">AbsolutePage</a> properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-114"><strong>textMarke</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-114"><strong>adBookmark</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="11e19-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="11e19-116">Unterstützt die <a href="bookmark-property-ado.md">Bookmark</a>-Eigenschaft, um Zugriff auf bestimmte Datensätze zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="11e19-116">Supports the <a href="bookmark-property-ado.md">Bookmark</a> property to gain access to specific records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-117"><strong>Löschen</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-117"><strong>adDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-118">0x1000800</span><span class="sxs-lookup"><span data-stu-id="11e19-118">0x1000800</span></span></p></td>
<td><p><span data-ttu-id="11e19-119">Unterstützt die <a href="delete-method-ado-recordset.md">Delete</a>-Methode, um Datensätze zu löschen.</span><span class="sxs-lookup"><span data-stu-id="11e19-119">Supports the <a href="delete-method-ado-recordset.md">Delete</a> method to delete records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-120"><strong>adFind</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-120"><strong>adFind</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-121">0x80000</span><span class="sxs-lookup"><span data-stu-id="11e19-121">0x80000</span></span></p></td>
<td><p><span data-ttu-id="11e19-122">Unterstützt die <a href="find-method-ado.md">Find</a>-Methode, um eine Zeile in einem <a href="recordset-object-ado.md">Recordset</a> zu finden.</span><span class="sxs-lookup"><span data-stu-id="11e19-122">Supports the <a href="find-method-ado.md">Find</a> method to locate a row in a <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-123"><strong>adHoldRecords</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-123"><strong>adHoldRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-124">0x100</span><span class="sxs-lookup"><span data-stu-id="11e19-124">0x100</span></span></p></td>
<td><p><span data-ttu-id="11e19-125">Ruft mehrere Datensätze ab oder ändert die nächste Position, ohne ein Commit für alle ausstehenden Änderungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="11e19-125">Retrieves more records or changes the next position without committing all pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-126"><strong>adIndex</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-126"><strong>adIndex</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-127">0x100000</span><span class="sxs-lookup"><span data-stu-id="11e19-127">0x100000</span></span></p></td>
<td><p><span data-ttu-id="11e19-128">Unterstützt die <a href="index-property-ado.md">Index</a>-Eigenschaft, um einen Index zu benennen.</span><span class="sxs-lookup"><span data-stu-id="11e19-128">Supports the <a href="index-property-ado.md">Index</a> property to name an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-129"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-129"><strong>adMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-130">0x200</span><span class="sxs-lookup"><span data-stu-id="11e19-130">0x200</span></span></p></td>
<td><p><span data-ttu-id="11e19-131">Unterstützt die Methoden <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> und <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> sowie die Methoden <a href="move-method-ado.md">Move</a> oder <a href="getrows-method-ado.md">GetRows</a>, um die aktuelle Datensatzposition rückwärts zu verschieben, ohne Textmarken erforderlich zu machen.</span><span class="sxs-lookup"><span data-stu-id="11e19-131">Supports the <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> and <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> methods, and <a href="move-method-ado.md">Move</a> or <a href="getrows-method-ado.md">GetRows</a> methods to move the current record position backward without requiring bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-132"><strong>Benachrichtigen</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-132"><strong>adNotify</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-133">0x40000</span><span class="sxs-lookup"><span data-stu-id="11e19-133">0x40000</span></span></p></td>
<td><p><span data-ttu-id="11e19-134">Gibt an, dass der zugrunde liegende Datenprovider Benachrichtigungen unterstützt (was bestimmt, ob <strong>Recordset</strong>-Ereignisse unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="11e19-134">Indicates that the underlying data provider supports notifications (which determines whether <strong>Recordset</strong> events are supported).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-135"><strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-135"><strong>adResync</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-136">0x20000</span><span class="sxs-lookup"><span data-stu-id="11e19-136">0x20000</span></span></p></td>
<td><p><span data-ttu-id="11e19-137">Unterstützt die <a href="resync-method-ado.md">Resync</a>-Methode, um den Cursor mit den Daten zu aktualisieren, die in der zugrunde liegenden Datenbank sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="11e19-137">Supports the <a href="resync-method-ado.md">Resync</a> method to update the cursor with the data that is visible in the underlying database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-138"><strong>anSuchen</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-138"><strong>adSeek</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-139">0x200000</span><span class="sxs-lookup"><span data-stu-id="11e19-139">0x200000</span></span></p></td>
<td><p><span data-ttu-id="11e19-140">Unterstützt die <a href="seek-method-ado.md">Seek</a> -Methode, um eine Zeile in einem <strong>Recordset</strong>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="11e19-140">Supports the <a href="seek-method-ado.md">Seek</a> method to locate a row in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-141"><strong>adUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-141"><strong>adUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-142">0x1008000</span><span class="sxs-lookup"><span data-stu-id="11e19-142">0x1008000</span></span></p></td>
<td><p><span data-ttu-id="11e19-143">Unterstützt die <a href="update-method-ado.md">Update</a>-Methode, um vorhandene Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="11e19-143">Supports the <a href="update-method-ado.md">Update</a> method to modify existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-144"><strong>adUpdateBatch</strong></span><span class="sxs-lookup"><span data-stu-id="11e19-144"><strong>adUpdateBatch</strong></span></span></p></td>
<td><p><span data-ttu-id="11e19-145">0x10000</span><span class="sxs-lookup"><span data-stu-id="11e19-145">0x10000</span></span></p></td>
<td><p><span data-ttu-id="11e19-146">Unterstützt die Stapelaktualisierung (Methoden <a href="updatebatch-method-ado.md">UpdateBatch</a> und <a href="cancelbatch-method-ado.md">CancelBatch</a>), um mehrere Änderungen an den Anbieter zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="11e19-146">Supports batch updating (<a href="updatebatch-method-ado.md">UpdateBatch</a> and <a href="cancelbatch-method-ado.md">CancelBatch</a> methods) to transmit groups of changes to the provider.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="11e19-147">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="11e19-147">ADO/WFC equivalent</span></span>

<span data-ttu-id="11e19-148">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="11e19-148">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11e19-149">Konstante</span><span class="sxs-lookup"><span data-stu-id="11e19-149">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11e19-150">AdoEnums. CursorOption. ADDNEW</span><span class="sxs-lookup"><span data-stu-id="11e19-150">AdoEnums.CursorOption.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-151">AdoEnums. CursorOption. APPROXPOSITION</span><span class="sxs-lookup"><span data-stu-id="11e19-151">AdoEnums.CursorOption.APPROXPOSITION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-152">AdoEnums. CursorOption. BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="11e19-152">AdoEnums.CursorOption.BOOKMARK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-153">AdoEnums. CursorOption. DELETE</span><span class="sxs-lookup"><span data-stu-id="11e19-153">AdoEnums.CursorOption.DELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-154">AdoEnums. CursorOption. FIND</span><span class="sxs-lookup"><span data-stu-id="11e19-154">AdoEnums.CursorOption.FIND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-155">AdoEnums. CursorOption. HOLDRECORDS</span><span class="sxs-lookup"><span data-stu-id="11e19-155">AdoEnums.CursorOption.HOLDRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-156">AdoEnums. CursorOption. INDEX</span><span class="sxs-lookup"><span data-stu-id="11e19-156">AdoEnums.CursorOption.INDEX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-157">AdoEnums. CursorOption. MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="11e19-157">AdoEnums.CursorOption.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-158">AdoEnums. CursorOption. NOTIFY</span><span class="sxs-lookup"><span data-stu-id="11e19-158">AdoEnums.CursorOption.NOTIFY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-159">AdoEnums. CursorOption. reSYNC</span><span class="sxs-lookup"><span data-stu-id="11e19-159">AdoEnums.CursorOption.RESYNC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-160">AdoEnums. CursorOption. SEEK</span><span class="sxs-lookup"><span data-stu-id="11e19-160">AdoEnums.CursorOption.SEEK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11e19-161">AdoEnums. CursorOption. UPDATE</span><span class="sxs-lookup"><span data-stu-id="11e19-161">AdoEnums.CursorOption.UPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11e19-162">AdoEnums. CursorOption. UPDATEBATCH</span><span class="sxs-lookup"><span data-stu-id="11e19-162">AdoEnums.CursorOption.UPDATEBATCH</span></span></p></td>
</tr>
</tbody>
</table>

