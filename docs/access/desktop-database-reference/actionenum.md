---
title: ActionEnum (Access-Desktopdatenbankreferenz)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c6d19ba5a19b8c49bb3c95fcc52040be62c364d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569615"
---
# <a name="actionenum"></a>ActionEnum

**Gilt für**: Access 2013, Office 2013

Gibt den Aktionstyp an, der beim Aufruf von [SetPermissions](setpermissions-method-adox.md) ausgeführt werden soll.

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
<td><p><strong>adAccessDeny</strong></p></td>
<td><p>3</p></td>
<td><p>Der Gruppe oder dem Benutzer werden die angegebenen Berechtigungen verweigert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessGrant</strong></p></td>
<td><p>1</p></td>
<td><p>Die Gruppe oder der Benutzer verfügt mindestens über die angeforderten Berechtigungen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAccessRevoke</strong></p></td>
<td><p>4 </p></td>
<td><p>Alle expliziten Zugriffsrechte der Gruppe oder des Benutzers werden aufgehoben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessSet</strong></p></td>
<td><p>2</p></td>
<td><p>Die Gruppe oder der Benutzer verfügen genau über die angeforderten Berechtigungen.</p></td>
</tr>
</tbody>
</table>

