---
title: Ereignisse ActiveX Data Objects (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3cc8ac02e2410a2f7bfe1038851e16f50c1ea2ee
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910943"
---
# <a name="ado-events"></a><span data-ttu-id="5e18c-102">ADO-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5e18c-102">ADO events</span></span>

<span data-ttu-id="5e18c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e18c-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="5e18c-104">Ereignis</span><span class="sxs-lookup"><span data-stu-id="5e18c-104">Event</span></span></th>
<th><span data-ttu-id="5e18c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e18c-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-107">Wird nach der <strong>BeginTrans</strong>-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e18c-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-109">Wird nach der <strong>CommitTrans</strong>-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e18c-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-111">Wird nach dem Starten einer Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e18c-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-112"><a href="connectcomplete-and-disconnect-events-ado.md">Verbindung trennen</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-113">Wird nach dem Beenden einer Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e18c-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-115">Wird aufgerufen beim Versuch, eine Zeile über das Ende des <strong>Recordset</strong>-Objekts hinaus zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5e18c-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-117">Wird aufgerufen, nachdem die Ausführung eines Befehls beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5e18c-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-119">Wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das <strong>Recordset</strong>-Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="5e18c-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-121">Wird regelmäßig während einer langen asynchronen Operation aufgerufen, um zu melden, wie viele Zeilen zurzeit in das <strong>Recordset</strong>-Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="5e18c-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-123">Wird aufgerufen, nachdem der Wert mindestens eines <strong>Field</strong>-Objekts geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e18c-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-124"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-125">Wird immer aufgerufen, wenn während einer <strong>ConnectionEvent</strong>-Operation eine Warnung auftritt.</span><span class="sxs-lookup"><span data-stu-id="5e18c-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-127">Wird aufgerufen, nachdem die aktuelle Position im <strong>Recordset</strong>-Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e18c-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-129">Wird aufgerufen, nachdem mindestens ein Datensatz geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e18c-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-131">Wird aufgerufen, nachdem das <strong>Recordset</strong>-Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e18c-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-133">Wird nach der <strong>RollbackTrans</strong>-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e18c-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-135">Wird aufgerufen, bevor durch eine ausstehende Operation der Wert mindestens eines <strong>Field</strong>-Objekts im <strong>Recordset</strong>-Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5e18c-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-137">Wird aufgerufen, bevor mindestens ein Datensatz (Zeilen) im <strong>Recordset</strong>-Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5e18c-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-139">Wird aufgerufen, bevor das <strong>Recordset</strong>-Objekt durch eine ausstehende Operation geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5e18c-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-140"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-141">Wird vor dem Starten einer Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e18c-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e18c-142"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-143">Wird aufgerufen, unmittelbar bevor ein ausstehender Befehl für diese Verbindung ausgeführt wird, und gibt dem Benutzer die Möglichkeit, die Parameter für die ausstehende Ausführung zu überprüfen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5e18c-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e18c-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="5e18c-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="5e18c-145">Das <strong>WillMove</strong> -Ereignis wird aufgerufen, <em>bevor</em> eine ausstehende Operation geändert, die aktuelle Position im <strong>Recordset-Objekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="5e18c-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>