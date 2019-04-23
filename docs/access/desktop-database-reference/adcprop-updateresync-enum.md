---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1952d473b51048a271a689498ae844cee761b001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280439"
---
# <a name="adcpropupdateresyncenum"></a>ADCPROP\_-\_UPDATERESYNC-Enumeration

**Gilt für**: Access 2013, Office 2013

Gibt an, ob die [UpdateBatch](updatebatch-method-ado.md)-Methode von einer impliziten [Resync](resync-method-ado.md)-Methodenoperation gefolgt wird. Ist dies der Fall, wird dadurch der Umfang einer solchen Operation festgelegt.

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
<td><p><strong>adResyncAll</strong></p></td>
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
<td><p>Ruft <strong>Resync</strong> für alle erfolgreich eingefügten Zeilen auf. AutoIncrement-Spaltenwerte werden jedoch nicht neu synchronisiert. Stattdessen werden die Inhalte neu eingefügter Zeilen basierend auf dem vorhandenen Primärschlüsselwert neu synchronisiert. Wenn der Primärschlüssel ein AutoIncrement-Wert ist, wird der Inhalt der beabsichtigten Zeile nicht mit <strong>Resync</strong> abgerufen. Rufen Sie für die automatische Inkrementierung von Primärschlüsselwerten <strong>UpdateBatch</strong> mit dem kombinierten Wert <strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>auf.</p></td>
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

