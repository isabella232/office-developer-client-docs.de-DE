---
title: QueryDefStateEnum-Aufzählung (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: afed37a05b4598c1f57399162a68f430941d9e93
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558030"
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

