---
title: StreamWriteEnum (Access PC-Datenbank-Referenz)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f58b5173a1208812a6eb9fd06b5f4a414de21ddd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473691"
---
# <a name="streamwriteenum"></a>StreamWriteEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob der Zeichenfolge, die in ein [Stream](stream-object-ado.md)-Objekt geschrieben wird, ein Zeilentrennzeichen angehängt wird.

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
<td><p><strong>adWriteChar</strong></p></td>
<td><p>0</p></td>
<td><p>Standardwert. Schreibt die angegebene Zeichenfolge (die vom <em>Data</em>-Parameter angegeben wird) in das <strong>Stream</strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1</p></td>
<td><p>Schreibt eine Textzeichenfolge und ein Zeilentrennzeichen in ein <strong>Stream</strong>-Objekt. Wenn keine <a href="lineseparator-property-ado.md">LineSeparator</a>-Eigenschaft definiert ist, wird ein Laufzeitfehler zurückgegeben.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

