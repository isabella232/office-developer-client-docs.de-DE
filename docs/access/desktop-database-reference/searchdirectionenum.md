---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f9fdf9dd5908b65ae3b6f6ce5a44eba07e4d9bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308806"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum


**Gilt für**: Access 2013, Office 2013

Gibt die Richtung einer Datensatzsuche innerhalb eines [Recordsets](recordset-object-ado.md) an.

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
<td><p><strong>adSearchBackward</strong></p></td>
<td><p>-1</p></td>
<td><p>Sucht rückwärts und hält am Anfang des Recordset- <strong>Objekts</strong>. Wenn keine Übereinstimmung gefunden wird, wird der Datensatzzeiger an <a href="bof-eof-properties-ado.md">BOF</a>positioniert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSearchForward</strong></p></td>
<td><p>1</p></td>
<td><p>Sucht nach vorn und beendet am Ende des <strong>Recordset-Objekts</strong>. Wenn keine Übereinstimmung gefunden wird, wird der Datensatzzeiger am <a href="bof-eof-properties-ado.md">EOF</a>positioniert.</p></td>
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
<td><p>AdoEnums. SearchDirection. rückwärts</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. SearchDirection. FORWARD</p></td>
</tr>
</tbody>
</table>

