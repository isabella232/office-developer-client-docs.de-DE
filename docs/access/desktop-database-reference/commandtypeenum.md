---
title: CommandTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cc5fee66746270f5ba8ee851010c6860cfc9e791
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861064"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**Betrifft**: Access 2013 | Office 2013

Gibt an, wie ein Befehlsargument interpretiert werden sollte.

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
<td><p><strong>adCmdUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt kein Befehlstypargument an.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1</p></td>
<td><p>Wertet <a href="commandtext-property-ado.md">CommandText</a> als Textdefinition eines Befehls oder eines gespeicherter Prozeduraufrufs aus.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTable</strong></p></td>
<td><p>2</p></td>
<td><p>Wertet <strong>CommandText</strong> als Namen einer Tabelle aus, deren Spalten alle von einer intern generierten SQL-Abfrage zurückgegeben werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdStoredProc fest</strong></p></td>
<td><p>4</p></td>
<td><p>Wertet <strong>CommandText</strong> als Namen einer gespeicherten Prozedur aus.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8</p></td>
<td><p>Standardwert. Gibt an, dass der Befehlstyp in der <strong>CommandText</strong>-Eigenschaft unbekannt ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p>Wertet <strong>CommandText</strong> als Dateinamen eines dauerhaft gespeicherten <a href="recordset-object-ado.md">Recordsets</a> aus. Wird lediglich mit <strong>Recordset. </strong><a href="open-method-ado-recordset.md">Open</a> oder <a href="requery-method-ado.md">Requery</a> verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p>Wertet <strong>CommandText</strong> als Namen einer Tabelle, deren Spalten alle zurückgegeben werden. Nur verwendet mit <strong>"Recordset.Open"</strong> oder <strong>Requery</strong> . Um die <a href="seek-method-ado.md">Seek</a> -Methode verwenden, muss das <strong>Recordset</strong> mit <strong>AdCmdTableDirect</strong>geöffnet werden. Dieser Wert kann nicht mit dem <a href="executeoptionenum.md">ExecuteOptionEnum</a>-Wert <strong>adAsyncExecute</strong> kombiniert werden.</p></td>
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
<td><p>AdoEnums.CommandType.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.TEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.STOREDPROC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.FILE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

