---
title: CursorDriverEnum-Aufzählung (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bf12758f823d656fd2ca1c8d9e867db5a3392e02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597492"
---
# <a name="cursordriverenum-enumeration-dao"></a>CursorDriverEnum-Aufzählung (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt den Typ des Cursortreibers an.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUseClientBatchCursor</p></td>
<td><p>3</p></td>
<td><p>Verwendet immer die FoxPro-Cursorbibliothek. Diese Option ist für Batchaktualisierungen erforderlich.</p></td>
</tr>
<tr class="even">
<td><p>dbUseDefaultCursor</p></td>
<td><p>-1</p></td>
<td><p>(Standard) Verwendet serverseitige Cursor, wenn diese vom Server unterstützt werden; andernfalls wird die ODBC-Cursorbibliothek verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseNoCursor</p></td>
<td><p>4 </p></td>
<td><p>Öffnet alle Cursor (d. h. <strong>Recordset</strong>-Objekte) als Vorwärtscursor, schreibgeschützt und mit der Rowsetgröße 1. Wird auch als &quot; cursorlose Abfragen bezeichnet.&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1</p></td>
<td><p>Verwendet immer die ODBC-Cursorbibliothek. Diese Option bietet für kleine Resultsets eine bessere Leistung, aber bei umfangreichen Resultsets wird die Leistung schnell beeinträchtigt.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseServerCursor</p></td>
<td><p>2</p></td>
<td><p>Verwendet immer serverseitige Cursor. Für die meisten umfangreichen Vorgänge bietet diese Option eine bessere Leistung; sie kann jedoch mehr Netzwerkverkehr verursachen.</p></td>
</tr>
</tbody>
</table>

