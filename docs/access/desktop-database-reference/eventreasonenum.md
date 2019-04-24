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
# <a name="eventreasonenum"></a>EventReasonEnum

**Gilt für**: Access 2013, Office 2013

Gibt den Grund an, der zu einem Ereignis führte.

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
<td><p><strong>adRsnAddNew</strong></p></td>
<td><p>1</p></td>
<td><p>Ein neuer Datensatz wurde während eines Vorgangs hinzugefügt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnClose</strong></p></td>
<td><p>9</p></td>
<td><p>Das Recordset wurde während eines Vorgangs geschlossen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnDelete</strong></p></td>
<td><p>2</p></td>
<td><p>Ein Datensatz wurde während eines Vorgangs gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnFirstChange</strong></p></td>
<td><p>11</p></td>
<td><p>Ein Datensatz wurde während eines Vorgangs erstmalig geändert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMove</strong></p></td>
<td><p>10</p></td>
<td><p>Der Datensatzzeiger wurde während eines Vorgangs innerhalb des Recordsets bewegt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveFirst</strong></p></td>
<td><p>12</p></td>
<td><p>Der Datensatzzeiger wurde während eines Vorgangs zum ersten Datensatz im Recordset verschoben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMoveLast</strong></p></td>
<td><p>15</p></td>
<td><p>Der Datensatzzeiger wurde während eines Vorgangs zum letzten Datensatz im Recordset verschoben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveNext</strong></p></td>
<td><p>13</p></td>
<td><p>Der Datensatzzeiger wurde während eines Vorgangs zum nächsten Datensatz im Recordset verschoben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMovePrevious</strong></p></td>
<td><p>14</p></td>
<td><p>Der Datensatzzeiger wurde während eines Vorgangs zum vorherigen Datensatz im Recordset verschoben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnRequery</strong></p></td>
<td><p>7</p></td>
<td><p>Das <a href="recordset-object-ado.md">Recordset</a> wurde während eines Vorgangs erneut abgefragt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnResynch</strong></p></td>
<td><p>8</p></td>
<td><p>Eine erneute Synchronisierung des Recordsets mit der Datenbank wurde während eines Vorgangs durchgeführt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoAddNew</strong></p></td>
<td><p>5</p></td>
<td><p>Das Hinzufügen eines neuen Datensatzes wurde während eines Vorgangs rückgängig gemacht.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUndoDelete</strong></p></td>
<td><p>6</p></td>
<td><p>Das Löschen eines Datensatzes wurde während eines Vorgangs rückgängig gemacht.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoUpdate</strong></p></td>
<td><p>4</p></td>
<td><p>Das Aktualisieren eines Datensatzes wurde während eines Vorgangs rückgängig gemacht.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUpdate</strong></p></td>
<td><p>3</p></td>
<td><p>Ein vorhandener Datensatz wurde während eines Vorgangs aktualisiert.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

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
<td><p>AdoEnums. EventReason. ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason.</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. DELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. FIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. MOVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. MOVEFIRST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. MOVELAST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. MOVENEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. reQUERY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. reSYNCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. UNDOADDNEW</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. UNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. EventReason. UNDOUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. EventReason. UPDATE</p></td>
</tr>
</tbody>
</table>

