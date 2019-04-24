---
title: QueryDefStateEnum-Aufzählung (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303318"
---
# <a name="querydefstateenum-enumeration-dao"></a>QueryDefStateEnum-Aufzählung (DAO)


**Gilt für**: Access 2013, Office 2013

Hiermit geben Sie zusammen mit der **Prepare**-Eigenschaft die Methode für die Vorbereitung einer Abfrage an.

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
<td><p>dbQPrepare</p></td>
<td><p>1</p></td>
<td><p>(Standard) Die Anweisung wird vorbereitet (d. h. die ODBC-API SQLPrepare wird aufgerufen).</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>2</p></td>
<td><p>Die Anweisung wird nicht vorbereitet (d. h. die ODBC-API SQLExecDirect wird aufgerufen).</p></td>
</tr>
</tbody>
</table>

