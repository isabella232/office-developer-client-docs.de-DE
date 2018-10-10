---
title: CursorLocationEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474012"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum


**Betrifft**: Access 2013 | Office 2013

Gibt den Speicherort des Cursordiensts an.

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
<td><p>Clientseitige Cursor von einer lokalen Cursorbibliothek bereitgestellt wird, verwendet. Lokale Cursor Services ermöglichen häufig viele Funktionen, die Treiber bereitgestellten Cursor möglicherweise nicht so mit dieser Einstellung Vorteil in Bezug auf Funktionen bereitstellen kann, die aktiviert werden sollen. Für die Abwärtskompatibilität wird das Synonym <strong>AdUseClientBatch</strong> ebenfalls unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Verwendet keine Cursordienste. (Diese Konstante ist veraltet und wird ausschließlich zur Abwärtskompatibilität angezeigt.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Standardwert. Verwendet Datenanbieter- oder treiberbasierte Cursor. Diese Cursor sind manchmal sehr flexibel und ermöglichen eine zusätzliche Unterscheidung von Änderungen, die andere Personen an der Datenquelle vornehmen. Andere Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service für OLE DB</a> (wie z. B. entkoppelte <a href="recordset-object-ado.md">Recordset</a>-Objekte) können nicht mit serverseitigen Cursorn simuliert werden. Diese Features stehen mit dieser Einstellung nicht zur Verfügung.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

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

