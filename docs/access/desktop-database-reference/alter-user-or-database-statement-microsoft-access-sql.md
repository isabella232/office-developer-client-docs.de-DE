---
title: ALTER USER- oder DATABASE-Anweisung (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9e2ef710d9a7036cc9f15e2c69d37e84393f978d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559073"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER- oder DATABASE-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Ändert das Kennwort für einen vorhandenen Benutzer oder eine Datenbank.

## <a name="syntax"></a>Syntax

ALTER DATABASE PASSWORD *NeuesKennwort AltesKennwort*

ALTER USER *Benutzer* PASSWORD *NeuesKennwort AltesKennwort*

Die ALTER USER- oder DATABASE-Anweisung besteht aus den folgenden Komponenten:

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
<td><p>Der Name eines Benutzers, der der Arbeitsgruppen-Informationsdatei hinzugefügt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>Newpassword</em></p></td>
<td><p>Das neue Kennwort, das dem <em>Benutzer</em> oder der <em>Datenbank</em> zugeordnet werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><em>Oldpassword</em></p></td>
<td><p>Das bestehende Kennwort, das dem angegebenen <em>Benutzer</em> oder der angegebenen <em>Gruppe</em> zugeordnet ist.</p></td>
</tr>
</tbody>
</table>

