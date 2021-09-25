---
title: CursorLocationEnum (Access-Desktopdatenbankreferenz)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d81a086e2ead45dbc56f5be5f24ba8bf5937f7a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615634"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Gilt für**: Access 2013, Office 2013

Gibt den Speicherort des Cursordiensts an.

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
<td><p><strong>adUseClient</strong></p></td>
<td><p>3</p></td>
<td><p>Verwendet clientseitige Cursor, die von einer lokalen Cursorbibliothek bereitgestellt werden. Lokale Cursordienste lassen häufig viele Features zu, die von Treibern bereitgestellte Cursor möglicherweise nicht haben. Daher bietet die Verwendung dieser Einstellung möglicherweise einen Vorteil im Hinblick auf aktivierte Features. Aus Gründen der Abwärtskompatibilität wird auch das Synonym <strong>"adUseClientBatch"</strong> unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Verwendet keine Cursordienste. (Diese Konstante ist veraltet und wird ausschließlich zur Abwärtskompatibilität angezeigt.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Standard. Verwendet vom Datenanbieter oder Treiber bereitgestellte Cursor. Diese Cursor sind manchmal sehr flexibel und ermöglichen eine zusätzliche Vertraulichkeit für Änderungen, die andere an der Datenquelle vornehmen. Einige Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service für OLE DB</a> (z. B. nicht zugeordnete <a href="recordset-object-ado.md">Recordset-Objekte)</a> können jedoch nicht mit serverseitigen Cursorn simuliert werden, und diese Features sind mit dieser Einstellung nicht verfügbar.</p></td>
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
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

