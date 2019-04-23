---
title: ADD USER-Anweisung (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280425"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Fügt einer bestehenden *Gruppe* einen oder mehrere *Benutzer* hinzu.

## <a name="syntax"></a>Syntax

Hinzufügen **\[von Benutzer ** Benutzer, Benutzer,... \] Zur *Gruppe*

Die ADD USER-Anweisung besteht aus den folgenden Komponenten:

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
<td><p>Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzugefügt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Nachdem ein *Benutzer* einer *Gruppe*hinzugefügt wurde, verfügt der *Benutzer* über alle Berechtigungen, die der *Gruppe*erteilt wurden.

