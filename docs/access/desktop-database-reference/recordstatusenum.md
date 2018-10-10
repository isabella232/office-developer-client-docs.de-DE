---
title: RecordStatusEnum (Access PC-Datenbank-Referenz)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88929ced56583316c42f2d5195054e51e98a1d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474047"
---
# <a name="recordstatusenum"></a><span data-ttu-id="4ece7-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="4ece7-102">RecordStatusEnum</span></span>


<span data-ttu-id="4ece7-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ece7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ece7-104">Gibt den Status eines Datensatzes in Bezug auf Batchaktualisierungen und andere Mengenoperationen an.</span><span class="sxs-lookup"><span data-stu-id="4ece7-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ece7-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="4ece7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4ece7-106">Wert</span><span class="sxs-lookup"><span data-stu-id="4ece7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4ece7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ece7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-109">0 x 100</span><span class="sxs-lookup"><span data-stu-id="4ece7-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="4ece7-110">Gibt an, dass der Datensatz nicht gespeichert wurde, da die Operation abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-112">0 x 400</span><span class="sxs-lookup"><span data-stu-id="4ece7-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="4ece7-113">Gibt an, dass der neue Datensatz nicht gespeichert wurde, weil der vorhandene Datensatz gesperrt war.</span><span class="sxs-lookup"><span data-stu-id="4ece7-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-115">0 x 800</span><span class="sxs-lookup"><span data-stu-id="4ece7-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="4ece7-116">Gibt an, dass der Datensatz nicht gespeichert wurde, da eine vollständiger Parallelität verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-118">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="4ece7-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-119">Gibt an, dass der Datensatz bereits aus der Datenquelle gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-121">0 x 4</span><span class="sxs-lookup"><span data-stu-id="4ece7-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="4ece7-122">Gibt an, dass der Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-124">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="4ece7-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-125">Gibt an, dass der Datensatz nicht gespeichert wurde, da der Benutzer Integritätseinschränkungen verletzte.</span><span class="sxs-lookup"><span data-stu-id="4ece7-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-127">0 x 10</span><span class="sxs-lookup"><span data-stu-id="4ece7-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="4ece7-128">Gibt an, dass der Datensatz nicht gespeichert wurde, da seine Textmarke ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="4ece7-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-130">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="4ece7-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-131">Gibt an, dass der Datensatz nicht gespeichert wurde, da es zu viele ausstehende Änderungen gab.</span><span class="sxs-lookup"><span data-stu-id="4ece7-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-133">0 x 2</span><span class="sxs-lookup"><span data-stu-id="4ece7-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="4ece7-134">Gibt an, dass der Datensatz geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-136">0 x 40</span><span class="sxs-lookup"><span data-stu-id="4ece7-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="4ece7-137">Gibt an, dass der Datensatz nicht gespeichert wurde, da sich dies auf mehrere Datensätze ausgewirkt hätte.</span><span class="sxs-lookup"><span data-stu-id="4ece7-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-139">0 x 1</span><span class="sxs-lookup"><span data-stu-id="4ece7-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="4ece7-140">Gibt an, dass der Datensatz neu ist.</span><span class="sxs-lookup"><span data-stu-id="4ece7-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-142">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="4ece7-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-143">Gibt an, dass der Datensatz aufgrund eines Konflikts mit einem geöffneten Speicherobjekt nicht gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-145">0</span><span class="sxs-lookup"><span data-stu-id="4ece7-145">0</span></span></p></td>
<td><p><span data-ttu-id="4ece7-146">Gibt an, dass der Datensatz erfolgreich aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-148">0 x 8000</span><span class="sxs-lookup"><span data-stu-id="4ece7-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-149">Gibt an, dass der Datensatz nicht gespeichert wurde, da der Computer keinen Arbeitsspeicher mehr zur Verfügung hat.</span><span class="sxs-lookup"><span data-stu-id="4ece7-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-151">0 x 80</span><span class="sxs-lookup"><span data-stu-id="4ece7-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="4ece7-152">Gibt an, dass der Datensatz nicht gespeichert wurde, da er sich auf eine ausstehende Einfügung bezieht.</span><span class="sxs-lookup"><span data-stu-id="4ece7-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-154">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="4ece7-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-155">Gibt an, dass der Datensatz nicht gespeichert wurde, da der Benutzer über unzureichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4ece7-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-157">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="4ece7-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="4ece7-158">Gibt an, dass der Datensatz nicht gespeichert wurde, da er gegen die Struktur der zugrunde liegenden Datenbank verstößt.</span><span class="sxs-lookup"><span data-stu-id="4ece7-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="4ece7-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="4ece7-160">0 x 8</span><span class="sxs-lookup"><span data-stu-id="4ece7-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="4ece7-161">Gibt an, dass der Datensatz nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ece7-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ece7-162">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="4ece7-162">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="4ece7-163">AdoEnums.RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="4ece7-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="4ece7-164">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4ece7-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ece7-165">Konstante</span><span class="sxs-lookup"><span data-stu-id="4ece7-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="4ece7-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="4ece7-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="4ece7-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="4ece7-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="4ece7-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="4ece7-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="4ece7-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="4ece7-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="4ece7-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="4ece7-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="4ece7-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="4ece7-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="4ece7-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="4ece7-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="4ece7-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="4ece7-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ece7-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="4ece7-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ece7-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="4ece7-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

