---
title: IsolationLevelEnum (Access-Desktopdatenbankreferenz)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a54f82a61605700d6691f4adc321114994b9e4a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568873"
---
# <a name="isolationlevelenum"></a>IsolationLevelEnum

**Gilt für**: Access 2013, Office 2013

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
<td><p>16 </p></td>
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
<td><p><strong>adXactCursorStabilität</strong></p></td>
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
<td><p>AdoEnums.IsolationLevel.CSV</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.BROWSE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READUNCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.CURSORSTABIL</p></td>
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

