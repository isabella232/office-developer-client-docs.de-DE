---
title: AffectEnum (Access-Desktopdatenbankreferenz)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2a212a7d29ab3f2dc0f6d9910dc369e1ff354f9b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607479"
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
<td><p>Wenn kein <a href="filter-property-ado.md">Filter</a> auf das <strong>Recordset</strong>angewendet wird, wirkt sich dies auf alle Datensätze aus. Wenn die <strong>Filter-Eigenschaft</strong> auf ein Zeichenfolgenkriterium festgelegt ist (z. &quot; B. Author='Smith' &quot; ), wirkt sich der Vorgang auf sichtbare Datensätze im aktuellen Kapitel aus. Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element der <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wirkt sich der Vorgang auf alle Zeilen des <strong>Recordset -Objekts</strong>aus.</p><p><strong>HINWEIS:</strong>adAffectAll ist im Visual Basic Objektbrowser ausgeblendet.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4 </p></td>
<td><p>Wirkt sich auf alle Datensätze in allen gleichgeordneten Kapiteln des <strong>Recordsets</strong>aus, einschließlich derer, die derzeit nicht über einen <strong>angewendeten Filter</strong> sichtbar sind.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>Wirkt sich lediglich auf den aktuellen Datensatz aus.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>Betrifft nur Datensätze, die die aktuelle Einstellung der <a href="filter-property-ado.md">Filter</a>-Eigenschaft erfüllen. Sie müssen die <strong>Filter-Eigenschaft</strong> auf einen <strong>FilterGroupEnum-Wert</strong> oder ein Array von <strong>Lesezeichen</strong> festlegen, um diese Option zu verwenden.</p></td>
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

