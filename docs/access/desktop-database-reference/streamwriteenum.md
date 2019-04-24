---
title: StreamWriteEnum (Access Desktop Database Reference)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308477"
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
<td><p><strong>WriteLine</strong></p></td>
<td><p>1</p></td>
<td><p>Schreibt eine Textzeichenfolge und ein Zeilentrennzeichen in ein <strong>Stream</strong>-Objekt. Wenn keine <a href="lineseparator-property-ado.md">LineSeparator</a>-Eigenschaft definiert ist, wird ein Laufzeitfehler zurückgegeben.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

