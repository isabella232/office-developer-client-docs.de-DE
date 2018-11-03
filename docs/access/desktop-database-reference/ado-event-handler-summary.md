---
title: Zusammenfassung der ADO-Ereignishandler
TOCTitle: ADO event handler summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d18414793d6a28450dea349e03624ad7aa2537f9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945362"
---
# <a name="ado-event-handler-summary"></a><span data-ttu-id="ab9e7-102">Zusammenfassung über den ADO-Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="ab9e7-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="ab9e7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab9e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab9e7-p101">Ereignisse können von zwei ADO-Objekten ausgelöst werden: [Connection](connection-object-ado.md) und [Recordset](recordset-object-ado.md). Die **ConnectionEvent** -Familie bezieht sich auf Operationen für das **Connection** -Objekt, und die **RecordsetEvent** -Familie bezieht sich auf Operationen für das **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-p101">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object. The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

- <span data-ttu-id="ab9e7-106">**Verbindungsereignisse**: Ereignisse werden ausgegeben, wenn für eine Verbindung eine Transaktion beginnt, ein Commit oder ein Rollback ausgeführt wird, wenn ein [Befehl](command-object-ado.md) ausgeführt wird, wenn während einer **Connection Event** -Operation eine Warnung auftritt oder wenn ein **Connection** -Objekt gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

- <span data-ttu-id="ab9e7-107">**Recordsetereignisse**: Ereignisse werden ausgegeben bei asynchronen Abrufoperationen, sowie wenn Sie durch die Zeilen eines **Recordset** -Objekts navigieren, ein Feld in einer Zeile eines **Recordsets** ändern, eine Zeile in einem **Recordset** ändern, ein **Recordset** mit einem serverseitigen Cursor öffnen, ein **Recordset** schließen oder eine beliebige Änderung im **Recordset** vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="ab9e7-108">Die Ereignisse und ihre Beschreibungen werden in den folgenden Tabellen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab9e7-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="ab9e7-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="ab9e7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab9e7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab9e7-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span><span class="sxs-lookup"><span data-stu-id="ab9e7-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="ab9e7-112"><strong>Verwaltung von Transaktionen</strong> - Benachrichtigung, dass die aktuelle Transaktion für die Verbindung gestartet wurde, ein Commit für sie ausgeführt wurde oder ein Rollback für sie ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab9e7-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, trennen</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-114"><strong>Verwaltung von Verbindungen</strong> - Benachrichtigung, dass die aktuelle Verbindung gestartet wird, gestartet wurde oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab9e7-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-116"><strong>Verwaltung der Befehlsausführung</strong> - Benachrichtigung, dass die Ausführung des aktuellen Befehls für die Verbindung gestartet wird oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab9e7-117"><a href="infomessage-event-ado.md">InfoMessage</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-118"><strong>Informationen</strong> - Benachrichtigung, dass zusätzliche Informationen zur aktuellen Operation vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab9e7-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="ab9e7-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="ab9e7-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab9e7-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab9e7-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-p102"><strong>Abrufstatus</strong> - Benachrichtigung über den Fortschritt einer Datenabrufoperation oder über den Abschluss der Abrufoperation. Diese Ereignisse stehen nur zur Verfügung, wenn das <strong>Recordset</strong>-Objekt mithilfe eines clientseitigen Cursors geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-p102"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed. These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab9e7-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-125"><strong>Verwaltung von Feldänderungen</strong> - Benachrichtigung, dass der Wert des aktuellen Felds geändert wird oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab9e7-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove-, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-127"><strong>Verwaltung der Navigation</strong> - Benachrichtigung, dass die aktuelle Zeilenposition in einem <strong>Recordset</strong>-Objekt geändert wird oder geändert wurde oder dass das Ende des <strong>Recordset</strong>-Objekts erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab9e7-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-129"><strong>Verwaltung von Zeilenänderungen</strong> - Benachrichtigung, dass etwas in der aktuellen Zeile des <strong>Recordset</strong>-Objekts geändert wird oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab9e7-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="ab9e7-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="ab9e7-131"><strong>Verwaltung von Recordsetänderungen</strong> - Benachrichtigung, dass etwas im aktuellen <strong>Recordset</strong>-Objekt geändert wird oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab9e7-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

