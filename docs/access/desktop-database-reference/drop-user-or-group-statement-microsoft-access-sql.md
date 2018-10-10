---
title: DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473165"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

Löscht, sofern vorhanden, einen oder mehrere *Benutzer* bzw. eine oder mehrere *Gruppe*(n) oder entfernt, sofern vorhanden, einen oder mehrere *Benutzer* aus einer vorhandenen *Gruppe*.

## <a name="syntax"></a>Syntax

Zum Löschen eines oder mehrerer *Benutzer*(s) bzw. zum Entfernen eines oder mehrerer *Benutzer*(s) aus einer *Gruppe*:

DROP USER *Benutzer*\[, *Benutzer*,... \] \[Aus *Gruppe*\]

Zum Löschen einer oder mehrerer *Gruppe*(n):

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

Wenn das FROM-Schlüsselwort in der DROP USER-Anweisung verwendet wird, werden alle in der Anweisung aufgelisteten *Benutzer* aus der *Gruppe* entfernt, die im Anschluss an das FROM-Schlüsselwort angegeben wird. Die *Benutzer* selbst werden jedoch nicht gelöscht.

Die DROP GROUP-Anweisung dient zum Löschen der angegebenen *Grupppe*(n). Dieser Löschvorgang hat keine Auswirkung auf die *Benutzer*, die Mitglieder der *Gruppe*(n) sind, sie sind lediglich keine Mitglieder der gelöschten *Gruppe*(n) mehr.

