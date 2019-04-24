---
title: EventReasonEnum (Access Desktop Database Reference)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293329"
---
# <a name="eventreasonenum"></a><span data-ttu-id="2d4bf-102">EventReasonEnum</span><span class="sxs-lookup"><span data-stu-id="2d4bf-102">EventReasonEnum</span></span>

<span data-ttu-id="2d4bf-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d4bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d4bf-104">Gibt den Grund an, der zu einem Ereignis führte.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-104">Specifies the reason that caused an event to occur.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d4bf-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="2d4bf-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d4bf-106">Wert</span><span class="sxs-lookup"><span data-stu-id="2d4bf-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2d4bf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d4bf-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-108"><strong>adRsnAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-108"><strong>adRsnAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-109">1</span><span class="sxs-lookup"><span data-stu-id="2d4bf-109">1</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-110">Ein neuer Datensatz wurde während eines Vorgangs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-110">An operation added a new record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-111"><strong>adRsnClose</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-111"><strong>adRsnClose</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-112">9</span><span class="sxs-lookup"><span data-stu-id="2d4bf-112">9</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-113">Das Recordset wurde während eines Vorgangs geschlossen.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-113">An operation closed the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-114"><strong>adRsnDelete</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-114"><strong>adRsnDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-115">2</span><span class="sxs-lookup"><span data-stu-id="2d4bf-115">2</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-116">Ein Datensatz wurde während eines Vorgangs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-116">An operation deleted a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-117"><strong>adRsnFirstChange</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-117"><strong>adRsnFirstChange</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-118">11</span><span class="sxs-lookup"><span data-stu-id="2d4bf-118">11</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-119">Ein Datensatz wurde während eines Vorgangs erstmalig geändert.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-119">An operation made the first change to a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-120"><strong>adRsnMove</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-120"><strong>adRsnMove</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-121">10</span><span class="sxs-lookup"><span data-stu-id="2d4bf-121">10</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-122">Der Datensatzzeiger wurde während eines Vorgangs innerhalb des Recordsets bewegt.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-122">An operation moved the record pointer within the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-123"><strong>adRsnMoveFirst</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-123"><strong>adRsnMoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-124">12</span><span class="sxs-lookup"><span data-stu-id="2d4bf-124">12</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-125">Der Datensatzzeiger wurde während eines Vorgangs zum ersten Datensatz im Recordset verschoben.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-125">An operation moved the record pointer to the first record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-126"><strong>adRsnMoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-126"><strong>adRsnMoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-127">15</span><span class="sxs-lookup"><span data-stu-id="2d4bf-127">15</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-128">Der Datensatzzeiger wurde während eines Vorgangs zum letzten Datensatz im Recordset verschoben.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-128">An operation moved the record pointer to the last record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-129"><strong>adRsnMoveNext</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-129"><strong>adRsnMoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-130">13</span><span class="sxs-lookup"><span data-stu-id="2d4bf-130">13</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-131">Der Datensatzzeiger wurde während eines Vorgangs zum nächsten Datensatz im Recordset verschoben.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-131">An operation moved the record pointer to the next record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-132"><strong>adRsnMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-132"><strong>adRsnMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-133">14</span><span class="sxs-lookup"><span data-stu-id="2d4bf-133">14</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-134">Der Datensatzzeiger wurde während eines Vorgangs zum vorherigen Datensatz im Recordset verschoben.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-134">An operation moved the record pointer to the previous record in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-135"><strong>adRsnRequery</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-135"><strong>adRsnRequery</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-136">7</span><span class="sxs-lookup"><span data-stu-id="2d4bf-136">7</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-137">Das <a href="recordset-object-ado.md">Recordset</a> wurde während eines Vorgangs erneut abgefragt.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-137">An operation requeried the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-138"><strong>adRsnResynch</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-138"><strong>adRsnResynch</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-139">8</span><span class="sxs-lookup"><span data-stu-id="2d4bf-139">8</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-140">Eine erneute Synchronisierung des Recordsets mit der Datenbank wurde während eines Vorgangs durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-140">An operation resynchronized the <strong>Recordset</strong> with the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-141"><strong>adRsnUndoAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-141"><strong>adRsnUndoAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-142">5</span><span class="sxs-lookup"><span data-stu-id="2d4bf-142">5</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-143">Das Hinzufügen eines neuen Datensatzes wurde während eines Vorgangs rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-143">An operation reversed the addition of a new record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-144"><strong>adRsnUndoDelete</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-144"><strong>adRsnUndoDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-145">6</span><span class="sxs-lookup"><span data-stu-id="2d4bf-145">6</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-146">Das Löschen eines Datensatzes wurde während eines Vorgangs rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-146">An operation reversed the deletion of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-147"><strong>adRsnUndoUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-147"><strong>adRsnUndoUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-148">4</span><span class="sxs-lookup"><span data-stu-id="2d4bf-148">4</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-149">Das Aktualisieren eines Datensatzes wurde während eines Vorgangs rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-149">An operation reversed the update of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-150"><strong>adRsnUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="2d4bf-150"><strong>adRsnUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="2d4bf-151">3</span><span class="sxs-lookup"><span data-stu-id="2d4bf-151">3</span></span></p></td>
<td><p><span data-ttu-id="2d4bf-152">Ein vorhandener Datensatz wurde während eines Vorgangs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-152">An operation updated an existing record.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2d4bf-153">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="2d4bf-153">ADO/WFC equivalent</span></span>

