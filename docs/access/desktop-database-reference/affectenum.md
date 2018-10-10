---
title: AffectEnum (Access PC-Datenbank-Referenz)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ffb2ab2abbd24a19ddc433b5fd315dd535fd2a0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473880"
---
# <a name="affectenum"></a>AffectEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, welche Datensätze von einer Operation betroffen sind.

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
<td><p>Wenn Sie nicht, dass ein <a href="filter-property-ado.md">Filter</a> für das <strong>Recordset-Objekt</strong>angewendet wird, wirkt sich auf alle Datensätze. Wenn die <strong>Filter</strong> -Eigenschaft auf ein zeichenfolgenkriterium festgelegt ist (wie &quot;Author = 'Smith'&quot;), und klicken Sie dann der Vorgang sichtbaren Datensätze im aktuellen Kapitel auswirkt. Wenn die <strong>Filter</strong> -Eigenschaft auf ein Element von <a href="filtergroupenum.md">FilterGroupEnum</a> oder ein Array von Lesezeichen festgelegt ist, wird der Vorgang alle Zeilen des <strong>Recordsets</strong>beeinflusst.</p>

> [!NOTE]
> <P>AdAffectAll ist im Objektbrowser von Visual Basic ausgeblendet.</P>


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

