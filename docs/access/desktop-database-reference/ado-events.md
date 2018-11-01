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
# <a name="ado-events"></a>ADO-Ereignisse


**Betrifft**: Access 2013, Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></p></td>
<td><p>Wird nach der <strong>BeginTrans</strong>-Operation aufgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></p></td>
<td><p>Wird nach der <strong>CommitTrans</strong>-Operation aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></p></td>
<td><p>Wird nach dem Starten einer Verbindung aufgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">Verbindung trennen</a></p></td>
<td><p>Wird nach dem Beenden einer Verbindung aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Wird aufgerufen beim Versuch, eine Zeile über das Ende des <strong>Recordset</strong>-Objekts hinaus zu verschieben.</p></td>
</tr>
<tr class="even">
<td><p><a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p>Wird aufgerufen, nachdem die Ausführung eines Befehls beendet wurde.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>Wird aufgerufen, nachdem alle Datensätze in einer langen asynchronen Operation in das <strong>Recordset</strong>-Objekt abgerufen wurden.</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>Wird regelmäßig während einer langen asynchronen Operation aufgerufen, um zu melden, wie viele Zeilen zurzeit in das <strong>Recordset</strong>-Objekt abgerufen wurden.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Wird aufgerufen, nachdem der Wert mindestens eines <strong>Field</strong>-Objekts geändert wurde.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p>Wird immer aufgerufen, wenn während einer <strong>ConnectionEvent</strong>-Operation eine Warnung auftritt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Wird aufgerufen, nachdem die aktuelle Position im <strong>Recordset</strong>-Objekt geändert wurde.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Wird aufgerufen, nachdem mindestens ein Datensatz geändert wurde.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Wird aufgerufen, nachdem das <strong>Recordset</strong>-Objekt geändert wurde.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></p></td>
<td><p>Wird nach der <strong>RollbackTrans</strong>-Operation aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Wird aufgerufen, bevor durch eine ausstehende Operation der Wert mindestens eines <strong>Field</strong>-Objekts im <strong>Recordset</strong>-Objekt geändert wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Wird aufgerufen, bevor mindestens ein Datensatz (Zeilen) im <strong>Recordset</strong>-Objekt geändert wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Wird aufgerufen, bevor das <strong>Recordset</strong>-Objekt durch eine ausstehende Operation geändert wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a></p></td>
<td><p>Wird vor dem Starten einer Verbindung aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a></p></td>
<td><p>Wird aufgerufen, unmittelbar bevor ein ausstehender Befehl für diese Verbindung ausgeführt wird, und gibt dem Benutzer die Möglichkeit, die Parameter für die ausstehende Ausführung zu überprüfen und zu ändern.</p></td>
</tr>
<tr class="even">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>Das <strong>WillMove</strong> -Ereignis wird aufgerufen, <em>bevor</em> eine ausstehende Operation geändert, die aktuelle Position im <strong>Recordset-Objekt</strong>.</p></td>
</tr>
</tbody>
</table>

