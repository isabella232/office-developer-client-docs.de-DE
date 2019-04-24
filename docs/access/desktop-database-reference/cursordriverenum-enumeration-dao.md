---
title: CursorDriverEnum-Aufzählung (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295247"
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
<td><p>4</p></td>
<td><p>Öffnet alle Cursor (d. h. <strong>Recordset</strong>-Objekte) als Vorwärtscursor, schreibgeschützt und mit der Rowsetgröße 1. Auch als &quot;cursorlos Abfragen bezeichnet.&quot;</p></td>
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

