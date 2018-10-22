---
title: UpdateTypeEnum Enumeration (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ee8638d6fdade7e6955613964f619270574ce4b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473882"
---
# <a name="updatetypeenum-enumeration-dao"></a>UpdateTypeEnum Enumeration (DAO)


**Betrifft**: Access 2013 | Office 2013

Hiermit geben Sie zusammen mit der **Update**-Methode an, welche Aktualisierungen auf den Datenträger geschrieben werden sollen.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUpdateBatch</p></td>
<td><p>4</p></td>
<td><p>Alle ausstehenden Änderungen im Updatecache werden auf den Datenträger geschrieben.</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>2</p></td>
<td><p>Nur die ausstehenden Änderungen des aktuellen Datensatzes werden auf den Datenträger geschrieben.</p></td>
</tr>
<tr class="odd">
<td><p>dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>(Standard) Ausstehende Änderungen werden nicht zwischengespeichert und werden sofort auf den Datenträger geschrieben.</p></td>
</tr>
</tbody>
</table>
