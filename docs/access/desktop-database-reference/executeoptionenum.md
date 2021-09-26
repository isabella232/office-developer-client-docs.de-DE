---
title: ExecuteOptionEnum (Access-Desktopdatenbankreferenz)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c2cdd7628e2c5116f92d63c5aae008a19577fec1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612176"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Gilt für**: Access 2013, Office 2013

Gibt an, wie ein Anbieter einen Befehl ausführen sollte.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0x10</p></td>
<td><p>Gibt an, dass der Befehl asynchron ausgeführt werden soll. Dieser Wert kann nicht mit dem <a href="commandtypeenum.md">ExecuteOptionEnum</a>-Wert <strong>adAsyncExecute</strong> kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p>Gibt an, dass die verbleibenden Zeilen nach der ersten, in der <a href="cachesize-property-ado.md">CacheSize</a>-Eigenschaft angegebenen Menge asynchron abgerufen werden sollten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>Gibt an, dass der Hauptthread beim Abrufen nie blockiert. Wenn die angeforderte Zeile nicht abgerufen worden ist, wird die aktuelle Zeile automatisch an das Ende der Datei verschoben.
</p><p>Wenn Sie ein <a href="recordset-object-ado.md">Recordset</a> aus einem <a href="stream-object-ado.md">Stream</a> öffnen, das ein dauerhaft gespeichertes <strong>Recordset</strong>enthält, hat <strong>adAsyncFetchNonBlocking</strong> keine Auswirkung. Der Vorgang ist synchron und blockiert. <strong>adAsynchFetchNonBlocking</strong> hat keine Auswirkung, wenn die <a href="commandtypeenum.md">Option adCmdTableDirect</a> zum Öffnen des <strong>Recordset</strong>-Objekts verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>Zeigt an, dass der Befehlstext ein Befehl oder eine gespeicherte Prozedur ist, der keine Zeilen zurückgibt (beispielsweise ein Befehl, der nur Daten einfügt). Wenn alle Zeilen abgerufen werden, werden sie verworfen und nicht zurückgegeben. <strong>adExecuteNoRecords</strong> kann nur als optionaler Parameter an die <strong>Command-</strong> oder <strong>Connection</strong> <strong>Execute-Methode</strong> übergeben werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0x400</p></td>
<td><p>Gibt an, dass die Ergebnisse einer Befehlsausführung als Datenstrom zurückgegeben werden sollten. <strong>adExecuteStream</strong> kann nur als optionaler Parameter an die <strong>Command</strong> <strong>Execute-Methode</strong> übergeben werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p>Gibt an, dass <strong>CommandText</strong> ein Befehl oder eine gespeicherte Prozedur ist, der bzw. die eine einzelne Zeile zurückgibt, die als <strong>Record</strong>-Objekt zurückgegeben werden sollte.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOptionUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt an, dass der Befehl nicht festgelegt ist.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

