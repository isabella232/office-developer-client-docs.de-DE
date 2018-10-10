---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc02e8cde556a70ca6b2c72f056d218904c31ec2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475686"
---
# <a name="adcpropautorecalcenum"></a>ADCPROP\_AUTORECALC\_ENUM

**Betrifft**: Access 2013 | Office 2013

Gibt an, wann der [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)-Anbieter aggregierte und berechnete Spalten eines hierarchischen Recordsets erneut berechnet.

Diese Konstanten werden nur mit dem **MSDataShape** -Anbieter und das **Recordset-Objekt** "**Auto Recalc**" dynamische-Eigenschaft, die im [Index für dynamische ADO-Eigenschaften](ado-dynamic-property-index.md) verwiesen wird und die in der Microsoft Cursor Service [dokumentiert für OLE verwendet DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) oder [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) -Dokumentation.

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Standardwert. Es wird eine Neuberechnung ausgeführt, sobald der <strong>MSDataShape</strong>-Anbieter festgestellt hat, dass sich Werte geändert haben, von den die berechneten Spalten abhängen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>Berechnung wird lediglich bei zunächst das hierarchische <strong>Recordset-Objekt</strong>zu erstellen.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

