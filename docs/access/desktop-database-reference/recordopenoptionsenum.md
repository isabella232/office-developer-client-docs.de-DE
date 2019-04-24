---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300686"
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
<td><p>0X8000</p></td>
<td><p>Gibt an, dass der Anbieter die mit dem <strong>Datensatz</strong> verknüpften Felder nicht anfänglich abgerufen werden muss, aber beim ersten Zugriff auf das Feld abgerufen werden kann. Das Standardverhalten, das durch das Fehlen dieses Flags angegeben wird, besteht darin, alle <strong>Record</strong> -Objektfelder abzurufen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Gibt dem Anbieter an, dass der dem <strong>Datensatz</strong> zugeordnete Standarddatenstrom nicht anfänglich abgerufen werden muss. Das Standardverhalten, das durch das Fehlen dieses Flags angegeben wird, besteht darin, den Standarddatenstrom abzurufen, der dem <strong>Record</strong> -Objekt zugeordnet ist.</p></td>
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


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

