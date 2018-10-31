---
title: ADD USER-Anweisung (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 80e3a8fe62cf077accfc18a30e188898fb279d1d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862289"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Fügt einer bestehenden *Gruppe* einen oder mehrere *Benutzer* hinzu.

## <a name="syntax"></a>Syntax

ADD USER *Benutzer*\[, *Benutzer*,... \] *Gruppe*

Die ADD USER-Anweisung besteht aus den folgenden Komponenten:

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
<td><p>Der Name einer Gruppe, der zur Informationsdatei der Arbeitsgruppe hinzugefügt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Nachdem ein *Benutzer* zu einer *Gruppe*hinzugefügt wurde, hat der *Benutzer* alle Berechtigungen, die der *Gruppe*erteilt wurden.

