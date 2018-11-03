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
# <a name="ado-event-handler-summary"></a>Zusammenfassung über den ADO-Ereignishandler


**Betrifft**: Access 2013, Office 2013

Ereignisse können von zwei ADO-Objekten ausgelöst werden: [Connection](connection-object-ado.md) und [Recordset](recordset-object-ado.md). Die **ConnectionEvent** -Familie bezieht sich auf Operationen für das **Connection** -Objekt, und die **RecordsetEvent** -Familie bezieht sich auf Operationen für das **Recordset** -Objekt.

- **Verbindungsereignisse**: Ereignisse werden ausgegeben, wenn für eine Verbindung eine Transaktion beginnt, ein Commit oder ein Rollback ausgeführt wird, wenn ein [Befehl](command-object-ado.md) ausgeführt wird, wenn während einer **Connection Event** -Operation eine Warnung auftritt oder wenn ein **Connection** -Objekt gestartet oder beendet wird.

- **Recordsetereignisse**: Ereignisse werden ausgegeben bei asynchronen Abrufoperationen, sowie wenn Sie durch die Zeilen eines **Recordset** -Objekts navigieren, ein Feld in einer Zeile eines **Recordsets** ändern, eine Zeile in einem **Recordset** ändern, ein **Recordset** mit einem serverseitigen Cursor öffnen, ein **Recordset** schließen oder eine beliebige Änderung im **Recordset** vornehmen.

Die Ereignisse und ihre Beschreibungen werden in den folgenden Tabellen zusammengefasst.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>Verwaltung von Transaktionen</strong> - Benachrichtigung, dass die aktuelle Transaktion für die Verbindung gestartet wurde, ein Commit für sie ausgeführt wurde oder ein Rollback für sie ausgeführt wurde.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, trennen</a></p></td>
<td><p><strong>Verwaltung von Verbindungen</strong> - Benachrichtigung, dass die aktuelle Verbindung gestartet wird, gestartet wurde oder beendet wurde.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>Verwaltung der Befehlsausführung</strong> - Benachrichtigung, dass die Ausführung des aktuellen Befehls für die Verbindung gestartet wird oder beendet wurde.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Informationen</strong> - Benachrichtigung, dass zusätzliche Informationen zur aktuellen Operation vorhanden sind.</p></td>
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
<th><p>RecordsetEvent</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p><strong>Abrufstatus</strong> - Benachrichtigung über den Fortschritt einer Datenabrufoperation oder über den Abschluss der Abrufoperation. Diese Ereignisse stehen nur zur Verfügung, wenn das <strong>Recordset</strong>-Objekt mithilfe eines clientseitigen Cursors geöffnet wurde.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField FieldChangeComplete</a></p></td>
<td><p><strong>Verwaltung von Feldänderungen</strong> - Benachrichtigung, dass der Wert des aktuellen Felds geändert wird oder geändert wurde.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove-, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p><strong>Verwaltung der Navigation</strong> - Benachrichtigung, dass die aktuelle Zeilenposition in einem <strong>Recordset</strong>-Objekt geändert wird oder geändert wurde oder dass das Ende des <strong>Recordset</strong>-Objekts erreicht ist.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord RecordChangeComplete</a></p></td>
<td><p><strong>Verwaltung von Zeilenänderungen</strong> - Benachrichtigung, dass etwas in der aktuellen Zeile des <strong>Recordset</strong>-Objekts geändert wird oder geändert wurde.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset RecordsetChangeComplete</a></p></td>
<td><p><strong>Verwaltung von Recordsetänderungen</strong> - Benachrichtigung, dass etwas im aktuellen <strong>Recordset</strong>-Objekt geändert wird oder geändert wurde.</p></td>
</tr>
</tbody>
</table>

