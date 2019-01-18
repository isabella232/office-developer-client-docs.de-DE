---
title: IsolationLevelEnum (Access PC-Datenbank-Referenz)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707186"
---
# <a name="isolationlevelenum"></a>IsolationLevelEnum

**Betrifft**: Access 2013, Office 2013

Gibt die Transaktionsisolation für ein [Connection](connection-object-ado.md)-Objekt an.

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
<td><p><strong>adXactUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt an, dass der Provider nicht die angegebene, sondern eine andere Isolationsstufe verwendet, diese Stufe jedoch nicht ermittelt werden kann.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactChaos</strong></p></td>
<td><p>16</p></td>
<td><p>Gibt an, dass die ausstehenden Änderungen aus isolierteren Transaktionen nicht überschrieben werden können.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactBrowse</strong></p></td>
<td><p>256</p></td>
<td><p>Gibt an, dass Sie nicht gespeicherte Änderungen einer Transaktion in anderen Transaktionen anzeigen können.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadUncommitted</strong></p></td>
<td><p>256</p></td>
<td><p>Entspricht <strong>adXactBrowse</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactCursorStability</strong></p></td>
<td><p>4096</p></td>
<td><p>Gibt an, dass Sie Änderungen einer Transaktion in anderen Transaktionen anzeigen können, nachdem sie gespeichert wurden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadCommitted</strong></p></td>
<td><p>4096</p></td>
<td><p>Entspricht <strong>adXactCursorStability</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactRepeatableRead</strong></p></td>
<td><p>65536</p></td>
<td><p>Gibt an, dass Sie von einer Transaktion keine Änderungen, die in anderen Transaktionen vorgenommen wurden, anzeigen können, aber dass durch erneutes Abfragen neue <strong>Recordset</strong>-Objekte abgerufen werden können.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactIsolated</strong></p></td>
<td><p>1048576</p></td>
<td><p>Gibt an, dass Transaktionen in Isolierung anderer Transaktionen durchgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactSerializable</strong></p></td>
<td><p>1048576</p></td>
<td><p>Entspricht <strong>adXactIsolated</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.CHAOS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.BROWSE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READUNCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.CURSORSTABILITY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.REPEATABLEREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.ISOLATED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.SERIALIZABLE</p></td>
</tr>
</tbody>
</table>

