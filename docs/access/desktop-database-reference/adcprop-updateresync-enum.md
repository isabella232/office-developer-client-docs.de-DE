---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ce8a0555e758cf2f3435de755720f312705ba374
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474497"
---
# <a name="adcpropupdateresyncenum"></a>ADCPROP\_UPDATERESYNC\_ENUM

**Betrifft**: Access 2013 | Office 2013

Gibt an, ob die [UpdateBatch](updatebatch-method-ado.md)-Methode von einer impliziten [Resync](resync-method-ado.md)-Methodenoperation gefolgt wird. Ist dies der Fall, wird dadurch der Umfang einer solchen Operation festgelegt.

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
<td><p><strong>vom Wert adResyncAll</strong></p></td>
<td><p>15</p></td>
<td><p>Ruft <strong>Resync</strong> mit dem kombinierten Wert aller anderen ADCPROP_UPDATERESYNC_ENUM-Elemente auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>Standardwert. Versucht, den neuen Identitätswert für Spalten abzurufen, die von der Datenquelle automatisch erhöht oder generiert werden, wie Microsoft Jet AutoWert-Felder oder Microsoft SQL Server Identity-Spalten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>Ruft <strong>Resync</strong> für alle Zeilen auf, in denen die Aktualisierungs- oder Löschoperation aufgrund eines Parallelitätskonflikts fehlgeschlagen ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8</p></td>
<td><p>Ruft <strong>Resync</strong> für alle erfolgreich eingefügten Zeilen auf. AutoIncrement-Spaltenwerte werden jedoch nicht neu synchronisiert. Stattdessen werden die Inhalte neu eingefügte Zeilen basierend auf der vorhandenen primären Schlüsselwert neu synchronisiert. Wenn der Primärschlüssel ein AutoIncrement-Wert ist, werden nicht den Inhalt der beabsichtigten Zeile <strong>Resync</strong> abgerufen werden. Rufen Sie zur automatischen Erhöhung der AutoIncrement Werte Primärschlüssel, <strong>UpdateBatch</strong> mit dem kombinierten Wert <strong>AdResyncAutoIncrement</strong> + <strong>AdResyncInserts</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>Ruft <strong>Resync</strong> nicht auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>Ruft <strong>Resync</strong> für alle erfolgreich aktualisierten Zeilen auf.</p></td>
</tr>
</tbody>
</table>

