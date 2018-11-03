---
title: DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f9662c4f0cb691136a556faa32cb0d5a1c775268
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936833"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Löscht eine oder mehrere vorhandene *Benutzer* oder *Gruppen*, oder einen oder mehrere vorhandene *Benutzer* aus einer vorhandenen *Gruppe*entfernt.

## <a name="syntax"></a>Syntax

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Löschen Sie einen oder mehrere Benutzer oder entfernen eine oder mehrere Benutzer aus einer Gruppe

DROP USER *Benutzer*\[, *Benutzer*,... \] \[Aus *Gruppe*\]

### <a name="delete-one-or-more-groups"></a>Löschen einer oder mehrerer Gruppen

DROP GROUP *Gruppe*\[, *Gruppe*,...\]

Die DROP USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:

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
<td><p>Der Name eines Benutzers, der aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>Gruppe</em></p></td>
<td><p>Der Name einer Gruppe, die aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn das FROM-Schlüsselwort in der DROP USER-Anweisung verwendet wird, wird jeder in der Anweisung aufgeführte *Benutzer* aus der *Gruppe* angegeben nach der FROM-Schlüsselwort entfernt werden. Jedoch die *Benutzer* selbst nicht gelöscht werden.

Die DROP GROUP-Anweisung löscht die angegebene *Gruppe*(s). Der *Benutzer* , die Mitglieder der *Gruppe*(s) sind nicht betroffen sind, aber sie werden nicht mehr Mitglieder der gelöschten *Gruppe*(s).

