---
title: CursorTypeEnum (Access Desktop Database Reference)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295163"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Gilt für**: Access 2013, Office 2013

Gibt den in einem [Recordset](recordset-object-ado.md)-Objekt verwendeten Cursortyp an.

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>Verwendet einen dynamischen Cursor. Hinzufügungen, Änderungen und Löschungen von anderen Benutzern sind sichtbar, und alle Arten der Navigation durch das Recordset sind zulässig, mit Ausnahme von Textmarken, falls diese vom Anbieter nicht unterstützt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Standardwert. Verwendet einen Vorwärtscursor. Mit einem statischen Cursor identisch, außer dass Sie in den Datensätzen nur einen Bildlauf vorwärts ausführen können. Wenn Sie nur einen Durchlauf durch ein Recordset ausführen müssen, wird die Leistung dadurch verbessert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Verwendet einen Keysetcursor. Wie bei einem dynamischen Cursor, außer, dass Sie keine Datensätze anzeigen können, die von anderen Benutzern hinzugefügt werden, obwohl die von anderen Benutzern gelöschten Datensätze von Ihrem Recordset aus nicht zugänglich sind. Die Datenänderungen durch andere Benutzer sind weiterhin sichtbar.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Verwendet einen statischen Cursor. Eine statische Kopie einer Datensatzgruppe, die Sie zum Suchen von Daten oder Erstellen von Berichten verwenden können. Hinzufügungen, Änderungen oder Löschvorgänge durch andere Benutzer sind nicht sichtbar.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt keinen Cursortyp an.</p></td>
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
<td><p>AdoEnums. CursorType. DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. CursorType. FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. CursorType. KEYSet</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. CursorType. STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. CursorType. unSPECIFIED</p></td>
</tr>
</tbody>
</table>

