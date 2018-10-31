---
title: AffectEnum (Access PC-Datenbank-Referenz)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9e1bd4d86e6e269c9363daca0ffa7b8df6303326
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863668"
---
# <a name="affectenum"></a>AffectEnum

**Betrifft**: Access 2013 | Office 2013

Gibt an, welche Datensätze von einer Operation betroffen sind.

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
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3</p></td>
<td><p>Wenn Sie nicht, dass ein <a href="filter-property-ado.md">Filter</a> für das <strong>Recordset-Objekt</strong>angewendet wird, wirkt sich auf alle Datensätze. Wenn die <strong>Filter</strong> -Eigenschaft auf ein zeichenfolgenkriterium festgelegt ist (wie &quot;Author = 'Smith'&quot;), der Vorgang wirkt sich auf die sichtbaren Datensätze im aktuellen Kapitel. Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wirkt sich die Operation alle Zeilen des <strong>Recordset-Objekts</strong>.</p>
<p><strong>Hinweis</strong>: AdAffectAll ist im Objektbrowser von Visual Basic ausgeblendet.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4</p></td>
<td><p>Wirkt sich auf alle Datensätze in allen gleichgeordneten Kapiteln des <strong>Recordset-Objekts</strong>, einschließlich derjenigen, die über keinen der <strong>Filter</strong> , die momentan angewendet ist nicht sichtbar.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>Wirkt sich lediglich auf den aktuellen Datensatz aus.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>Wirkt sich auf nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a> -Eigenschaft zu erfüllen. Sie müssen die <strong>Filter</strong> -Eigenschaft auf ein <strong>FilterGroupEnum</strong> -Wert oder ein Array von <strong>Lesezeichen</strong> verwenden Sie diese Option festlegen.</p></td>
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
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

