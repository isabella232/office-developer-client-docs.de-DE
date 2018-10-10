---
title: CREATE USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dce5b9a6894eb1e09a0307b389207baefae6aa58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474874"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>CREATE USER- oder GROUP-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

Erstellt einen oder mehrere neue Benutzer bzw. eine oder mehrere neue Gruppen.

## <a name="syntax"></a>Syntax

Zum Erstellen eines Benutzers:

CREATE USER *Benutzer* *Kennwort pid* \[, *Benutzer* *Kennwort pid*,...\]

Zum Erstellen einer Gruppe:

CREATE GROUP *Gruppe* *pid*\[, *Gruppe* *pid*,...\]

Die CREATE USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Komponente</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Benutzer</em></p></td>
<td><p>Der Name eines Benutzers, der der Arbeitsgruppen-Informationsdatei hinzugefügt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>Gruppe</em></p></td>
<td><p>Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzuzufügen ist.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Das Kennwort, das dem angegebenen <em>Benutzer</em> zuzuordnen ist.</p></td>
</tr>
<tr class="even">
<td><p><em>PID</em></p></td>
<td><p>Die persönliche ID.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Ein *Benutzer* und eine *Gruppe* können nicht den gleichen Namen haben.

Ein *Kennwort* ist erforderlich für jeden *Benutzer* oder *Gruppe* , die erstellt wird.

