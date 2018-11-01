---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c39d9ca7da2955343e38c67628c9c603a2c256b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869806"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Betrifft**: Access 2013, Office 2013

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
<td><p>0 x 8000</p></td>
<td><p>Der Anbieter zeigt, dass die Felder, die dem <strong>Eintrag</strong> zugeordnete zunächst nicht abgerufen werden müssen, aber beim ersten Versuch Zugriff auf das Feld abgerufen werden können. Das Standardverhalten, durch die Abwesenheit dieses Flags ist die <strong>Datensatz</strong> -Objektfelder abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Der Anbieter zeigt, dass der dem <strong>Eintrag</strong> zugeordnete Standarddatenstrom zunächst nicht abgerufen werden muss. Das Standardverhalten, durch die Abwesenheit dieses Flags ist abzurufenden den Standarddatenstrom das <strong>Record</strong> -Objekt zugeordnet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Gibt an, dass das <strong>Record</strong>-Objekt im asynchronen Modus geöffnet wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Gibt an, dass die Quellzeichenfolge Befehlstext enthält, der ausgeführt werden sollte. Dieser Wert entspricht der <strong>adCmdText</strong>-Option von <strong>Recordset.Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Gibt an, dass keine Optionen angegeben sind.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0 x 800000</p></td>
<td><p>Gibt an, dass, wenn die Datenquelle an einen Knoten verweist, der ein ausführbares Skript enthält (z. B. ein. ASP-Seite), und klicken Sie dann die geöffnete <strong>Datensatz</strong> die Ergebnisse des ausgeführten Skripts enthalten soll. Dieser Wert ist nur gültig, wenn nicht der Auflistung Datensätze.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

