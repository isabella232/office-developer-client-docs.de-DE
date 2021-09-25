---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 159fc73c68e3da4082533009cf67b7381ea9850b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569482"
---
# <a name="adcprop_autorecalc_enum"></a>ADCPROP \_ \_ AUTORECALC-ENUMERATION

**Gilt für**: Access 2013, Office 2013

Gibt an, wann der [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)-Anbieter aggregierte und berechnete Spalten eines hierarchischen Recordsets erneut berechnet.

Diese Konstanten werden nur mit dem **MSDataShape-Anbieter** und der dynamischen Eigenschaft **"Auto Recalc"** des **Recordset** verwendet, auf die im Index der [dynamischen ADO-Eigenschaft](ado-dynamic-property-index.md) verwiesen wird und in der Dokumentation des [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) oder des Microsoft Data Shaping Service für OLE [DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) dokumentiert ist.

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Standardwert. Es wird eine Neuberechnung ausgeführt, sobald der <strong>MSDataShape</strong>-Anbieter festgestellt hat, dass sich Werte geändert haben, von den die berechneten Spalten abhängen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>Eine Berechnung wird lediglich bei der ersten Erstellung des hierarchischen Recordsets durchgeführt.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

