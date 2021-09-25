---
title: CREATE USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5da68a0574bb0e81a403f456e48f6dd1b965b9e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569209"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>CREATE USER- oder GROUP-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt einen oder mehrere neue Benutzer bzw. eine oder mehrere neue Gruppen.

## <a name="syntax"></a>Syntax

### <a name="create-a-user"></a>Erstellen eines Benutzers

CREATE USER *user* *password pid* \[ , *user* *password pid*, ...\]

### <a name="create-a-group"></a>Erstellen einer Gruppe

CREATE GROUP *group* *pid* \[ , *group* *pid*, ...\]

Die CREATE USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>user</em></p></td>
<td><p>Der Name eines Benutzers, der zur Informationsdatei der Arbeitsgruppe hinzugefügt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzuzufügen ist.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Das Kennwort, das dem angegebenen <em>Benutzer</em> zuzuordnen ist.</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Die persönliche ID.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Ein *Benutzer* und eine *Gruppe* können nicht über den gleichen Namen verfügen.

Ein *Kennwort* ist für jeden erstellten *Benutzer* bzw. für jede erstellte *Gruppe* erforderlich.

