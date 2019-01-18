---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721220"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**Betrifft**: Access 2013, Office 2013

Gibt Optionen an, um ein [Stream](stream-object-ado.md)-Objekt zu öffnen. Die Werte können mit einer OR-Operation kombiniert werden.

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
<td><p><strong>adOpenStreamAsync</strong></p></td>
<td><p>1</p></td>
<td><p>Öffnet das <strong>Stream</strong>-Objekt im asynchronen Modus.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStreamFromRecord</strong></p></td>
<td><p>4</p></td>
<td><p>Identifiziert den Inhalt des <em>Source</em>-Parameters als bereits geöffnetes <a href="record-object-ado.md">Record</a>-Objekt. Das Standardverhalten besteht darin, die <em>Quelle</em> als eine URL zu behandeln, die direkt auf einen Knoten in einer Baumstruktur verweist. Der diesem Knoten zugeordnete Standarddatenstrom wird geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenStreamUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Gibt das Öffnen des <strong>Stream</strong>-Objekts mit Standardoptionen an.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

