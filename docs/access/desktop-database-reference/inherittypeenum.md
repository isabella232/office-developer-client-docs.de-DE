---
title: InheritTypeEnum (Access-Desktopdatenbankreferenz)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7b4a66853fcb51c617d8afdd9b806a6faa567a2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626372"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Gilt für**: Access 2013, Office 2013

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
<td><p>4 </p></td>
<td><p>Die Flags <strong>adInheritObjects</strong> und <strong>adInheritContainers</strong> werden nicht an einen vererbten Eintrag weitergeleitet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>Nicht-Container-Objekte innerhalb des Containers erben die Berechtigungen.</p></td>
</tr>
</tbody>
</table>

