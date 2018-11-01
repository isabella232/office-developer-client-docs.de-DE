---
title: ExecuteOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8fa81d535a10aa0f359ba6e03b0f47048713671f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867853"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Betrifft**: Access 2013, Office 2013

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
<td><p>0 x 10</p></td>
<td><p>Gibt an, dass der Befehl asynchron ausgeführt werden soll.
 Dieser Wert kann nicht mit dem <a href="commandtypeenum.md">ExecuteOptionEnum</a>-Wert <strong>adAsyncExecute</strong> kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0 x 20</p></td>
<td><p>Gibt an, dass die verbleibenden Zeilen nach der ersten, in der <a href="cachesize-property-ado.md">CacheSize</a>-Eigenschaft angegebenen Menge asynchron abgerufen werden sollten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0 x 40</p></td>
<td><p>Gibt an, dass der Hauptthread beim Abrufen nie blockiert. Wenn die angeforderte Zeile nicht abgerufen worden ist, wird die aktuelle Zeile automatisch an das Ende der Datei verschoben.
</p><p>Wenn Sie ein <a href="recordset-object-ado.md">Recordset-Objekt</a> aus einem <a href="stream-object-ado.md">Stream</a> , der ein dauerhaft gespeichertes <strong>Recordset</strong>enthält öffnen, wird <strong>AdAsyncFetchNonBlocking</strong> keinen Einfluss; der Vorgang wird synchron und blockiert werden. <strong>AdAsynchFetchNonBlocking</strong> hat keine Auswirkung, wenn die <a href="commandtypeenum.md">AdCmdTableDirect</a> -Option zum Öffnen des <strong>Recordset-Objekt</strong>verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0 x 80</p></td>
<td><p>Gibt an, dass der Befehlstext ist, einen Befehl oder eine gespeicherte Prozedur, der gibt keine Zeilen (beispielsweise einen Befehl, der nur Daten einfügt) zurück. Wenn alle Zeilen abgerufen werden, werden sie verworfen und nicht zurückgegeben. <strong>AdExecuteNoRecords</strong> kann nur als optionaler Parameter an die <strong>Command-</strong> oder <strong>Connection</strong> <strong>Execute</strong> -Methode übergeben werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0 x 400</p></td>
<td><p>Gibt an, dass die Ergebnisse einer Befehlsausführung als Datenstrom zurückgegeben werden sollten.
 <strong>AdExecuteStream</strong> können nur als optionaler Parameter an den <strong>Befehl</strong> <strong>Execute</strong> -Methode übergeben werden.</p></td>
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

