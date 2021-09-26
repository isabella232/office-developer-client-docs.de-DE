---
title: DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4054256c8a158fdee13af683a4bd80ea93647985
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597436"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER- oder GROUP-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Löscht einen oder mehrere vorhandene *Benutzer* oder *Gruppen* oder entfernt einen oder mehrere vorhandene *Benutzer* aus einer vorhandenen *Gruppe.*

## <a name="syntax"></a>Syntax

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Löschen eines oder mehrerer Benutzer oder Entfernen eines oder mehrerer Benutzer aus einer Gruppe

DROP *USER-Benutzer,* \[ *Benutzer*, ... \] \[ *FROM-Gruppe*\]

### <a name="delete-one-or-more-groups"></a>Löschen einer oder mehrerer Gruppen

DROP *GROUP-Gruppe,* \[ *Gruppe*, ...\]

Die DROP USER- oder GROUP-Anweisung besteht aus folgenden Komponenten:

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
<td><p>Der Name eines Benutzers, der aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>Gruppe</em></p></td>
<td><p>Der Name einer Gruppe, die aus der Informationsdatei für die Arbeitsgruppe entfernt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Wenn das FROM-Schlüsselwort in der DROP USER-Anweisung verwendet wird, werden alle in der Anweisung aufgeführten *Benutzer* aus der *Gruppe* entfernt, die nach dem FROM-Schlüsselwort angegeben wurde. Die *Benutzer* selbst werden jedoch nicht gelöscht.

Die DROP GROUP-Anweisung dient zum Löschen der angegebenen *Grupppe*(n). Die *Benutzer,* die Mitglieder der *Gruppe*(en) sind, sind nicht betroffen, aber sie sind nicht mehr Mitglieder der gelöschten Gruppe(n). 

