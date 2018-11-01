---
title: ActiveX Data Objects (ADO)-Ereignisse
TOCTitle: ADO Events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d7a885d5fdd7736a37c2f195c3bf14b4af8a70d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876232"
---
# <a name="ado-events"></a><span data-ttu-id="2058b-102">ADO-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2058b-102">ADO Events</span></span>


<span data-ttu-id="2058b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2058b-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2058b-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-104"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-105">Wird nach der <strong>BeginTrans</strong>-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2058b-105">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-107">Wird nach der <strong>CommitTrans</strong>-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2058b-107">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-108"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-109">Wird nach dem Starten einer Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2058b-109">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-110"><a href="connectcomplete-and-disconnect-events-ado.md">Verbindung trennen</a></span><span class="sxs-lookup"><span data-stu-id="2058b-110"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-111">Wird nach dem Beenden einer Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2058b-111">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="2058b-112"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-113">Wird aufgerufen beim Versuch, eine Zeile über das Ende des <strong>Recordset</strong>-Objekts hinaus zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="2058b-113">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-114"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-115">Wird aufgerufen, nachdem die Ausführung eines Befehls beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2058b-115">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-116"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-117">Wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das <strong>Recordset</strong>-Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="2058b-117">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="2058b-118"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-119">Wird regelmäßig während einer langen asynchronen Operation aufgerufen, um zu melden, wie viele Zeilen zurzeit in das <strong>Recordset</strong>-Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="2058b-119">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-120"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-121">Wird aufgerufen, nachdem der Wert mindestens eines <strong>Field</strong>-Objekts geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2058b-121">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-122"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="2058b-122"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-123">Wird immer aufgerufen, wenn während einer <strong>ConnectionEvent</strong>-Operation eine Warnung auftritt.</span><span class="sxs-lookup"><span data-stu-id="2058b-123">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-124"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-125">Wird aufgerufen, nachdem die aktuelle Position im <strong>Recordset</strong>-Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2058b-125">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-126"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-127">Wird aufgerufen, nachdem mindestens ein Datensatz geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2058b-127">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-128"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-129">Wird aufgerufen, nachdem das <strong>Recordset</strong>-Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2058b-129">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="2058b-130"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-131">Wird nach der <strong>RollbackTrans</strong>-Operation aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2058b-131">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="2058b-132"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-133">Wird aufgerufen, bevor durch eine ausstehende Operation der Wert mindestens eines <strong>Field</strong>-Objekts im <strong>Recordset</strong>-Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2058b-133">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="2058b-134"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-135">Wird aufgerufen, bevor mindestens ein Datensatz (Zeilen) im <strong>Recordset</strong>-Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2058b-135">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="2058b-136"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-137">Wird aufgerufen, bevor das <strong>Recordset</strong>-Objekt durch eine ausstehende Operation geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2058b-137">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-138"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="2058b-138"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-139">Wird vor dem Starten einer Verbindung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2058b-139">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2058b-140"><a href="willexecute-event-ado.md">WillExecute</a></span><span class="sxs-lookup"><span data-stu-id="2058b-140"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-141">Wird aufgerufen, unmittelbar bevor ein ausstehender Befehl für diese Verbindung ausgeführt wird, und gibt dem Benutzer die Möglichkeit, die Parameter für die ausstehende Ausführung zu überprüfen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2058b-141">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2058b-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="2058b-142"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="2058b-143">Das <strong>WillMove</strong> -Ereignis wird aufgerufen, <em>bevor</em> eine ausstehende Operation geändert, die aktuelle Position im <strong>Recordset-Objekt</strong>.</span><span class="sxs-lookup"><span data-stu-id="2058b-143">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

