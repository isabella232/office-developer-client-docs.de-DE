---
title: EventReasonEnum (Access PC-Datenbank-Referenz)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec32b47d8e69c065d167fe86553aafdec906bc24
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472721"
---
# <a name="eventreasonenum"></a><span data-ttu-id="eb542-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="eb542-102">EventReasonEnum</span></span>


<span data-ttu-id="eb542-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb542-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb542-104">Gibt den Grund an, der zu einem Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="eb542-104">Specifies the reason that caused an event to occur.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb542-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="eb542-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="eb542-106">Wert</span><span class="sxs-lookup"><span data-stu-id="eb542-106">Value</span></span></p></th>
<th><p><span data-ttu-id="eb542-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb542-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb542-108"><strong>adRsnAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-109">1</span><span class="sxs-lookup"><span data-stu-id="eb542-109">1</span></span></p></td>
<td><p><span data-ttu-id="eb542-110">Ein neuer Datensatz wurde während eines Vorgangs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eb542-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-111"><strong>adRsnClose</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-112">9</span><span class="sxs-lookup"><span data-stu-id="eb542-112">9</span></span></p></td>
<td><p><span data-ttu-id="eb542-113">Ein Vorgangs geschlossen das <strong>Recordset-Objekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="eb542-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-114"><strong>adRsnDelete</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-115">2</span><span class="sxs-lookup"><span data-stu-id="eb542-115">2</span></span></p></td>
<td><p><span data-ttu-id="eb542-116">Ein Datensatz wurde während eines Vorgangs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="eb542-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-117"><strong>adRsnFirstChange</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-118">11</span><span class="sxs-lookup"><span data-stu-id="eb542-118">11</span></span></p></td>
<td><p><span data-ttu-id="eb542-119">Ein Datensatz wurde während eines Vorgangs erstmalig geändert.</span><span class="sxs-lookup"><span data-stu-id="eb542-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-120"><strong>adRsnMove</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-121">10</span><span class="sxs-lookup"><span data-stu-id="eb542-121">10</span></span></p></td>
<td><p><span data-ttu-id="eb542-122">Den Datensatzzeiger innerhalb des <strong>Recordset-Objekt</strong>während eines Vorgangs verschoben.</span><span class="sxs-lookup"><span data-stu-id="eb542-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-123"><strong>adRsnMoveFirst</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-124">12</span><span class="sxs-lookup"><span data-stu-id="eb542-124">12</span></span></p></td>
<td><p><span data-ttu-id="eb542-125">Den Datensatzzeiger während eines Vorgangs zum ersten Datensatz im <strong>Recordset</strong>verschoben.</span><span class="sxs-lookup"><span data-stu-id="eb542-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-126"><strong>adRsnMoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-127">15</span><span class="sxs-lookup"><span data-stu-id="eb542-127">15</span></span></p></td>
<td><p><span data-ttu-id="eb542-128">Den Datensatzzeiger während eines Vorgangs zum letzten Datensatz im <strong>Recordset</strong>verschoben.</span><span class="sxs-lookup"><span data-stu-id="eb542-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-129"><strong>adRsnMoveNext</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-130">13</span><span class="sxs-lookup"><span data-stu-id="eb542-130">13</span></span></p></td>
<td><p><span data-ttu-id="eb542-131">Den Datensatzzeiger während eines Vorgangs zum nächsten Datensatz im <strong>Recordset</strong>verschoben.</span><span class="sxs-lookup"><span data-stu-id="eb542-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-133">14</span><span class="sxs-lookup"><span data-stu-id="eb542-133">14</span></span></p></td>
<td><p><span data-ttu-id="eb542-134">Den Datensatzzeiger während eines Vorgangs zum vorherigen Datensatz im <strong>Recordset</strong>verschoben.</span><span class="sxs-lookup"><span data-stu-id="eb542-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-135"><strong>adRsnRequery</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-136">7</span><span class="sxs-lookup"><span data-stu-id="eb542-136">7</span></span></p></td>
<td><p><span data-ttu-id="eb542-137">Das <a href="recordset-object-ado.md">Recordset</a> wurde während eines Vorgangs erneut abgefragt.</span><span class="sxs-lookup"><span data-stu-id="eb542-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-138"><strong>adRsnResynch</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-139">8</span><span class="sxs-lookup"><span data-stu-id="eb542-139">8</span></span></p></td>
<td><p><span data-ttu-id="eb542-140">Ein Vorgang neu das <strong>Recordset-Objekt</strong> mit der Datenbank synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="eb542-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-142">5</span><span class="sxs-lookup"><span data-stu-id="eb542-142">5</span></span></p></td>
<td><p><span data-ttu-id="eb542-143">Das Hinzufügen eines neuen Datensatzes wurde während eines Vorgangs rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="eb542-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-145">6</span><span class="sxs-lookup"><span data-stu-id="eb542-145">6</span></span></p></td>
<td><p><span data-ttu-id="eb542-146">Das Löschen eines Datensatzes wurde während eines Vorgangs rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="eb542-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-148">4</span><span class="sxs-lookup"><span data-stu-id="eb542-148">4</span></span></p></td>
<td><p><span data-ttu-id="eb542-149">Das Aktualisieren eines Datensatzes wurde während eines Vorgangs rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="eb542-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-150"><strong>adRsnUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="eb542-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="eb542-151">3</span><span class="sxs-lookup"><span data-stu-id="eb542-151">3</span></span></p></td>
<td><p><span data-ttu-id="eb542-152">Ein vorhandener Datensatz wurde während eines Vorgangs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="eb542-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eb542-153">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="eb542-153">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="eb542-154">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="eb542-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb542-155">Konstante</span><span class="sxs-lookup"><span data-stu-id="eb542-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb542-156">AdoEnums.EventReason.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="eb542-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-157">AdoEnums.EventReason.CLOSE</span><span class="sxs-lookup"><span data-stu-id="eb542-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-158">AdoEnums.EventReason.DELETE</span><span class="sxs-lookup"><span data-stu-id="eb542-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-159">AdoEnums.EventReason.FIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="eb542-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-160">AdoEnums.EventReason.MOVE</span><span class="sxs-lookup"><span data-stu-id="eb542-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-161">AdoEnums.EventReason.MOVEFIRST</span><span class="sxs-lookup"><span data-stu-id="eb542-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-162">AdoEnums.EventReason.MOVELAST</span><span class="sxs-lookup"><span data-stu-id="eb542-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-163">AdoEnums.EventReason.MOVENEXT</span><span class="sxs-lookup"><span data-stu-id="eb542-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-164">AdoEnums.EventReason.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="eb542-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-165">AdoEnums.EventReason.REQUERY</span><span class="sxs-lookup"><span data-stu-id="eb542-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-166">AdoEnums.EventReason.RESYNCH</span><span class="sxs-lookup"><span data-stu-id="eb542-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-167">AdoEnums.EventReason.UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="eb542-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-168">AdoEnums.EventReason.UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="eb542-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb542-169">AdoEnums.EventReason.UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="eb542-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb542-170">AdoEnums.EventReason.UPDATE</span><span class="sxs-lookup"><span data-stu-id="eb542-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

