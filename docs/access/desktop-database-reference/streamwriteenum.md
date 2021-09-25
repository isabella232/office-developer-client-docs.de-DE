---
title: StreamWriteEnum (Access-Desktopdatenbankreferenz)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1f5448d697cb7cb6c959bc15ccb05abd7a8de5ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585291"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**Gilt für**: Access 2013, Office 2013

Gibt an, ob der Zeichenfolge, die in ein [Stream](stream-object-ado.md)-Objekt geschrieben wird, ein Zeilentrennzeichen angehängt wird.

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


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

