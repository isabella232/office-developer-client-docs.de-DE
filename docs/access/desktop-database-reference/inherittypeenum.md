---
title: InheritTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bf7d7ceac1e4822344ce4f7ad8a05e09c0429dff
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860567"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Betrifft**: Access 2013 | Office 2013

Gibt an, wie Objekte Berechtigungen erben, die mit [SetPermissions](setpermissions-method-adox.md) festgelegt sind.

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
<td><p><strong>adInheritBoth</strong></p></td>
<td><p>3</p></td>
<td><p>Objekte und andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers</strong></p></td>
<td><p>2</p></td>
<td><p>Andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>0</p></td>
<td><p>Standardeinstellung. Es tritt keine Vererbung auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>4</p></td>
<td><p>Die Flags <strong>adInheritObjects</strong> und <strong>adInheritContainers</strong> werden nicht an einen vererbten Eintrag weitergeleitet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Flags adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>Nicht-Container-Objekte innerhalb des Containers erben die Berechtigungen.</p></td>
</tr>
</tbody>
</table>

