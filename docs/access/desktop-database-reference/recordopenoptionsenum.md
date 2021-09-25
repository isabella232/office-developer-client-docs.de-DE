---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e4a348338e66e0d20153c41fb48ab76e1fd0b681
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568544"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Gilt für**: Access 2013, Office 2013

Gibt Optionen zum Öffnen eines [Datensatzes](record-object-ado.md) an. Diese Werte können mit OR kombiniert werden.

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
<td><p><strong>adDelayFetchFields</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Gibt dem Anbieter an, dass die dem <strong>Datensatz</strong> zugeordneten Felder nicht zunächst abgerufen werden müssen, sondern beim ersten Versuch, auf das Feld zuzugreifen, abgerufen werden können. Das Standardverhalten, das durch das Fehlen dieses Kennzeichens angegeben wird, besteht darin, alle <strong>Record-Objektfelder</strong> abzurufen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Gibt dem Anbieter an, dass der dem <strong>Datensatz</strong> zugeordnete Standarddatenstrom anfänglich nicht abgerufen werden muss. Das Standardverhalten, das durch das Fehlen dieses Flags angegeben wird, besteht darin, den Standarddatenstrom abzurufen, der dem <strong>Record -Objekt</strong> zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Gibt an, dass das <strong>Record</strong>-Objekt im asynchronen Modus geöffnet wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Gibt an, dass die Quellzeichenfolge Befehlstext enthält, der ausgeführt werden sollte. Dieser Wert entspricht der <strong>adCmdText</strong>-Option von <strong>Recordset.Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Gibt an, dass keine Optionen angegeben sind.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0x800000</p></td>
<td><p>Wenn die Quelle auf einen Knoten verweist, der ein ausführbares Skript (z. B. eine ASP-Seite) enthält, dann enthält der geöffnete Datensatz die Ergebnisse des ausgeführten Skripts. Dieser Wert ist nur gültig mit Datensätzen, die nicht der Auflistung angehören.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

