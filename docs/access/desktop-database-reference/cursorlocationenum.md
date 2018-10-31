---
title: CursorLocationEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863631"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Betrifft**: Access 2013 | Office 2013

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
<td><p>Standard. Verwendet vom Datenanbieter oder Treiber bereitgestellte Cursor. Diese Cursor sind in einigen Fällen sehr flexibel und zusätzliche Empfindlichkeit gegenüber Änderungen, die andere Personen an der Datenquelle ermöglichen. Jedoch einige Features des <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service für OLE DB</a> (beispielsweise nicht verbundenes <a href="recordset-object-ado.md">Recordset</a> -Objekte) können nicht mit serverseitigen Cursorn simuliert werden, und diese Funktionen werden mit dieser Einstellung nicht verfügbar sein.</p></td>
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

