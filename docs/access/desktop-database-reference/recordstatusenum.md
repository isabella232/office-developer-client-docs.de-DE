---
title: RecordStatusEnum (Access Desktop Database Reference)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309380"
---
# <a name="recordstatusenum"></a><span data-ttu-id="256b1-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="256b1-102">RecordStatusEnum</span></span>

<span data-ttu-id="256b1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="256b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="256b1-104">Gibt den Status eines Datensatzes in Bezug auf Batchaktualisierungen und andere Mengenoperationen an.</span><span class="sxs-lookup"><span data-stu-id="256b1-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="256b1-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="256b1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="256b1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="256b1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="256b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="256b1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="256b1-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-109">0x100</span><span class="sxs-lookup"><span data-stu-id="256b1-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="256b1-110">Gibt an, dass der Datensatz nicht gespeichert wurde, da die Operation abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-112">0x400</span><span class="sxs-lookup"><span data-stu-id="256b1-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="256b1-113">Gibt an, dass der neue Datensatz nicht gespeichert wurde, weil der vorhandene Datensatz gesperrt war.</span><span class="sxs-lookup"><span data-stu-id="256b1-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-115">0x800</span><span class="sxs-lookup"><span data-stu-id="256b1-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="256b1-116">Gibt an, dass der Datensatz nicht gespeichert wurde, da eine vollständiger Parallelität verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-118">0x40000</span><span class="sxs-lookup"><span data-stu-id="256b1-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="256b1-119">Gibt an, dass der Datensatz bereits aus der Datenquelle gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-121">0x4</span><span class="sxs-lookup"><span data-stu-id="256b1-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="256b1-122">Gibt an, dass der Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="256b1-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="256b1-125">Gibt an, dass der Datensatz nicht gespeichert wurde, da der Benutzer Integritätseinschränkungen verletzte.</span><span class="sxs-lookup"><span data-stu-id="256b1-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-127">0x10</span><span class="sxs-lookup"><span data-stu-id="256b1-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="256b1-128">Gibt an, dass der Datensatz nicht gespeichert wurde, da seine Textmarke ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="256b1-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="256b1-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="256b1-131">Gibt an, dass der Datensatz nicht gespeichert wurde, da es zu viele ausstehende Änderungen gab.</span><span class="sxs-lookup"><span data-stu-id="256b1-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-133">0x2</span><span class="sxs-lookup"><span data-stu-id="256b1-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="256b1-134">Gibt an, dass der Datensatz geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-136">0x40</span><span class="sxs-lookup"><span data-stu-id="256b1-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="256b1-137">Gibt an, dass der Datensatz nicht gespeichert wurde, da sich dies auf mehrere Datensätze ausgewirkt hätte.</span><span class="sxs-lookup"><span data-stu-id="256b1-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-139">0x1</span><span class="sxs-lookup"><span data-stu-id="256b1-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="256b1-140">Gibt an, dass der Datensatz neu ist.</span><span class="sxs-lookup"><span data-stu-id="256b1-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="256b1-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="256b1-143">Gibt an, dass der Datensatz aufgrund eines Konflikts mit einem geöffneten Speicherobjekt nicht gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-145">0</span><span class="sxs-lookup"><span data-stu-id="256b1-145">0</span></span></p></td>
<td><p><span data-ttu-id="256b1-146">Gibt an, dass der Datensatz erfolgreich aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-148">0X8000</span><span class="sxs-lookup"><span data-stu-id="256b1-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="256b1-149">Gibt an, dass der Datensatz nicht gespeichert wurde, da der Computer keinen Arbeitsspeicher mehr zur Verfügung hat.</span><span class="sxs-lookup"><span data-stu-id="256b1-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-151">0x80</span><span class="sxs-lookup"><span data-stu-id="256b1-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="256b1-152">Gibt an, dass der Datensatz nicht gespeichert wurde, da er sich auf eine ausstehende Einfügung bezieht.</span><span class="sxs-lookup"><span data-stu-id="256b1-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-154">0x10000</span><span class="sxs-lookup"><span data-stu-id="256b1-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="256b1-155">Gibt an, dass der Datensatz nicht gespeichert wurde, da der Benutzer über unzureichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="256b1-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-157">0x20000</span><span class="sxs-lookup"><span data-stu-id="256b1-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="256b1-158">Gibt an, dass der Datensatz nicht gespeichert wurde, da er gegen die Struktur der zugrunde liegenden Datenbank verstößt.</span><span class="sxs-lookup"><span data-stu-id="256b1-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="256b1-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="256b1-160">0x8</span><span class="sxs-lookup"><span data-stu-id="256b1-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="256b1-161">Gibt an, dass der Datensatz nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="256b1-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="256b1-162">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="256b1-162">ADO/WFC equivalent</span></span>

<span data-ttu-id="256b1-163">AdoEnums. RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="256b1-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="256b1-164">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="256b1-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="256b1-165">Konstante</span><span class="sxs-lookup"><span data-stu-id="256b1-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="256b1-166">AdoEnums. RecordStatus. CANCELed</span><span class="sxs-lookup"><span data-stu-id="256b1-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-167">AdoEnums. RecordStatus. CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="256b1-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-168">AdoEnums. RecordStatus. CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="256b1-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-169">AdoEnums. RecordStatus. dbDELETEd</span><span class="sxs-lookup"><span data-stu-id="256b1-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-170">AdoEnums. RecordStatus. DELETED</span><span class="sxs-lookup"><span data-stu-id="256b1-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-171">AdoEnums. RecordStatus. INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="256b1-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-172">AdoEnums. RecordStatus. INVALID</span><span class="sxs-lookup"><span data-stu-id="256b1-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-173">AdoEnums. RecordStatus. MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="256b1-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-174">AdoEnums. RecordStatus. MODIFIED</span><span class="sxs-lookup"><span data-stu-id="256b1-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-175">AdoEnums. RecordStatus. MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="256b1-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-176">AdoEnums. RecordStatus. NEW</span><span class="sxs-lookup"><span data-stu-id="256b1-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-177">AdoEnums. RecordStatus. objectOPEN</span><span class="sxs-lookup"><span data-stu-id="256b1-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-178">AdoEnums. RecordStatus. OK</span><span class="sxs-lookup"><span data-stu-id="256b1-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-179">AdoEnums. RecordStatus. OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="256b1-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-180">AdoEnums. RecordStatus. PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="256b1-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-181">AdoEnums. RecordStatus. PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="256b1-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256b1-182">AdoEnums. RecordStatus. SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="256b1-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256b1-183">AdoEnums. RecordStatus. unMODIFIED</span><span class="sxs-lookup"><span data-stu-id="256b1-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

