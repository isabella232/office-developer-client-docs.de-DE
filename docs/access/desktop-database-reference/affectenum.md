---
title: AffectEnum (Access Desktop Database Reference)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297200"
---
# <a name="affectenum"></a>AffectEnum

**Gilt für**: Access 2013, Office 2013

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
<td><p>Wenn kein <a href="filter-property-ado.md">Filter</a> auf das <strong>Recordset</strong>angewendet wird, wirkt sich dies auf alle Datensätze aus. Wenn die <strong>Filter</strong> -Eigenschaft auf eine Zeichenfolge (beispielsweise &quot;Author = ' Smith '&quot;) festgelegt ist, wirkt sich die Operation auf sichtbare Datensätze im aktuellen Kapitel aus. Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wirkt sich die Operation auf alle Zeilen des <strong>Recordset-Objekts</strong>aus.</p><p><strong>Hinweis</strong>: adAffectAll ist im Visual Basic-Objekt Browser ausgeblendet.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4</p></td>
<td><p>Wirkt sich auf alle Datensätze in allen nebengeordneten Kapiteln des <strong>Recordset-Objekts</strong>aus, einschließlich derer, die nicht über einen <strong>Filter</strong> angezeigt werden, der derzeit angewendet wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>Wirkt sich lediglich auf den aktuellen Datensatz aus.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>Betrifft nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a>-Eigenschaft erfüllen. Sie müssen die <strong>Filter</strong> -Eigenschaft auf einen <strong>FilterGroupEnum</strong> -Wert oder ein Array von <strong>Textmarken</strong> festlegen, um diese Option zu verwenden.</p></td>
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
<td><p>AdoEnums. affect. ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. affect. allCHAPTERs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. affect. CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. affect. GROUP</p></td>
</tr>
</tbody>
</table>

