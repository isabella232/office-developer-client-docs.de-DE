---
title: PositionEnum (Access PC-Datenbank-Referenz)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c791cbd31e346eef5ab8503cb55b0dec5e9fbbc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702838"
---
# <a name="positionenum"></a>PositionEnum

**Betrifft**: Access 2013, Office 2013

Gibt die aktuelle Position des Datensatzzeigers innerhalb eines [Recordsets](recordset-object-ado.md) an.

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
<td><p><strong>adPosBOF</strong></p></td>
<td><p>-2</p></td>
<td><p>Gibt an, dass der aktuelle Datensatzzeiger bei BOF liegt (das heißt, die <a href="bof-eof-properties-ado.md">BOF</a>-Eigenschaft lautet <strong>Wahr</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPosEOF</strong></p></td>
<td><p>-3</p></td>
<td><p>Gibt an, dass der aktuelle Datensatzzeiger bei EOF liegt (das heißt, die <a href="bof-eof-properties-ado.md">EOF</a>-Eigenschaft lautet <strong>Wahr</strong>).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPosUnknown</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt an, dass das <strong>Recordset</strong> leer ist, die aktuelle Position unbekannt ist oder der Anbieter nicht die <a href="absolutepage-property-ado.md">AbsolutePage-</a> oder <a href="absoluteposition-property-ado.md">AbsolutePosition</a> -Eigenschaft.</p></td>
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
<td><p>AdoEnums.Position.BOF</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Position.EOF</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Position.UNKNOWN</p></td>
</tr>
</tbody>
</table>