<span data-ttu-id="2d4bf-154">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2d4bf-154">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d4bf-155">Konstante</span><span class="sxs-lookup"><span data-stu-id="2d4bf-155">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-156">AdoEnums. EventReason. ADDNEW</span><span class="sxs-lookup"><span data-stu-id="2d4bf-156">AdoEnums.EventReason.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-157">AdoEnums. EventReason.</span><span class="sxs-lookup"><span data-stu-id="2d4bf-157">AdoEnums.EventReason.CLOSE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-158">AdoEnums. EventReason. DELETE</span><span class="sxs-lookup"><span data-stu-id="2d4bf-158">AdoEnums.EventReason.DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-159">AdoEnums. EventReason. FIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="2d4bf-159">AdoEnums.EventReason.FIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-160">AdoEnums. EventReason. MOVE</span><span class="sxs-lookup"><span data-stu-id="2d4bf-160">AdoEnums.EventReason.MOVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-161">AdoEnums. EventReason. MOVEFIRST</span><span class="sxs-lookup"><span data-stu-id="2d4bf-161">AdoEnums.EventReason.MOVEFIRST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-162">AdoEnums. EventReason. MOVELAST</span><span class="sxs-lookup"><span data-stu-id="2d4bf-162">AdoEnums.EventReason.MOVELAST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-163">AdoEnums. EventReason. MOVENEXT</span><span class="sxs-lookup"><span data-stu-id="2d4bf-163">AdoEnums.EventReason.MOVENEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-164">AdoEnums. EventReason. MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="2d4bf-164">AdoEnums.EventReason.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-165">AdoEnums. EventReason. reQUERY</span><span class="sxs-lookup"><span data-stu-id="2d4bf-165">AdoEnums.EventReason.REQUERY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-166">AdoEnums. EventReason. reSYNCH</span><span class="sxs-lookup"><span data-stu-id="2d4bf-166">AdoEnums.EventReason.RESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-167">AdoEnums. EventReason. UNDOADDNEW</span><span class="sxs-lookup"><span data-stu-id="2d4bf-167">AdoEnums.EventReason.UNDOADDNEW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-168">AdoEnums. EventReason. UNDODELETE</span><span class="sxs-lookup"><span data-stu-id="2d4bf-168">AdoEnums.EventReason.UNDODELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d4bf-169">AdoEnums. EventReason. UNDOUPDATE</span><span class="sxs-lookup"><span data-stu-id="2d4bf-169">AdoEnums.EventReason.UNDOUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d4bf-170">AdoEnums. EventReason. UPDATE</span><span class="sxs-lookup"><span data-stu-id="2d4bf-170">AdoEnums.EventReason.UPDATE</span></span></p></td>
</tr>
</tbody>
</table>

