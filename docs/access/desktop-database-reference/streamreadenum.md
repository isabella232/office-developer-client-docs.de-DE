---
title: StreamReadEnum (Access PC-Datenbank-Referenz)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1255f691f2cd0bde1e3ed83ebffc1f0d31fb3119
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474693"
---
# <a name="streamreadenum"></a>StreamReadEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob der gesamte Datenstrom oder die nächste Zeile aus einem [Stream](stream-object-ado.md)-Objekt gelesen werden sollte.

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


**ADO/WFC-Entsprechung**

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

