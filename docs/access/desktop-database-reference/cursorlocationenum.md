---
title: CursorLocationEnum (Access Desktop Database Reference)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295212"
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
<td><p>Verwendet clientseitige Cursor, die von einer lokalen Cursorbibliothek bereitgestellt werden. Lokale Cursor Dienste ermöglichen häufig viele Features, die von vom Treiber bereitgestellten Cursorn möglicherweise nicht verwendet werden, sodass die Verwendung dieser Einstellung für Features, die aktiviert werden, einen Vorteil bieten kann. Aus Gründen der Abwärtskompatibilität wird auch das Synonym <strong>adUseClientBatch</strong> unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Verwendet keine Cursordienste. (Diese Konstante ist veraltet und wird ausschließlich zur Abwärtskompatibilität angezeigt.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Standardwert. Verwendet Datenanbieter oder vom Treiber bereitgestellte Cursor. Diese Cursor sind manchmal sehr flexibel und ermöglichen eine zusätzliche Vertraulichkeit für andere Änderungen an der Datenquelle. Einige Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor-Diensts für OLE DB</a> (beispielsweise nicht zugeordnete <a href="recordset-object-ado.md">Recordset</a> -Objekte) können jedoch nicht mit serverseitigen Cursorn simuliert werden, und diese Funktionen sind bei dieser Einstellung nicht verfügbar.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

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
<td><p>AdoEnums. CursorLocation. CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. CursorLocation. NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. CursorLocation. SERVER</p></td>
</tr>
</tbody>
</table>

