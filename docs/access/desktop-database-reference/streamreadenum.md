---
title: StreamReadEnum (Access-Desktopdatenbankreferenz)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f7387ad6762d3beb9d5573c8ae67956b8a84545b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601709"
---
# <a name="streamreadenum"></a>StreamReadEnum

**Gilt für**: Access 2013, Office 2013

Gibt an, ob der gesamte Datenstrom oder die nächste Zeile aus einem [Stream](stream-object-ado.md)-Objekt gelesen werden sollte.

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
<td><p><strong>adReadAll</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Liest alle Bytes aus dem Datenstrom, von der aktuellen Position bis zur <a href="eos-property-ado.md">EOS</a>-Markierung. Dies ist der einzige gültige <strong>StreamReadEnum</strong>-Wert mit binären Datenströmen (<a href="type-property-ado-stream.md">Typ</a> ist <strong>adTypeBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adReadLine</strong></p></td>
<td><p>-2</p></td>
<td><p>Liest die nächste Zeile aus dem Datenstrom (angegeben durch die <a href="lineseparator-property-ado.md">LineSeparator</a>-Eigenschaft).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

